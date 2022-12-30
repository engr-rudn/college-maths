---
title: "Decorators, class methods, and properties"
teaching: 20
exercises: 25
questions:
- "What is a decorator?"
- "How do I tag methods as being applicable to a class rather than an
  instance?"
- "How can I add logic to process changes to instance variables?"
objectives:
- "Understand the purpose of decorators and how they are implemented"
- "Be able to use `@classmethod` and  `@property`"
keypoints:
- "A decorator adds functionality to a class or function. To use the
  `decoratorname` decorator, add `@decoratorname` one line before the
  class or function definition."
- Use the `@classmethod` decorator to indicate methods to be called
  from the class rather than from an instance.
- Use the `@property` decorator to control access to instance
  variables
---

Sometimes when we are writing software we would like to be able to
attach additional functionality to a variety of functions (or classes)
without writing the functionality directly into the function. Python
gives us some extra syntax to make this easier.

For example, say that we want to track what functions are being called
in our program. We can write a function that will take a function that
we want to track as an argument, and return a new function that
outputs before and after calling the function we are interested in.

~~~
def track_this(function):
    def new_function():
        print("Entering", function)
        function()
        print("Leaving", function)

    return new_function
~~~
{: .language-python}

To test this out:

~~~
def say_hello():
    print("Hello, world.")

say_hello = track_this(say_hello)

def say_goodbye():
    print("See you later.")

say_goodbye = track_this(say_goodbye)

def conversation():
    say_hello()
    say_goodbye()

conversation = track_this(conversation)

conversation()
~~~
{: .language-python}

~~~
Entering <function conversation at 0x1115c07b8>
Entering <function say_hello at 0x11143be18>
Hello, world.
Leaving <function say_hello at 0x11143be18>
Entering <function say_goodbye at 0x1115c0e18>
See you later.
Leaving <function say_goodbye at 0x1115c0e18>
Leaving <function conversation at 0x1115c07b8>
~~~
{: .output}

So we can now see in more detail what's going on as we move through
this program. However, having to set each function to the result of
calling `track_this` on the function is laborious; it would be nicer
if there were an easier way to do this, and thankfully Python gives us
one.

~~~
@track_this
def say_hello():
    print("Hello, world.")

@track_this
def say_goodbye():
    print("See you later.")

@track_this
def conversation():
    say_hello()
    say_goodbye()

conversation()
~~~
{: .language-python}

Using `@` followed by the name of the altering function (`track_this`
in this case), and placing this before the function definition, Python
takes the result of calling the altering function and overwrites the
new function with it.

This syntax is called a "decorator"; the functions `say_hello`,
`say_goodbye`, and `conversation` have been decorated with the
`track_this` decorator.

Our `@track_this` decorator is currently not very general. We can see
a problem when we try and decorate a function that takes arguments:

> ## Decorators and arguments
>
> ~~~
> @track_this
> def say_something(thing_to_say):
>     print(thing_to_say)
>
> say_something("Hello there")
> ~~~
> {: .language-python}
>
> ~~~
> TypeError                                 Traceback (most recent call last)
> <ipython-input-29-000c7283eed1> in <module>()
>       3     print(thing_to_say)
>       4
> ----> 5 say_something("Hello there")
>
> TypeError: new_function() takes 0 positional arguments but 1 was given
> ~~~
> {: .output}
>
> To make this more flexible, we can rewrite the `track_this`
> decorator as:
>
> ~~~
> def track_this(function):
>     def new_function(*args, **kwargs):
>         print("Entering", function)
>         function(*args, **kwargs)
>         print("Leaving", function)
>
>     return new_function
> ~~~
> {: .language-python}
>
> The `*` and `**` here carry two meanings. In the definition `def
> new_function(*args, **kwargs)`, they mean "take any positional
> arguments and put them into a list called `args`, and take any
> keyword arguments and put them into a dict called `kwargs`. In the
> function call `function(*args, **kwargs)`, they mean "pass each
> element of the list `args` as a separate argument, and pass each
> element of the dict `kwargs` as a keyword argument.
>
> You can also write and use decorators that themselves accept
> arguments by using a nested function definition, but we won't go
> into detail about this today.
{: .callout}

