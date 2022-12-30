---
title: "Writing classes"
teaching: 20
exercises: 25
questions:
- "How are classes written in Python?"
- "What do methods look like?"
- "How can a class customise how its instances are constructed?"
objectives:
- "Write classes from scratch"
- "Write methods for classes"
- "Write custom `__init__` methods"
- "<a href='https://pfur-my.sharepoint.com/:v:/g/personal/teklay_ty_pfur_ru/EZMRiauV6_5Btx0S7pIgdj0B9HvaACRPHsB6kVgg09SPAg?e=HGGBiz' target='_blank'> View Lecture Video</a>"

keypoints:
- "Classes in Python are blocks started with the `class` keyword"
- "Method definitions look like functions, but must take a `self` argument"
- "The `__init__` method is called when instances are constructed"
---

In the previous section, we've seen how objects can have different behaviour, provided by methods, which in turn are provided by the class of an object.

But what if we want to make our own classes and objects?

If we wanted to plot a variety of quadratic functions, with a
consistent set of styles, we could define a class that does this:

~~~
from matplotlib.pyplot import subplots
from numpy import linspace

class QuadraticPlotter:
    color = 'red'
    linewidth = 1

    def plot(self, a, b, c):
        '''Plot the line a * x ** 2 + b * x + c and output to the screen.
        x runs between -10 and 10, with 1000 intermediary points.
        The line is plotted in the colour specified by color, and with width
        linewidth.'''

        fig, ax = subplots()
        x = linspace(-10, 10, 1000)
        ax.plot(x, a * x ** 2 + b * x + c,
                color=self.color, linewidth=self.linewidth)
~~~
{: .language-python}

Similarly to how `def` is used to define a function, the `class` keyword is
used to define a new class. Both functions and variables can be created inside
the class block, and these will be accessible on any objects of the class that are
created.

When functions are defined within a class, they will become methods of instances
of the class. In order for the function to be aware of the object that they need
to refer to, methods are always given the instance as their first argument. By
convention, the first argument of methods is always called `self`, so that the
object can be referred to consistently whenever it is needed.

Note that variables within methods are local to that method. For example, `fig`
and `ax` will be deleted once the method finishes running. To access variables
attached to the object, their names must be prefixed by `self.`.

> ## Other names than `self`
>
> While it is possible to use any variable name for the first argument of a
> method, and Python will not complain, other programmers will. Since one aim
> when programming is to be as clear as possible to others who may read the
> program later, we strongly recommend following the convention of calling
> the first argument to methods `self`.
{: .callout}

> ## Naming classes
>
> Another convention in Python is that class names start with a capital letter,
> and instead of underscores, initial letters of subsequent words are also
> capitalised. This makes it easier to distinguish classes from objects and
> other variables at a glance.
{: .callout}

So far this code hasn't visibly done anything; while we have defined a class,
we have yet to use it. Let's do that now.

~~~
plotter = QuadraticPlotter()
plotter.plot(1, 2, 3)
plotter.plot(1, 0, -1)
~~~
{: .language-python}

Notice that we only supply the arguments `a`, `b`, and `c` to `plotter.plot()`—
Python automatically adds the object to become the `self` parameter.

So far, this hasn't done anything that we couldn't have done with a function
to perform the setup and then do the plot&mdash;perhaps something like:

~~~
def quadratic_plot(a, b, c, color='red', linewidth=1):
    '''Plot the line a * x ** 2 + b * x + c and output to the screen.
    x runs between -10 and 10, with 1000 intermediary points.
    The line is plotted in the colour specified by color, and with width
    linewidth.'''

    fig, ax = subplots()
    x = linspace(-10, 10, 1000)
    ax.plot(x, a * x ** 2 + b * x + c, color=color, linewidth=linewidth)
~~~
{: .language-python}

However, what if we wanted to plot some of the curves in a thick blue line?
With this function, we could set the `color` and `linewidth` on every call,
but that would create a lot of repetition, and hence opportunities for
the code to become inconsistent.

