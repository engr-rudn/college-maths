---
title: "Inheritance"
teaching: 20
exercises: 20
questions:
- "How can classe relationships where one represents a specific subset
of another be represented?"
- "How can functionality on one class be overridden or extended by its
children?"
objectives:
- "Be able to use inheritance to construct parent-child relationships between
classes"
- "Be able to override methods on child classes, and refer back to the parent class's implementations"
- "<a href='https://pfur-my.sharepoint.com/:v:/g/personal/teklay_ty_pfur_ru/ERw5Fw8Kg1JIkcBW-grYVpoBLeA_cNH5aUcqbcE1JIvwqQ?e=3wpZXb' target='_blank'> View Lecture Video</a>"

keypoints:
- "Adding a class in parentheses after a class definition indicates
that the new class is a subclass of the bracketed class (parent class)."
- "The subclass inherits all of that parent class's attributes and methods."
- "Defining a method with the same name as one of the parent class's overrides
it."
- "Use `super()` to access parent classes and their methods."
---

We have talked about using classes as a way to reduce repetition in the
software we write. However, what happens if we want to write two classes that
do similar but distinct things? For example, if we wanted to write a
`CubicPlotter` as well as our `QuadraticPlotter`, would we need to repeat all
of the code common to both of them? What if we wanted a `QuarticPlotter` and a
`QuinticPlotter` as well? This repetitive code would quickly start to build
up...

Thankfully, Python (and most other languages that have classes) give us a
mechanism to avoid this in the form of _inheritance_. A class that inherits
from a second class automatically gains all of the second's attributes and
methods. The class that is being inherited from is called the _parent class_,
_superclass_, or _base class_, while the new class inheriting from it is called
the _child class_, _subclass_, or _derived class_.

We saw earlier that `ValueError` is a subclass of `Exception`, and that this
can be used to handle both specific and more general exceptions in a
hierarchy. We can also use this to define our own exceptions. Say, for
example, we have a function to convert temperatures from degrees Celsius to
degrees Fahrenheit,
\\(\theta_{\mathrm{F}}(\theta_{\mathrm{C}})=\frac{9}{5}\theta_{\mathrm{C}} +
32\\).
We know that temperatures below absolute zero are not valid, so if we
encounter those in our code we would like to raise the alarm as soon as
possible; we could do this with an `assert`, but another way of expressing this
could be by defining our own exception to flag this. A temperature below
\\(-273.15^\circ\mathrm{C}\\) is an example of a bad _value_, so this would want to
inherit from `ValueError`.

~~~
class InvalidTemperatureError(ValueError):
    pass

def celsius_to_fahrenheit(temperature_c):
    if temperature_c < -273.15:
        raise InvalidTemperatureError
    return temperature_c * 9 / 5 + 32
~~~
{: .language-python}

The `pass` keyword here tells Python that while we have started an indented
block, we don't actually have anything to put in it. (If we were to omit it,
Python would complain at us that it expected a block and didn't get one.) So we
have constructed a new class called `InvalidTemperatureError`, which is an
exact copy of `ValueError`, except that it knows that `ValueError` is its
parent. Let's test this.

~~~
for temperature_c in 0, 100, -300:
    print(temperature_c, "degrees Celsius is",
          celsius_to_fahrenheit(temperature_c), "degrees Fahrenheit")
~~~
{: .language-python}

~~~
0 degrees Celsius is 32.0 degrees Fahrenheit
100 degrees Celsius is 212.0 degrees Fahrenheit
Traceback (most recent call last):
  File "<stdin>", line 3, in <module>
  File "<stdin>", line 3, in celsius_to_fahrenheit
__main__.InvalidTemperatureError
~~~
{: .output}

If we wanted to, we could catch this exception with `except
InvalidTemperatureError` or with `except ValueError` (or even `except
Exception`).

What about if we want to add functionality? Let's consider an example
of a `Polygon` class, which can calculate its perimeter.

~~~
class Polygon:
    def __init__(self, side_lengths):
        self.side_lengths = side_lengths

    def perimeter(self):
        '''Returns the perimeter of the polygon.'''
        return sum(self.side_lengths)

some_shape = Polygon([1, 2, 3, 4, 5])
print(some_shape.perimeter())
~~~
{: .language-python}

~~~
15
~~~
{: .output}

Now, we know more about triangles than we do about generic polygons,
so we can create a specialised subclass of `Polygon` called
`Triangle`. For example, for a triangle of sides \\(a\\), \\(b\\), and \\(c\\),
Heron's formula states that the perimeter of the triangle is given by
\\(\sqrt{p(p-a)(p-b)(p-c)}\\), where \\(p=\frac{1}{2}(a+b+c)\\).

~~~
class Triangle(Polygon):
    def __init__(self, side_lengths):
        # Triangles have three sides
        assert len(side_lengths) == 3
        self.side_lengths = side_lengths

    def area(self):
        '''Returns the area of the triangle.'''
        a, b, c = self.side_lengths
        p = self.perimeter() / 2
        return (p * (p - a) * (p - b) * (p - c)) ** 0.5

