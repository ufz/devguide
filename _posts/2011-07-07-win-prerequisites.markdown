---
layout: default
title: Set Up Prerequisites
description: A quick guide to help you to install the prerequisites
---

This guide will show you how to install and setup all prerequisites in **Windows**. There are also guides for **[Linux](/linux-prerequisites)** and **[Mac OS X](/mac-prerequisites)**. It is assumed that you have already <a href="https://help.github.com/articles/set-up-git">set up Git</a>!

{% include prerequisites-general.markdown %}

## Install Git and set up GitHub ##

Simply install the [graphical GitHub client](http://windows.github.com/) and log into it with your GitHub account credentials.

## Install CMake ##

- At the [CMake download page](http://www.cmake.org/cmake/resources/software.html) choose the **Windows (Win32 Installer)**
- Execute the installer: on installing please check the *Add CMake to the system path for ...*:

![Check path option](/images/cmake-win-install.png)

## Install Visual Studio ##

Install Microsoft Visual Studio. All versions from 2012 on should work (also
the freely available [Visual Studio 2012 Express for Windows Desktop](http://www.microsoft.com/visualstudio/eng/downloads#d-express-windows-desktop)). On installation you can uncheck all options belonging to other programming
languages than C++. Make sure to also install the latest update for your Visual Studio version (e.g. [Visual Studio 2012 Update 3](http://www.microsoft.com/en-us/download/details.aspx?id=39305)).

## Install Boost (Optional) ##

This step is optional but recommended for faster compilation times. Download the [Boost source code](http://sourceforge.net/projects/boost/files/boost/1.54.0/boost_1_54_0.zip/download) and unzip it. Best location for unzipping is `C:\boost` because in this case Boost gets automatically found by CMake.

Then in a Visual Studio Command Line run the following inside the Boost directory:

{% highlight bat %}
bootstrap.bat
b2 toolset=msvc-11.0 --build-type=complete architecture=x86 address-model=64
{% endhighlight %}

**Note:** If you have unzipped Boost in another location than `C:\boost` then you should add a Windows environemnt variable for it so that CMake can find it. The variable is named `BOOST_ROOT` and should be set to the directory where you unzipped Boost.

## Checkout the source code ##

{% include checkout-general.markdown %}

{% include next-steps-prereqs.markdown %}
