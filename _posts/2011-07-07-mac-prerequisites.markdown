---
layout: default
title: Set Up Prerequisites
description: A quick guide to help you to install the prerequisites
---

<p class="intro">This guide will show you how to install and setup all prerequisites on <strong>Mac OS X</strong>. There are also guides for <strong><a href="/linux-prerequisites">Linux</a></strong> and <strong><a href="/win-prerequisites">Windows</a></strong>. It is assumed that you have already <a href="https://help.github.com/articles/set-up-git">set up Git</a>!</p>

{% include prerequisites-general.markdown %}

## <span class="step">First:</span> Install Git and set up GitHub ##

Because Git and Github are more complex topics its installation and setup is
described on the [GitHub help pages](https://help.github.com/articles/set-up-git).
Please follow the steps on the help pages and come back afterwards.

You can also install the [graphical GitHub client](http://mac.github.com/) which is nice to use.

## <span class="step">Second:</span> Install Xcode ##

Install Xcode 4 through the Mac App Store (Mac OS X 10.6.x and higher) or [Xcode 3](http://connect.apple.com/cgi-bin/WebObjects/MemberSite.woa/wo/5.1.17.2.1.3.3.1.0.1.1.0.3.1.3.3.1) (you need an apple developer login).

## <span class="step">Third:</span> Install Homebrew ##

[Homebrew][homebrew] is a package manager for Mac OS X and should be used to install all necessary libraries and tools. To install run the following on the Terminal:

<pre class="terminal bootcamp">
	<span class="codeline">$ /usr/bin/ruby -e "$(curl -fsSL https://raw.github.com/gist/323731)"<span>This installs Homebrew</span></span>
</pre>

You can now use the `homebrew` command to search, install or deinstall libraries.

## <span class="step">Fourth:</span> Install GCC, CMake ##

As of Xcode 4.2 clang (LLVM) is the default compiler and gcc is no longer distributed with Xcode. You have to use gcc which you can install via [Homebrew][homebrew]:

<pre class="terminal bootcamp">
	<span class="codeline">$ brew tap homebrew/dupes</span>
	<span class="codeline">$ brew install gcc --enable-cxx<span>This installs gcc 4.7.2 with C++ enabled</span></span>
</pre>

You may want to set this as your default C/C++ compiler in your *.bashrc*:

    export CC=/usr/local/bin/gcc-4.7
    export CXX=/usr/local/bin/g++-4.7

Then also install CMake:

<pre class="terminal bootcamp">
	<span class="codeline">$ brew install cmake<span>This installs CMake through the Homebrew package manager</span></span>
</pre>

## <span class="step">Fourth:</span> Checkout the source code ##

{% include checkout-general.markdown %}

## <span class="step">Optional:</span> Install libraries needed for the Data Explorer ##

This installs Qt, Vtk, shapelib and geotiff:

<pre class="terminal bootcamp">
	<span class="codeline">$ brew install qt shapefile libgeotiff vtk --qt<span>This installs libraries through the Homebrew package manager</span></span>
</pre>

## <span class="step">Optional:</span> Install optional libraries and tools ##

{% include adv-tools-links.markdown %}

<pre class="terminal bootcamp">
	<span class="codeline">$ brew install gtest open-sg cppcheck doxygen netcdf uncrustify<span>This installs libraries through the Homebrew package manager</span></span>
</pre>

{% include next-steps-prereqs.markdown %}

[homebrew]: http://mxcl.github.com/homebrew/