> ## Double checking
>
> Try writing a decorator that checks the result of a computation is
> consistent by running it twice and checking the outputs are
> equal. This should return the result if it is consistent, and raise
> an exception otherwise. Test it by decorating the `area` and
> `perimeter` methods of the `Polygon` and `Triangle` classes from the
> previous episode.
>
>> ## Solution
>>
>> ~~~
>> class InconsistentResultsError(AssertionError):
>>     pass
>>
>>
>> def check_consistency(function):
>>     def consistent_function(*args, **kwargs):
>>         results = [function(*args, **kwargs) for _ in range(2)]
>>         if results[0] != results[1]:
>>             raise InconsistentResultsError
>>         return results[0]
>>
>>     return consistent_function
>>
>>
>> class Polygon:
>>     def __init__(self, side_lengths):
>>         filtered_side_lengths = []
>>         for side_length in side_lengths:
>>             assert side_length >= 0
>>             if side_length > 0:
>>                 filtered_side_lengths.append(side_length)
>>         self.side_lengths = filtered_side_lengths
>>
>>     @check_consistency
>>     def perimeter(self):
>>         '''Returns the perimeter of the polygon.'''
>>         return sum(self.side_lengths)
>>
>> class Triangle(Polygon):
>>     def __init__(self, side_lengths):
>>         # Triangles have three sides
>>         super().__init__(side_lengths)
>>         assert len(self.side_lengths) == 3
>>
>>     @check_consistency
>>     def area(self):
>>         '''Returns the area of the triangle.'''
>>         a, b, c = self.side_lengths
>>         p = (a + b + c) / 2
>>         return (p * (p - a) * (p - b) * (p - c)) ** 0.5
>>
>> a_triangle = Triangle([3, 4, 5])
>> print("Perimeter:", a_triangle.perimeter())
>> print("Area:", a_triangle.area())
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}


## Class methods

Sometimes we want to write functions associated with classes that are
relevant to the class as a whole, rather than to one specific
instance. We can do this by adding the `@classmethod` decorator to a
method.

Class methods are most frequently used as specialised constructors,
to create instances of the class without having to supply every
argument to `__init__`.

For example, revisiting the `Triangle` class from earlier, we may want
to be able to define an equilateral triangle by giving a single side
length.

~~~
class Triangle(Polygon):
    def __init__(self, side_lengths):
        # Triangles have three sides
        super().__init__(side_lengths)
        assert len(self.side_lengths) == 3

    @classmethod
    def equilateral(cls, side_length):
        return cls([side_length] * 3)

    def area(self):
        '''Returns the area of the triangle.'''
        a, b, c = self.side_lengths
        p = (a + b + c) / 2
        return (p * (p - a) * (p - b) * (p - c)) ** 0.5
~~~
{: .language-python}

Notice that in addition to adding the `@classmethod` decorator, the
first argument which is usually `self` has been replaced with
`cls`. Since class methods aren't specific to a particular instance,
there is no need to have the `self` argument referring to
it. Conversely, it is useful to be able to refer to the specific class
without having to do this by name, since in general we would like
class methods to work and return the correct type of class for
subclasses as well.

Let's test this now.

~~~
e_triangle = Triangle.equilateral(1.5)
print("Perimeter:", e_triangle.perimeter())
print("Area:", e_triangle.area())
~~~
{: .language-python}

~~~
Perimeter: 4.5
Area: 0.9742785792574935
~~~
{: .output}

Now we only need to supply a single number, the length of the side,
and the `equilateral` class method constructs the list of three equal
side lengths from this, returning a `Triangle` with three equal sides.

