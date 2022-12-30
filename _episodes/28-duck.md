---
title: "Duck typing and interfaces"
teaching: 10
exercises: 15
questions:
- "How does Python decide what you can and can't do with an object?"
- "When is inheritance not appropriate?"
- "What alternatives are there to inheritance?"
objectives:
- "Understand how duck typing works, and how interfaces assist with
  understanding this."
- "Understand the circumstances where inheritance can be a hindrance
  rather than a help."
- "Be aware of concepts such as composition which can help where
  inheritance fails."
keypoints:
- "Provided a class exposes all required functionality for an
  operation to work, Python allows it."
- "Only use inheritance to express relationships where the subclass is
  the same kind of thing as the superclass."
- "Implementing interfaces and adding functionality with composition
  can be better alternatives to inheritance in some cases."
---

There is a principle that if something "looks like a duck, and swims
like a duck, and quacks like a duck, then it is probably a duck".

{% include image.html url="../assets/img/duck.jpg"
alt="Photograph of a duck and three ducklings on a body of
water" caption="These ducks are swimming and look like ducks, although
the quacking can't be guaranteed from this image."%}

Python's type system adopts a similar philosophy&mdash;if it looks,
swims, and quacks like a duck, and that's the only duck-like aspects
that we need at a particular time, then as far as Python is concerned,
then it _is_ a duck.

For example, the Newton&ndash;Raphson method solves equations of the form
\\(f(x)=0\\) iteratively from a starting point \\(x_0\\) as
\\[x_{n+1}=x_n - \frac{f(x_n)}{f'(x_n)}\;.\\]
We could implement this in Python as:

~~~
def newton(function, derivative, initial_estimate, num_iters=10):
    '''Solves the equation `function`(x) == 0 using the Newton&ndash;Raphson
    method with `num_iters` iterations, starting from `initial_estimate`.
    `derivative` is the derivative of `function` with respect to x.'''

    current_estimate = initial_estimate
    for _ in range(num_iters):
        current_estimate = (
            current_estimate
            - function(current_estimate) / derivative(current_estimate)
        )
    return current_estimate
~~~
{: .language-python}

This clearly works with functions that operate on and return real
numbers.

~~~
from math import sin, cos

print(newton(sin, cos, 1))
print(newton(sin, cos, 2))
print(newton(sin, cos, 1.5))
~~~
{: .language-python}

~~~
0.0
3.141592653589793
-12.566370614359172
~~~
{: .output}

If you only planned for this to work with real numbers, you might
think of adding a check at the start of the function that the
`initial_estimate` given is a real number, or that each successive
`current_estimate` is real. However, if we think about this in a duck
typed way, we don't really need to care about this&mdash;provided that
the values can be subtracted and divided, and `function` and
`derivative` can operate on them, then the algorithm will work.

This means that we can apply this function to cases we may not have
considered. For example, when \\(f(z)\\) is a polynomial, then
plotting the solution \\(z_n\\) (which is now a complex number) obtained
as a function of the initial estimate \\(z_0\\) gives us Newton's
fractal.

~~~
%matplotlib inline
from numpy import angle, linspace, newaxis, pi
from matplotlib.pyplot import colorbar, subplots

def complex_linspace(lower, upper, num_real, num_imag):
    real_space = linspace(lower.real, upper.real, num_real)
    imag_space = linspace(lower.imag, upper.imag, num_imag) * 1J
    return real_space + imag_space[:, newaxis]

def test_polynomial(x):
    return x ** 3 - 1

def test_derivative(x):
    return 3 * x ** 2


z_min = -1 - 1J
z_max = 1 + 1J
initial_z = complex_linspace(z_min, z_max, 1000, 1000)

results = newton(test_polynomial, test_derivative, initial_z, 20)

fig, ax = subplots()
image = ax.imshow(angle(results), vmin=-3, vmax=3,
                  extent=(z_min.real, z_max.real, z_min.imag, z_max.imag))
cbar = colorbar(image, ax=ax, ticks=(-2*pi/3, 0, 2*pi/3))
cbar.set_label(r'$\arg(z_n)$')
cbar.ax.set_yticklabels((r'$-\frac{2\pi}{3}$', '0', r'$\frac{2\pi}{3}$'))
ax.set_xlabel(r'$\operatorname{Re}(z_0)$')
ax.set_ylabel(r'$\operatorname{Im}(z_0)$')
~~~
{: .language-python}

Because our Newton&ndash;Raphson function was duck typed, it
automatically worked for this problem, despite this problem requiring
Numpy arrays of complex numbers rather than the real numbers we
thought we were writing for.


## Protocols

It is frequently useful to codify exactly what requirements are placed
on an object (or duck) so that we can design classes to match. In
Python, when these requirements are documented, the specification is
called a _protocol_; you may also hear the word (informal) _interface_
used to describe this as well.

An example of a well-known protocol in Python is the iterator
protocol, which should be obeyed by objects returned by the
`__iter__()` method. For a class to support the iterator protocol, it
must have two methods:

* `__iter__()`, which returns the object itself. (This is so that an
  iterator can be given to a `for` loop directly, which is sometimes
  desirable rather than relying on it being returned by the
  `__iter__()` method of a collection-type object.)
* `__next__()`, which returns the next item in the sequence. If there
  are no more items, then this should raise the `StopIteration`
  exception, and successive calls should keep raising this exception.

For instance, an iterator that returns the Fibonacci numbers up to
some upper bound may look something like:

~~~
class FibonacciIterator:
    def __init__(self, max_value):
        self.max_value = max_value
        self.last_two_numbers = (1, 0)

    def __iter__(self):
        return self

    def __next__(self):
        next_number = sum(self.last_two_numbers)
        self.last_two_numbers = (self.last_two_numbers[1], next_number)
        if self.max_value < next_number:
            raise StopIteration
        else:
            return next_number
~~~
{: .language-python}

This is an example of where we want to use the iterator directly with
the `for` loop, since we want to initialise it with a
`max_value`. Testing this:

~~~
for number in FibonacciIterator(100):
    print(number)
~~~
{: .language-python}

~~~
1
1
2
3
5
8
13
21
34
55
89
~~~
{: .output}

> ## Triangular numbers
>
> Write a class that implements the iterator protocol and that returns
> the first \\(n\\) triangular numbers. These are defined such that
> the \\(n\\)th triangular number is the sum of the first \\(n\\)
> positive integers, so the first five are 1, 3, 6, 10, and 15.
>
> What would happen if you removed the upper bound (and so never
> raised `StopIteration`) and used the iterator in a `for` loop? When
> might this behaviour be useful?
>
>> ## Solution
>>
>> ~~~
>> class TriangularIterator:
>>     def __init__(self, n):
>>         self.n = n
>>         self.total = 0
>>         self.index = 0
>>
>>     def __iter__(self):
>>         return self
>>
>>     def __next__(self):
>>         if self.index >= self.n:
>>             raise StopIteration
>>         self.index += 1
>>         self.total += self.index
>>         return self.total
>> ~~~
>> {: .language-python}
>>
>> A loop over an iterator that can't raise `StopIteration` will run
>> forever. This could be useful if you're using `zip()` to iterate
>> over another, bounded, iterable at the same time; then each element
>> will get a corresponding triangular number, no matter how many
>> elements there are.
> {: .solution}
{: .challenge}

> ## Spot the problem
>
> Look back at the solutions for the `QuadraticPlotter`,
> `PolynomialPlotter`, and `FunctionPlotter`. What problems do you see
> with the `plot` method of these classes?
>
>> ## Solution
>>
>> The arguments to `FunctionPlotter.plot()`, `PolynomialPlotter.plot()`,
>> and `QuadraticPlotter.plot()` are all different&mdash;one expects a
>> callable, one expects a list of coefficients as one argument, and
>> one expects three coefficients as separate arguments. In general,
>> specialistations of a class should keep the same interface to its
>> functions, and the parent class should be interchangeable with its
>> specialisations.
> {: .solution}
{: .challenge}

> ## Over to you
>
> Thinking about your own research software, what kind of places might
> an interface be useful to better codify how different parts of the
> software interact?
{: .challenge}


## Abstract base classes

Python also allows us to go a step further than a protocol, and
formalise the requirements we place on our interfaces in code. An
_abstract base class_ is a class that must be inherited from&mdash;you
can't create instances of it directly. Python provides these for many
of its protocols in the `collections.abc` module. For example, the
Fibonacci iterator above could inherit from `abc.Iterator`. This would
allow other code to check in advance that it supports the protocol,
and also would guard against us forgetting to implement some part of
the protocol. For example, if we forgot the `__next__()` method:

~~~
from collections.abc import Iterator
class FibonacciIterator(Iterator):
    def __init__(self, max_value):
        self.max_value = max_value
        self.last_two_numbers = (1, 0)

    def __iter__(self):
        return self

for number in FibonacciIterator(100):
    print(number)
~~~
{: .language-python}

In this case Python gives us an error:

~~~
TypeError                                 Traceback (most recent call last)
<ipython-input-3-a96ac2788df3> in <module>
      5         self.last_two_numbers = (1, 0)
      6
----> 7 for number in FibonacciIterator(100):
      8     print(number)

TypeError: Can't instantiate abstract class FibonacciIterator with abstract methods __next__
~~~
{: .output}

This can be useful when working with more complex interfaces. (On the
other hand, removing the `__iter__()` method works fine, because
`abc.Iterator` helpfully defines `__iter__()` for us, so we can
inherit it.)

> ## Implementing multiple interfaces
>
> You may find yourself wanting to implement multiple interfaces in a
> single class. This is possible by making use of _multiple
> inheritance_, where a class inherits from more than one base
> class. This is not supported in all programming languages, and in
> many programming languages it is considered to be problematic. It is
> more common in Python, but we don't have space to go into detail
> about it in this lesson.
{: .callout}

> ## Hashable `Polygon`s
>
> The hashable protocol allows classes to be used as dictionary keys
> and as members of sets. Look up [the hashable protocol][hashable]
> and adjust the `Polygon` class so that it follows this.
>
> Test this by using a `Triangle` instance as a dict key:
>
> ~~~
> triangle_descriptions = {
>     Triangle([3, 4, 5]): "The basic Pythagorean triangle"
> }
> ~~~
> {: .language-python}
>
>> ## Solution
>>
>> The hashable protocol requires implementing one method,
>> `__hash__()`, which should return a hash of the aspects of the
>> instance that make it unique. Lists can't be hashed, so we also
>> need to turn the list of `side_lengths` into a tuple.
>>
>> ~~~
>>     def __hash__(self):
>>         return hash(tuple(self.side_lengths))
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}


## Composition

Composition is a technique where rather than adding more and more
functionality to a single class (either explicitly, or via
inheritance), functionality is added by adding instances of other
classes that group together the related functionality.

An example of a library that makes heavy use of composition is the
Matplotlib object-oriented API. While Matplotlib makes its `pyplot`
API available for basic plotting, it is built on top of a very
intricate hierarchy of classes and objects. Those who want more
control over their plots are encouraged to use this interface instead
of the simplified `pyplot` version.

To get a feel for how Matplotlib uses composition to separate its
concerns while having a large amount of functionality, we can write a
small test function to recursively walk through a member variables of
an object that are themselves instances of a non-builtin class.

~~~
from matplotlib.pyplot import subplots

def traverse_objects(base_object, level=0, max_level=5):
    """Recursively walk through the member variables of base_object,
    and print out information about each that is an instance of a
    non-built-in class. max_level controls the depth that the
    recursion may continue to, to avoid infinite loops."""

    if hasattr(base_object, '__dict__') and level < max_level:
        for child_name, child_object in vars(base_object).items():
            if child_object.__class__.__module__ != 'builtins':
                print(" " * level, child_name, ':', type(child_object))
                traverse_objects(child_object, level=level+1)


# Create a simple plot
fig, ax = plt.subplots()
ax.scatter([1, 2, 3], [1, 4, 9])
ax.scatter([1, 1.5, 2, 2.5, 3], [1, 1, 2, 3, 5])

# Inspect the object hierarchy of ths figure object
traverse_objects(fig)
~~~
{: .language-python}

This gives a lot of output&mdash;72 lines, so in principle 72
different classes are combining here. In practice this number is not
accurate; there is some duplication in this list, since for example
both `canvas` and `patch` have a `figure` member variable so that they
can refer back to the `Figure` that they work with. Conversely, this
simple traversal ignores some additional composition; for example,
`fig._axstack._elements` is a list of tuples, but within some of those
tuples are more objects of type `matplotlib.gridspec.SubplotSpec` and
`matplotlib.axes._subplots.AxesSubplot`.

This is why when you have errors in your code, tracebacks from some
libraries can be quite long. Having lots of small methods in classes
that are dedicated to one very specific aspect means that it is easier
to reason about what each one is doing in isolation by itself, but can
make it more complicated to get a view of the big picture.

> ## Composing plotters
>
> How could the `FunctionPlotter`, `PolynomialPlotter`, and
> `QuadraticPlotter` be refactored to make use of composition instead
> of inheritance?
>
>> ## Solution
>>
>> One way of doing this is to define a "plottable function"
>> interface. An object respecting this interface would:
>>
>> * be callable
>> * accept one argument
>> * return \\(f(x)\\)
>>
>> Then, with the `FunctionPlotter` as defined previously, there is no
>> need to subclass to create `QuadraticPlotter`s and
>> `PolynomialPlotter`s; instead, we can define a `QuadraticFunction`
>> class as:
>>
>> ~~~
>> class Quadratic:
>>     def __init__(self, a, b, c):
>>         self.a = a
>>         self.b = b
>>         self.c = c
>>
>>     def __call__(self, x):
>>         return self.a * x ** 2 + self.b * x + self.c
>> ~~~
>> {: .language-python}
>>
>> This can then be passed to a `FunctionPlotter`:
>>
>> ~~~
>> plotter = FunctionPlotter()
>> plotter.plot(Quadratic(1, -1, 1))
>> ~~~
>> {: .language-python}
>>
>> Alternatively, we can _encapsulate_ the function to be plotted as
>> part of the class.
>>
>> ~~~
>> from matplotlib.colors import is_color_like
>>
>> class FunctionPlotter:
>>     def __init__(self, function, color='red', linewidth=1, x_min=-10, x_max=10):
>>         assert is_color_like(color)
>>         self.color = color
>>         self.linewidth = linewidth
>>         self.x_min = x_min
>>         self.x_max = x_max
>>         self.function = function
>>
>>     def plot(self):
>>         '''Plot a function of a single argument.
>>         The line is plotted in the colour specified by color, and with width
>>         linewidth.'''
>>         fig, ax = subplots()
>>         x = linspace(self.x_min, self.x_max, 1000)
>>         ax.plot(x, self.function(x), color=self.color, linewidth=self.linewidth)
>>         fig.show()
>> ~~~
>> {: .language-python}
>>
>> This could then be used as:
>>
>> ~~~
>> from numpy import sin
>> sin_plotter = FunctionPlotter(sin)
>> quadratic_plotter = FunctionPlotter(Quadratic(1, -1, 1), color='blue')
>> sin_plotter.plot()
>> quadratic_plotter.plot()
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}

[hashable]: https://docs.python.org/library/collections.abc.html#collections.abc.Hashable
