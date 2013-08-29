## Build with Make ##

To build with the *make* tool on the shell go to your [previously created][cmake] build directory and type `make`:

{% highlight bash %}
$ cd build
$ make
{% endhighlight %}

To speedup the compilation process append the number of cores of your cpu to the make command. E.g. for 8 cores:

{% highlight bash %}
$ make -j 8
{% endhighlight %}