> ## Squares
>
> Add a class method to the `Rectangle` class which you wrote in the
> previous episode to create a square, given the length of its side.
>
>> ## Solution
>>
>> ~~~
>> class Rectangle(Polygon):
>>     def __init__(self, side_lengths):
>>         super().__init__(side_lengths)
>>         num_sides = len(self.side_lengths)
>>         assert num_sides == 2 or num_sides == 4
>>         if num_sides == 2:
>>             width, height = side_lengths
>>             self.side_lengths = [width, height, width, height]
>>         else:
>>             assert self.side_lengths[0] == self.side_lengths[2]
>>             assert self.side_lengths[1] == self.side_lengths[3]
>>
>>     def area(self):
>>         return self.side_lengths[0] * self.side_lengths[1]
>>
>>     @classmethod
>>     def square(cls, side_length):
>>         return cls([side_length] * 4)
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}


## Properties

In general, when working with classes, there is an assumption that
instance variables can be modified, unless something is done to
prevent this. In some languages, variables can be defined as
read-only, or private so that they cannot be seen from outside of the
class. Python has neither of these&mdash;any instance variable can be
modified by any piece of code using the class. There is, however, a
convention that variables and methods whose names begin with `_` are
private to the implementation&mdash;while they can be accessed from
outside the class, they are not guaranteed to remain stable between
versions, and the class doesn't guarantee to behave well if they are
changed.

To look at a specific example, what happens if we take the `Triangle`
class and change `side_lengths`?

~~~
a_triangle = Triangle([3, 4, 5])
a_triangle.side_lengths = [3, 4, 5, 6]
print(a_triangle.area())
~~~
{: .language-python}

~~~
     11     def area(self):
     12         '''Returns the area of the triangle.'''
---> 13         a, b, c = self.side_lengths
     14         p = (a + b + c) / 2
     15         return (p * (p - a) * (p - b) * (p - c)) ** 0.5

ValueError: too many values to unpack (expected 3)
~~~
{: .output}

Our implementation of `area` assumes that `side_lengths` was validated
by `__init__` and so has three elements, all positive. By adding a
fourth, the implementation becomes broken as a list of four elements
can't be unpacked to three variables. Similarly,

~~~
a_polygon = Polygon([1, 2, 3, 4, 5])
a_polygon.side_lengths = 'spam and eggs'
a_polygon.perimeter()
~~~
{: .language-python}

~~~
TypeError                                 Traceback (most recent call last)
<ipython-input-50-9b8ffd74de36> in <module>()
      1 a_polygon = Polygon([1, 2, 3, 4, 5])
      2 a_polygon.side_lengths = 'spam and eggs'
----> 3 a_polygon.perimeter()

<ipython-input-49-5ae60040e7be> in perimeter(self)
     10     def perimeter(self):
     11         '''Returns the perimeter of the polygon.'''
---> 12         return sum(self.side_lengths)
     13
     14

TypeError: unsupported operand type(s) for +: 'int' and 'str'
~~~
{: .output}

It doesn't make sense to take the sum of a string (or more precisely,
to add the individual characters together), so this also fails.

One way to fix this is to signal that this shouldn't happen is to mark
`side_lengths` as private by renaming it to `_side_lengths`. However,
this removes some potentially useful functionality&mdash;it would
definitely be useful for a user of the class to be able to read the
side lengths, just not write them directly. Python provides us with an
`@property` decorator that lets us do this.

~~~
class Polygon:
    def __init__(self, side_lengths):
        filtered_side_lengths = []
        for side_length in side_lengths:
            assert side_length >= 0
            if side_length > 0:
                filtered_side_lengths.append(side_length)
        self._side_lengths = filtered_side_lengths

    def perimeter(self):
        '''Returns the perimeter of the polygon.'''
        return sum(self._side_lengths)

    @property
    def side_lengths(self):
        return self._side_lengths
~~~
{: .language-python}