We could also use a `dict` to hold the common options:

~~~
thick_blue = {'color': 'blue', 'linewidth': 5}

quadratic_plot(3, -5, 5)
quadratic_plot(-3, 1, 0, **thick_blue)
quadratic_plot(2, 10, 2)
quadratic_plot(-2, 13, 4, **thick_blue)
~~~
{: .language-python}

> ## `**`
>
> The `**` syntax here tells Python to take the `thick_blue` `dict`, and
> use its keys and values as keywords and keyword arguments. We'll
> look at this operator later in the lesson where we talk about
> decorators.
{: .callout}

Using objects on the other hand gives a neat alternative way of achieving
this result:

~~~
blue_plotter = QuadraticPlotter()
blue_plotter.color = 'blue'
blue_plotter.linewidth = 5

plotter.plot(3, -5, 5)
blue_plotter.plot(-3, 1, 0)
plotter.plot(2, 10, 2)
blue_plotter.plot(-2, 13, 4)
~~~
{: .language-python}

The two objects `plotter` and `blue_plotter` can store the different states
needed to set up the two styles of plot, whilst keeping the plotting
functionlity common, so it doesn't need to be written separately for red and
blue versions. We no longer have to specify the colour every time we
want to plot with a non-default colour&mdash;instead, we can use the
`QuadraticPlotter` instance that has the colour we want set.

If we need to, we can check the values of the variables we defined:

~~~
print("Line width of red plotter is", plotter.linewidth)
print("Line width of blue plotter is", blue_plotter.linewidth)
~~~
{: .language-python}

~~~
Line width of red plotter is 1
Line width of blue plotter is 5
~~~
{: .output}

> ## Mutation revisitied
>
> Note that the classes we create ourselves in this way will produce mutable objects. This means that we can change the values in objects of `plotter.linewidth`, and Python allows us to do that. It doesn't throw an error.
{: .callout}

> ## Zoom in
>
> Currently `QuadraticPlotter` is hardcoded to plot between -10 and 10.
> Try adjusting it so that it can be adjusted in the same way as the `color`
> and `linewidth` can, while keeping the current defaults.
>
> Use the new class to plot the curve with `a = 3, b = 2, c = 1` both between
> -10 and 10, and between -5 and 50. Do this without changing the
> arguments to the `plot` method.
>
>> ## Solution
>>
>> ~~~
>> class QuadraticPlotter:
>>    color = 'red'
>>    linewidth = 1
>>    x_min = -10
>>    x_max = 10
>>
>>    def plot(self, a, b, c):
>>        '''Plot the line a * x ** 2 + b * x + c and output to the screen.
>>        x runs between -10 and 10, with 1000 intermediary points.
>>        The line is plotted in the colour specified by color, and with width
>>        linewidth.'''
>>
>>        fig, ax = subplots()
>>        x = linspace(self.x_min, self.x_max, 1000)
>>        ax.plot(x, a * x ** 2 + b * x + c,
>>                color=self.color, linewidth=self.linewidth)
>>
>> narrow_plot = QuadraticPlotter()
>> wide_plot = QuadraticPlotter()
>> wide_plot.x_min = -5
>> wide_plot.x_max = 50
>>
>> narrow_plot.plot(3, 2, 1)
>> wide_plot.plot(3, 2, 1)
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}


