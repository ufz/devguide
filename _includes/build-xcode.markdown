## Build with Xcode ##

To let CMake generate the Xcode project files change the generator argument to the [CMake run][cmake]:

{% highlight bash %}
$ cmake [your configuration options] -G Xcode ../sources
{% endhighlight %}

Then load the generated project file by either clicking the *OGS.xcodeproj* or via

{% highlight bash %}
$ open OGS.xcodeproj
{% endhighlight %}

In Xcode choose *ogs* or *ogs-gui* from the drop-down menu on the top right and then hit the *Run*-button.

### Use Xcode's clang compiler ###

You can also use the [Clang compiler](http://clang.llvm.org/features.html) compiler from Xcode to speed up compilation times significantly (OGS_FEM configuration with gcc on a Dual-Core Mac takes about 120 seconds whereas the Clang compilation finishes in 45 seconds.) or to get better compiler warning and error messages. Add those options to the CMake run:

{% highlight bash %}
-DCMAKE_C_COMPILER=/usr/bin/clang -DCMAKE_CXX_COMPILER=/usr/bin/clang++
{% endhighlight %}

Afterwards select **LLVM compiler 2.0** in Xcodes build settings.