We have done two things here: `self.side_lengths` has been renamed to
`self._side_lengths`, indicating that it is intended to be considered
as private to the class. We have also added a new method
`side_lengths`, and decorated that with the `@property`
decorator. This allows the result of calling this function to be
accessed as though it were an instance variable:

~~~
a_polygon = Polygon([1, 2, 3, 4, 5])
print(a_polygon.side_lengths)
~~~
{: .language-python}

~~~
[1, 2, 3, 4, 5]
~~~
{: .output}

However, we can't assign to it without referring to the private
`_side_lengths`:

~~~
a_polygon.side_lengths = 'spam and eggs'
~~~
{: .language-python}

~~~
AttributeError                            Traceback (most recent call last)
<ipython-input-57-9b8ffd74de36> in <module>()
      1 a_polygon = Polygon([1, 2, 3, 4, 5])
----> 2 a_polygon.side_lengths = 'spam and eggs'
      3 a_polygon.perimeter()

AttributeError: can't set attribute
~~~
{: .output}

So we have now successfully "protected" our class from changes that
will break it, by signalling to users of it what is internal to the
implementation, and what is designed for them to use. However, we have
still removed a little functionality in the process&mdash;previously,
a user could change `side_lengths` without breaking things, provided
that they were careful (since the consistency checks of `__init__`
were being bypassed), whereas now this is not supported behaviour
(even if it is possible).

What we would like is to offer the ability to set the value for the
property, but add some kind of validation function that does that
rather than allowing it to be assigned directly. This kind of function
is called a _setter_, and the `@property` decorator in fact allows us
to create one. (The first function, which gets the value, is referred
to as a _getter_.)

~~~
class Polygon:
    def __init__(self, side_lengths):
        self.side_lengths = side_lengths

    def perimeter(self):
        '''Returns the perimeter of the polygon.'''
        return sum(self._side_lengths)

    @property
    def side_lengths(self):
        return self._side_lengths

    @side_lengths.setter
    def side_lengths(self, side_lengths):
        filtered_side_lengths = []
        for side_length in side_lengths:
            assert side_length >= 0
            if side_length > 0:
                filtered_side_lengths.append(side_length)
        self._side_lengths = filtered_side_lengths
~~~
{: .language-python}

We've moved the validation logic into the method `side_length`, as
decorated by the `@side_lengths.setter` decorator, and the `__init__`
method uses this to do its initial setup. Testing this:

~~~
a_polygon = Polygon([1, 2, 3, 4, 5])
print("Original perimeter:", a_polygon.perimeter())
a_polygon.side_lengths = ([1, 2, 3, 4, 5, 6])
print("Modified perimeter:", a_polygon.perimeter())
~~~
{: .language-python}

~~~
Original perimeter: 15
Modified perimeter: 21
~~~
{: .output}

> ## More robust plotters
>
> Adjust the `FunctionPlotter`, `PolynomialPlotter`, or
> `QuadraticPlotter` example from earlier to make `color` a property,
> with a getter and a setter, with the setter checking that the the
> color is a valid matplotlib color.
>
>> ## Solution
>>
>> ~~~
>> from numpy import linspace
>> from matplotlib.pyplot import subplots
>> from matplotlib.colors import is_color_like
>>
>> class FunctionPlotter:
>>     def __init__(self, color='red', linewidth=1, x_min=-10, x_max=10):
>>         self.color = color
>>         self.linewidth = linewidth
>>         self.x_min = x_min
>>         self.x_max = x_max
>>
>>     @property
>>     def color(self):
>>         return self._color
>>
>>     @color.setter
>>     def color(self, color):
>>         assert is_color_like(color)
>>         self._color = color
>>
>>     def plot(self, function):
>>         '''Plot a function of a single argument.
>>         The line is plotted in the colour specified by color, and with width
>>         linewidth.'''
>>         fig, ax = subplots()
>>         x = linspace(self.x_min, self.x_max, 1000)
>>         ax.plot(x, function(x), color=self._color, linewidth=self.linewidth)
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}
