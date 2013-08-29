---
layout: default
title: Set Up Prerequisites
description: A quick guide to help you to install the prerequisites
---

This guide will show you how to install and setup all prerequisites on <strong>Mac OS X</strong>. There are also guides for <strong><a href="/linux-prerequisites">Linux</a></strong> and <strong><a href="/win-prerequisites">Windows</a></strong>. It is assumed that you have already <a href="https://help.github.com/articles/set-up-git">set up Git</a>!

{% include prerequisites-general.markdown %}

# Step by step

## Install Git and set up GitHub ##

Because Git and Github are more complex topics its installation and setup is
described on the [GitHub help pages](https://help.github.com/articles/set-up-git).
Please follow the steps on the help pages and come back afterwards.

You can also install the [graphical GitHub client](http://mac.github.com/) which is nice to use.

## Install Xcode ##

Install Xcode 4 through the Mac App Store (Mac OS X 10.6.x and higher) or install Xcode's [command line tools](https://developer.apple.com/downloads).

## Install Homebrew ##

[Homebrew][homebrew] is a package manager for Mac OS X and should be used to install all necessary libraries and tools. To install run the following on the Terminal:

{% highlight bash %}
$ ruby -e "$(curl -fsSL https://raw.github.com/mxcl/homebrew/go)"
{% endhighlight %}

You can now use the `homebrew` command to search, install or deinstall libraries.

## Install GCC, CMake, Boost##

As of Xcode 4.2 clang (LLVM) is the default compiler and gcc is no longer distributed with Xcode. You have to use gcc which you can install via [Homebrew][homebrew]:

{% highlight bash %}
$ brew tap homebrew/versions
$ brew install gcc49 --enable-cxx
{% endhighlight %}

You may want to set this as your default C/C++ compiler in your *.bashrc*:

{% highlight bash %}
export CC=/usr/local/bin/gcc-4.9
export CXX=/usr/local/bin/g++-4.9
{% endhighlight %}

Then also install CMake and Boost:

{% highlight bash %}
$ brew install cmake boost
{% endhighlight %}

Boost is optional but recommended for faster compilation.

## Checkout the source code ##

{% include checkout-general.markdown %}

## Install libraries needed for the Data Explorer (Optional) ##

This installs Qt, Vtk, shapelib and geotiff:

{% highlight bash %}
$ brew install qt shapefile libgeotiff vtk --qt
{% endhighlight %}

## Install optional libraries and tools (Optional)##

{% include adv-tools-links.markdown %}

{% highlight bash %}
$ brew install gtest open-sg cppcheck doxygen netcdf uncrustify
{% endhighlight %}

{% include next-steps-prereqs.markdown %}

[homebrew]: http://mxcl.github.com/homebrew/
