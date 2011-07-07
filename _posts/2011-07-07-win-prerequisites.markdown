---
layout: default
title: Build configuration with CMake
description: How to configure a build with CMake
---

<p class="intro">This guide will show you how to install and setup all prerequisites in <strong>Windows</strong>. There are also guides for <strong><a href="/help/linux-prerequisites">Linux</a></strong> and <strong><a href="/help/mac-prerequisites">OSX</a></strong>.</p>

{% include prerequisites-general.markdown %}

## <span class="step">Second:</span> Install CMake ##

1. <span class="step-title">Download the installer</span>

	At the [CMake download page](http://www.cmake.org/cmake/resources/software.html)
	choose the **Windows (Win32 Installer)**.

2. <span class="step-title">Execute the installer</span>

	On installing please check the *Add CMake to the system path for ...*:

	<img src="/devguide/images/cmake-win-install.png" width="511" height="396" alt="Check path option" />

## <span class="step">Third:</span> Install Visual Studio ##

Install Microsoft Visual Studio. All versions from 2005 on should work (also
the freely available [C++ Express editions](http://www.microsoft.com/germany/express/)).
On installation you can uncheck all options belonging to other programming
  languages than C++.
  
## <span class="step">Fourth:</span> Install wget for Windows ##

1. <span class="step-title">Create bin-directory</span>

	On the Git Bash in your Home-directory (`~/`):

	<pre class="terminal bootcamp">
		<span class="bash-output"><em>username</em>@<em>computername</em> ~</span>
		<span class="codeline">$ mkdir bin<span></span>Creates the bin-directory</span>
	</pre>

2. <span class="step-title">Download wget</span>

	Download wget [here](https://github.com/downloads/ufz/devguide/wget.exe) and
	place the executable in the created bin-directory which is located inside
	your user-directory.

## <span class="step">Optional:</span> Install Qt (needed for DataExplorer) ##

Please follow the steps in the official Qt documentation [installation guide](http://doc.qt.nokia.com/latest/install-win.html) and come back afterwards.

## <span class="step">Optional:</span> Install VTK (needed for DataExplorer) ##