a_triangle = Triangle([3, 4, 5])
print("Perimeter:", a_triangle.perimeter())
print("Area:", a_triangle.area())
~~~
{: .language-python}

~~~
Perimeter: 12
Area: 6.0
~~~
{: .output}

We've done a few new things here. Firstly, we've overridden the
`__init__` method of the `Polygon` parent class, since we now need to
check that the sides that the shape is being given form a triangle,
and not some other shape. This means that only the `__init__` method
from the `Triangle` class is called, and not the one in the `Polygon`
class. Next, we've defined a new method `area`, which is only
available on the `Triangle` class. We've also called the `perimeter`
method, which is defined on the `Polygon` parent class&mdash;we don't
have to recreate this, since we can use it as-is.

One niggling issue is that we are still repeating ourselves a little
here. The line `self.side_lengths = side_lengths` appears in the
`__init__` method of both classes. If we can, we'd like to remove this
by using the equivalent method from the `Polygon` class. In principle
we could use `Polygon.__init__`, but this still has some repetition,
since we have to specify the name of the `Polygon` class more than
once, even though the class knows what its parent class is.

What we can do instead is make use of the `super()` function. This
gives us access to the superclass (and any superclasses further up the
chain), without having to refer to any one of them by name. When we
call a method of the `super()` object, Python automatically works its
way up the tree until the first class which has a method of the
correct name, and calls that. The `Triangle` class would then become:

~~~
class Triangle(Polygon):
    def __init__(self, side_lengths):
        # Triangles have three sides
        assert len(side_lengths) == 3
        super().__init__(side_lengths)

    def area(self):
        '''Returns the area of the triangle.'''
        a, b, c = self.side_lengths
        p = (a + b + c) / 2
        return (p * (p - a) * (p - b) * (p - c)) ** 0.5
~~~
{: .language-python}

(You can see that `super()` has also taken care of the `self` argument
for us, which using `Polygon` directly wouldn't do.)

While in this case we have only saved a single line of repetition,
making use of `super()` becomes essential as methods become
increasingly complex and build up functionality in layers.

> ## Not implemented
>
> If we anticipate a lot of subclasses may provide a particular
> method, but we can't or don't want to provide it on the superclass,
> we can add a stub method that raises `NotImplementedError` instead,
> so that it becomes clear if an implementation has been
> forgotten. For example, the `area` method of `Polygon` could be:
>
> ~~~
> def area(self):
>     raise NotImplementedError
> ~~~
> {: .language-python}
{: .callout}

> ## Inheriting from `object`
>
> Sometimes in older Python you will see classes inherit from
> `object`. This is a holdover from Python 2, where this was needed to
> create a "new-style" class instead of an "old-style"
> class. Old-style classes were removed in Python 3, with all classes
> being new-style ones which inherit from `object` automatically, so
> you don't need to (and shouldn't) do this any more.
{: .callout}

> ## `super()` placement
>
> A four-sided shape where one of the side lengths is zero is a
> triangle. We can adjust the `__init__` method of the `Polygon`
> to reflect this by removing any zero-length sides before storing
> the list of side lengths. The method then becomes:
>
> ~~~
> def __init__(self, side_lengths):
>     filtered_side_lengths = []
>     for side_length in side_lengths:
>         assert side_length >= 0
>         if side_length > 0:
>             filtered_side_lengths.append(side_length)
>     self.side_lengths = filtered_side_lengths
> ~~~
> {: .language-python}
>
> How does this affect our implementation of `Triangle.__init__`?
> Adjust this so that `Triangle([3, 4, 0, 5])` works, and
> `Triangle([3, 4, 0])` does not.
>
>> ## Solution
>>
>> We now need to call `super().__init__` _before_ checking the
>> lengths, and check the resulting instance variable rather than the
>> `side_lengths` argument.
>>
>> ~~~
>> class Polygon:
>>     def __init__(self, side_lengths):
>>         filtered_side_lengths = []
>>         for side_length in side_lengths:
>>             assert side_length >= 0
>>             if side_length > 0:
>>                 filtered_side_lengths.append(side_length)
>>         self.side_lengths = filtered_side_lengths
>>
>>     def perimeter(self):
>>         '''Returns the perimeter of the polygon.'''
>>         return sum(self.side_lengths)
>>
>>  class Triangle(Polygon):
>>     def __init__(self, side_lengths):
>>         # Triangles have three sides
>>         super().__init__(side_lengths)
>>         assert len(self.side_lengths) == 3
>>
>>     def area(self):
>>         '''Returns the area of the triangle.'''
>>         a, b, c = self.side_lengths
>>         p = (a + b + c) / 2
>>         return (p * (p - a) * (p - b) * (p - c)) ** 0.5
>>
>> a_triangle = Triangle([3, 4, 0, 5])
>> print("Perimeter:", a_triangle.perimeter())
>> print("Area:", a_triangle.area())
>> b_triangle = Triangle([3, 4, 0])
>> ~~~
>> {: .language-python}
>>
>> ~~~
>> Perimeter: 12
>> Area: 6.0
>> ---------------------------------------------------------------------------
>> AssertionError                            Traceback (most recent call last)
>> <ipython-input-17-751f0372a229> in <module>()
>>      27 print("Perimeter:", a_triangle.perimeter())
>>      28 print("Area:", a_triangle.area())
>> ---> 29 b_triangle = Triangle([3, 4, 0])
>>
>> <ipython-input-17-751f0372a229> in __init__(self, side_lengths)
>>      16         # Triangles have three sides
>>      17         super().__init__(side_lengths)
>> ---> 18         assert len(self.side_lengths) == 3
>>      19
>>      20     def area(self):
>>
>> AssertionError:
>> ~~~
>> {: .output}
>>
>> Where to place your call to `super()` is an important thing to
>> consider when writing subclasses!
> {: .solution}
{: .challenge}

