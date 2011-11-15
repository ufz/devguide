---
layout: default
title: Set Up Prerequisites
description: A quick guide to help you to install the prerequisites
---

<p class="intro">This guide will show you how to install and setup all prerequisites on <strong>Mac OS X</strong>. There are also guides for <strong><a href="/devguide/linux-prerequisites">Linux</a></strong> and <strong><a href="/devguide/win-prerequisites">Windows</a></strong>.</p>

{% include prerequisites-general.markdown %}

## <span class="step">Second:</span> Install Xcode ##

Install Xcode 4 through the Mac App Store (Mac OS X 10.6.x and higher) or [Xcode 3](http://connect.apple.com/cgi-bin/WebObjects/MemberSite.woa/wo/5.1.17.2.1.3.3.1.0.1.1.0.3.1.3.3.1) (you need an apple developer login).

## <span class="step">Third:</span> Install Homebrew ##

[Homebrew](http://mxcl.github.com/homebrew/) is a package manager for Mac OS X and should be used to install all necessary libraries and tools. To install run the following on the Terminal:

<pre class="terminal bootcamp">
	<span class="codeline">$ /usr/bin/ruby -e "$(curl -fsSL https://raw.github.com/gist/323731)"<span>This installs Homebrew</span></span>
</pre>

You can now use the `homebrew` command to search, install or deinstall libraries.

## <span class="step">Fourth:</span> Install CMake ##

<pre class="terminal bootcamp">
	<span class="codeline">$ brew install cmake<span>This installs CMake through the Homebrew package manager</span></span>
</pre>

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