> ## Plots of fits
>
> The following function performs an [Orthogonal Distance Regression][odr]
> fit of some data, and plots the resulting fit line along with the
> data.
>
> ~~~
> from scipy.odr import ODR, Model, RealData
> from matplotlib.pyplot import show
>
> def linear(params, x):
>     return params[0] * x + params[1]
>
>
> def odr_fit(f, x, y, xerr=None, yerr=None, p0=None, num_params=None):
>     if not p0 and not num_params:
>         raise ValueError("p0 or num_params must be specified")
>     if p0 and (num_params is not None):
>         assert len(p0) == num_params
>
>     data_to_fit = RealData(x, y, xerr, yerr)
>     model_to_fit_with = Model(f)
>     if not p0:
>         p0 = tuple(1 for _ in range(num_params))
>
>     odr_analysis = ODR(data_to_fit, model_to_fit_with, p0)
>     odr_analysis.set_job(fit_type=0)
>     return odr_analysis.run()
>
>
> def plot_results(f, fitobj, x, y,
>                  xmin=None, xmax=None, xerr=None, yerr=None, filename=None):
>     fig, ax = subplots()
>     if xmin is None:
>         xmin = min(x)
>     if xmax is None:
>         xmax = max(x)
>
>     x_range = linspace(xmin, xmax, 1000)
>     ax.plot(x_range, f(fitobj.beta, x_range), label='Fit')
>     ax.errorbar(x, y, xerr=xerr, yerr=yerr, fmt='.', label='Data')
>     ax.set_xlabel(r'$x$')
>     ax.set_ylabel(r'$y$')
>     fig.suptitle(f'Data: $A={fitobj.beta[0]:.02}'
>                  f'\\pm{fitobj.cov_beta[0][0]**0.5:.02}, '
>                  f'B={fitobj.beta[1]:.02}\\pm{fitobj.cov_beta[1][1]**0.5:.02}$')
>     ax.legend(loc=0, frameon=False)
>
>     if filename is not None:
>         fig.savefig(filename)
>
>
> x_data = [0, 1, 2, 3, 4, 5]
> y_data = [1, 3, 2, 4, 5, 5]
> x_err = [0.2, 0.1, 0.3, 0.2, 0.5, 0.3]
> y_err = [0.4, 0.4, 0.1, 0.2, 0.1, 0.4]
>
> result = odr_fit(linear, x_data, y_data, x_err, y_err, num_params=2)
> plot_results(linear, result, x_data, y_data, xerr=x_err, yerr=y_err)
> show()
> ~~~
> {: .language-python}
>
> This code has a lot of repeated terms, and would have even more if
> we wanted to set custom formatting each time.
>
> Try rewriting this as a class, turning most function arguments into
> variables attached to the object, and functions into methods. Some
> of these you won't be able to set in the class definition, but will
> need to be set before the functions will work.
>
>> ## Solution
>>
>> ~~~
>> class FitterPlotter:
>>     x_data = None
>>     y_data = None
>>     x_err = None
>>     y_err = None
>>
>>     fit_result = None
>>     fit_form = None
>>     num_fit_params = None
>>
>>     xmin = None
>>     xmax = None
>>
>>     def odr_fit(self, p0=None):
>>         if None in (self.x_data, self.y_data, self.fit_form):
>>             raise ValueError("x_data, y_data, and fit_form must be specified")
>>         if not p0 and not self.num_fit_params:
>>             raise ValueError("p0 or num_fit_params must be specified")
>>         if p0 and (self.num_fit_params is not None):
>>             assert len(p0) == self.num_fit_params
>>
>>         data_to_fit = RealData(self.x_data, self.y_data, self.x_err, self.y_err)
>>         model_to_fit_with = Model(self.fit_form)
>>         if not p0:
>>             p0 = tuple(1 for _ in range(self.num_fit_params))
>>
>>         odr_analysis = ODR(data_to_fit, model_to_fit_with, p0)
>>         odr_analysis.set_job(fit_type=0)
>>         self.fit_result = odr_analysis.run()
>>         return self.fit_result
>>
>>     def plot_results(self, filename=None):
>>         if None in (self.x_data, self.y_data):
>>             raise ValueError("x_data and y_data must be specified")
>>         fig, ax = subplots()
>>         xmin, xmax = self.xmin, self.xmax
>>         if xmin is None:
>>             xmin = min(self.x_data)
>>         if xmax is None:
>>             xmax = max(self.x_data)
>>
>>         if self.fit_result is not None:
>>             x_range = linspace(xmin, xmax, 1000)
>>             ax.plot(x_range, self.fit_form(self.fit_result.beta, x_range),
>>                     label='Fit')
>>             fig.suptitle(f'Data: $A={self.fit_result.beta[0]:.02}'
>>                          f'\\pm{self.fit_result.cov_beta[0][0]**0.5:.02}, '
>>                          f'B={self.fit_result.beta[1]:.02}'
>>                          f'\\pm{self.fit_result.cov_beta[1][1]**0.5:.02}$')
>>
>>         ax.errorbar(self.x_data, self.y_data, xerr=self.x_err, yerr=self.y_err,
>>                     fmt='.', label='Data')
>>         ax.set_xlabel(r'$x$')
>>         ax.set_ylabel(r'$y$')
>>         ax.legend(loc=0, frameon=False)
>>
>>         if filename is not None:
>>             fig.savefig(filename)
>>
>>
>> fitterplotter = FitterPlotter()
>> fitterplotter.x_data = [0, 1, 2, 3, 4, 5]
>> fitterplotter.y_data = [1, 3, 2, 4, 5, 5]
>> fitterplotter.x_err = [0.2, 0.1, 0.3, 0.2, 0.5, 0.3]
>> fitterplotter.y_err = [0.4, 0.4, 0.1, 0.2, 0.1, 0.4]
>> fitterplotter.fit_form = linear
>> fitterplotter.num_fit_params = 2
>>
>> fitterplotter.odr_fit()
>> fitterplotter.plot_results()
>> show()
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}