> ## Rectangles
>
> Write another subclass of `Polygon` to represent rectangles, and add
> a method to calculate their area.
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
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}

> ## Polynomial plotters
>
> In the previous episode, we wrote a `QuadraticPlotter` class for
> plotting quadratic functions. We know, however, that quadratics are
> not the only type of polynomial in the world.
>
> Write a `PolynomialPlotter` class similar to `QuadraticPlotter`, and
> rewrite `QuadraticPlotter` to be a subclass of it.
>
>> ## Solution
>>
>> ~~~
>> from numpy import linspace
>> from matplotlib.pyplot import subplots
>> from matplotlib.colors import is_color_like
>>
>> class PolynomialPlotter:
>>     def __init__(self, color='red', linewidth=1, x_min=-10, x_max=10):
>>         assert is_color_like(color)
>>         self.color = color
>>         self.linewidth = linewidth
>>         self.x_min = x_min
>>         self.x_max = x_max
>>
>>     def polynomial(self, x, coefficients):
>>         '''For a given x and list of n+1 coefficients [a, b, c, d, ...],
>>         returns the polynomial f(x) = ax^n + bx^(n-1) + cx^(n-2) + ...'''
>>         result = 0
>>         for coefficient in coefficients:
>>             result = result * x + coefficient
>>         return result
>>
>>     def plot(self, coefficients):
>>         '''Given the list of coefficients [a, b, c, d, ...],
>>         plot the polynomial f(x) = ax^n + bx^(n-1) + cx^(n-2) + ... .
>>         The line is plotted in the colour specified by color, and with width
>>         linewidth.'''
>>         fig, ax = subplots()
>>         x = linspace(self.x_min, self.x_max, 1000)
>>         ax.plot(x, self.polynomial(x, coefficients),
>>                 color=self.color, linewidth=self.linewidth)
>>
>> class QuadraticPlotter(PolynomialPlotter):
>>     def plot(self, a, b, c):
>>         super().plot([a, b, c])
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}

> ## More general function plotters
>
> Taking this a step further, write a more general `FunctionPlotter`
> class, and adjust `PolynomialPlotter` to be a subclass of it.
>
>> ## Solution
>>
>> ~~~
>> class FunctionPlotter:
>>     def __init__(self, color='red', linewidth=1, x_min=-10, x_max=10):
>>         assert is_color_like(color)
>>         self.color = color
>>         self.linewidth = linewidth
>>         self.x_min = x_min
>>         self.x_max = x_max
>>
>>     def plot(self, function):
>>         '''Plot a function of a single argument.
>>         The line is plotted in the colour specified by color, and with width
>>         linewidth.'''
>>         fig, ax = subplots()
>>         x = linspace(self.x_min, self.x_max, 1000)
>>         ax.plot(x, function(x), color=self.color, linewidth=self.linewidth)
>>
>>
>> class PolynomialPlotter(FunctionPlotter):
>>     def plot(self, coefficients):
>>         '''Given the list of coefficients [a, b, c, d, ...],
>>         plot the polynomial f(x) = ax^n + bx^(n-1) + cx^(n-2) + ... .
>>         The line is plotted in the colour specified by color, and with width
>>         linewidth.'''
>>         def polynomial(x):
>>             '''For a given x and list of n+1 coefficients [a, b, c, d, ...],
>>             returns the polynomial f(x) = ax^n + bx^(n-1) + cx^(n-2) + ...'''
>>             result = 0
>>             for coefficient in coefficients:
>>                 result = result * x + coefficient
>>             return result
>>         super().plot(polynomial)
>>
>>
>> class QuadraticPlotter(PolynomialPlotter):
>>     def plot(self, a, b, c):
>>        '''Plot the line a * x ** 2 + b * x + c and output to the screen.
>>        x runs between x_min and x_max, with 1000 intermediary points.
>>        The line is plotted in the colour specified by color, and with width
>>        linewidth.'''
>>         super().plot([a, b, c])
>> ~~~
>> {: .language-python}
>>
>> Defining a function within another function as we do in
>> `PolynomialPlotter` is a useful way of
>> parametrising functions without having to pass arguments every time.
> {: .solution}
{: .challenge}
