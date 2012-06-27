---
layout: default
title: Set Up Prerequisites
description: A quick guide to help you to install the prerequisites
---

<p class="intro">This guide will show you how to install and setup all prerequisites in <strong>Windows</strong>. There are also guides for <strong><a href="{{site.baseurl}}/linux-prerequisites">Linux</a></strong> and <strong><a href="{{site.baseurl}}/mac-prerequisites">OSX</a></strong>. It is assumed that you have already <a href="https://help.github.com/articles/set-up-git">set up Git</a>!</p>

{% include prerequisites-general.markdown %}

Furthermore you need:

- a bash environment (is included in the Git installation)
- wget (if you want to use the automatic setup script)

## <span class="step">Second:</span> Install CMake ##

1. <span class="step-title">Download the installer</span>

	At the [CMake download page](http://www.cmake.org/cmake/resources/software.html)
	choose the **Windows (Win32 Installer)**.

2. <span class="step-title">Execute the installer</span>

	On installing please check the *Add CMake to the system path for ...*:

	<img src="{{site.baseurl}}/images/cmake-win-install.png" width="511" height="396" alt="Check path option" />

## <span class="step">Third:</span> Install Visual Studio ##

Install Microsoft Visual Studio. All versions from 2005 on should work (also
the freely available [C++ Express editions](http://www.microsoft.com/germany/express/)).
On installation you can uncheck all options belonging to other programming
languages than C++.

## <span class="step">Fourth:</span> Checkout the source code ##

On Windows it is necessary to checkout the source code in a directory which contains ***no spaces*** or other Windows specific file system characters! So
on the git bash change the current directory to C:/ogs for example:

<pre class="terminal bootcamp">
	<span class="codeline">$ cd /c/ogs<span>Changes the current working directory to C:/ogs</span></span>
</pre>

{% include checkout-general.markdown %}

## <span class="step">Optional:</span> Install required libraries automatically (needed for Data Explorer) ##

On the git shell go to the OGS *sources/scripts/setup/*-directory and run the setup
script:

<pre class="terminal bootcamp">
	<span class="codeline">$ cd sources/scripts/setup<span>Change current directory to the script directory</span></span>
	<span class="codeline">$ ./setup.sh -a [x32|x64]<span>Run the setup script and pass your architecture: choose either x32 or x64</span></span>
</pre>

See [the scripts source code](https://github.com/ufz/ogs/tree/master/scripts/setup) for more informations.

Afterwards [create some environment variables](http://www.itechtalk.com/thread3595.html) for qt:

- Set `QTDIR` variable to `Path_to_your_Libs_directory\qt`
- Add `%QTDIR%\bin` to your `PATH`-variable:

## <span class="step">Optional:</span> Install optional libraries and tools ##

{% include adv-tools-links.markdown %}

{% include next-steps-prereqs.markdown %}