## Initialising instances

So far we can create an object with the defaults that we set in the class
definition, and then customise it afterwards. But wouldn't it be nice to be
able to create an object with the attributes that we want straight out of the
box?

To do this, we can define an _initialiser_ for the class. When Python creates
an instance of a class, it looks for a method called `__init__`. If it finds
one, then it calls it, giving it all the arguments passed to the class.

For example, for the `QuadraticPlotter`, the variables `color` and `linewidth`
could be passed as arguments to `__init__` and set on initialisation, rather
than being defined as part of the class definition:

~~~
from matplotlib.colors import is_color_like

class QuadraticPlotter:
    def __init__(self, color='red', linewidth=1):
        '''Set the initial attributes of this plotter.'''
        assert is_color_like(color)

        self.color = color
        self.linewidth = linewidth

    def plot(self, a, b, c):
        '''Plot the line a * x ** 2 + b * x + c and output to the screen.
        x runs between x_min and x_max, with 1000 intermediary points.
        The line is plotted in the colour specified by color, and with width
        linewidth.'''

        fig, ax = subplots()
        x = linspace(-10, 10, 1000)
        ax.plot(x, a * x ** 2 + b * x + c,
                color=self.color, linewidth=self.linewidth)

pink_plotter = QuadraticPlotter(color='magenta', linewidth=3)
pink_plotter.plot(0, 1, 0)
~~~
{: .language-python}

This also lets us do some validation that the values we are given are
usable, rather than deferring these errors to a long way down the line.

> ## Pronouncing `__init__`
>
> The method name `__init__` is most often pronounced "dunder init",
> where the "dunder" is short for "double underscore", since the name
> starts and ends with two underscores.
>
> We'll encounter more methods with "dunder" in the name in a later episode.
{: .callout}

> ## Zoom in again
>
> Try rewriting the "Zoom in" example above to set the bounds of the plot,
> as well as the `color` and `linewidth`, using arguments to the constructor.
>
>> ## Solution
>>
>> ~~~
>> class QuadraticPlotter:
>>     def __init__(self, color='red', linewidth=1, x_min=-10, x_max=10):
>>         '''Set the initial attributes of this plotter.'''
>>         assert is_color_like(color)
>>         self.color = color
>>         self.linewidth = linewidth
>>         self.x_min = x_min
>>         self.x_max = x_max
>>
>>    def plot(self, a, b, c):
>>        '''Plot the line a * x ** 2 + b * x + c and output to the screen.
>>        x runs between x_min and x_max, with 1000 intermediary points.
>>        The line is plotted in the colour specified by color, and with width
>>        linewidth.'''
>>
>>        fig, ax = subplots()
>>        x = linspace(self.x_min, self.x_max, 1000)
>>        ax.plot(x, a * x ** 2 + b * x + c,
>>                color=self.color, linewidth=self.linewidth)
>>
>> narrow_plot = QuadraticPlotter()
>> wide_plot = QuadraticPlotter(x_min=-5, x_max=50)
>>
>> narrow_plot.plot(3, 2, 1)
>> wide_plot.plot(3, 2, 1)
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}

