---
layout: default
title: Set Up Prerequisites
description: A quick guide to help you to install the prerequisites
---

<p class="intro">This guide will show you how to install and setup all prerequisites on <strong>Linux</strong> (Ubuntu). There are also guides for <strong><a href="{{site.baseurl}}/mac-prerequisites">Mac OS X</a></strong> and <strong><a href="{{site.baseurl}}/win-prerequisites">Windows</a></strong>.</p>

{% include prerequisites-general.markdown %}

## <span class="step">Second:</span> Install required packages ##

For the OGS command line only a compiler and CMake is needed. Install both with:

<pre class="terminal bootcamp">
    <span class="codeline">$ sudo apt-get install build-essential cmake cmake-curses-gui<span>This installs CMake and its curses gui (ccmake)</span></span>
</pre>

## <span class="step">Optional:</span> Install libraries needed for the Data Explorer ##

This installs Qt, Vtk, shapelib and geotiff:

<pre class="terminal bootcamp">
    <span class="codeline">$ sudo apt-get install qt4-dev-tools libvtk5-dev libvtk5-qt4-dev libnetcdf-dev libshp-dev libgeotiff-dev<span>This installs the libraries through the package manager</span></span>
</pre>

## <span class="step">Optional:</span> Install optional libraries and tools ##

{% include adv-tools-links.markdown %}

<pre class="terminal bootcamp">
    <span class="codeline">$ sudo apt-get install libgtest-dev cppcheck doxygen uncrustify<span>This installs libraries through the package manager</span></span>
</pre>