> ## Initialising fitting
>
> Adjust your solution to the _Plots of fits_ challenge above so that
> it has an initialiser which checks that the needed parameters are
> given before initialising the object.
>
>> ## Solution
>>
>> ~~~
>> class FitterPlotter:
>>     fit_result = None
>>
>>     def __init__(self, x_data, y_data, x_err=None, y_err=None,
>>                  fit_form=None, num_fit_params=None, xmin=None, xmax=None):
>>         self.x_data = x_data
>>         self.y_data = y_data
>>         self.x_err = x_err
>>         self.y_err = y_err
>>         self.fit_form = fit_form
>>         self.num_fit_params = num_fit_params
>>         self.xmin = xmin
>>         self.xmax = xmax
>>
>>     def odr_fit(self, p0=None):
>>         if self.fit_form is None:
>>             raise ValueError("fit_form must be specified")
>>         if not p0 and not self.num_fit_params:
>>             raise ValueError("p0 or num_fit_params must be specified")
>>         if p0 and (self.num_fit_params is not None):
>>             assert len(p0) == self.num_fit_params
>>
>>         data_to_fit = RealData(self.x_data, self.y_data, self.x_err, self.y_err)
>>         model_to_fit_with = Model(self.fit_form)
>>         if not p0:
>>             p0 = tuple(1 for _ in range(self.num_fit_params))
>>
>>         odr_analysis = ODR(data_to_fit, model_to_fit_with, p0)
>>         odr_analysis.set_job(fit_type=0)
>>         self.fit_result = odr_analysis.run()
>>         return self.fit_result
>>
>>     def plot_results(self, filename=None):
>>         fig, ax = subplots()
>>         xmin, xmax = self.xmin, self.xmax
>>         if xmin is None:
>>             xmin = min(self.x_data)
>>         if xmax is None:
>>             xmax = max(self.x_data)
>>
>>         if self.fit_result is not None:
>>             x_range = linspace(xmin, xmax, 1000)
>>             ax.plot(x_range, self.fit_form(self.fit_result.beta, x_range),
>>                     label='Fit')
>>             fig.suptitle(f'Data: $A={self.fit_result.beta[0]:.02}'
>>                          f'\\pm{self.fit_result.cov_beta[0][0]**0.5:.02}, '
>>                          f'B={self.fit_result.beta[1]:.02}'
>>                          f'\\pm{self.fit_result.cov_beta[1][1]**0.5:.02}$')
>>
>>         ax.errorbar(self.x_data, self.y_data, xerr=self.x_err, yerr=self.y_err,
>>                     fmt='.', label='Data')
>>         ax.set_xlabel(r'$x$')
>>         ax.set_ylabel(r'$y$')
>>         ax.legend(loc=0, frameon=False)
>>
>>         if filename is not None:
>>             fig.savefig(filename)
>>
>>
>> fitterplotter = FitterPlotter(
>>     x_data=[0, 1, 2, 3, 4, 5],
>>     y_data=[1, 3, 2, 4, 5, 5],
>>     x_err=[0.2, 0.1, 0.3, 0.2, 0.5, 0.3],
>>     y_err=[0.4, 0.4, 0.1, 0.2, 0.1, 0.4],
>>     fit_form=linear,
>>     num_fit_params=2
>> )
>>
>> fitterplotter.odr_fit()
>> fitterplotter.plot_results()
>> show()
>> ~~~
>> {: .language-python}
> {: .solution}
{: .challenge}

{% include links.md %}

[odr]: https://docs.scipy.org/doc/scipy/reference/odr.html
