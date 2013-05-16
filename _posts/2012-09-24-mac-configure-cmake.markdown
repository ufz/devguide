---
layout: default
title: Build configuration with CMake
description: How to configure a build with CMake
---

<p class="intro">This guide will show you how to configure your build configuration on <strong>Mac OS X</strong>. There are also a guides for <strong><a href="{% raw %}{{ site.baseurl }}{% endraw %}/win-configure-cmake">Windows</a></strong> and <strong><a href="{% raw %}{{ site.baseurl }}{% endraw %}/linux-configure-cmake">Linux</a></strong>. It is assumed that you have already <a href="{% raw %}{{ site.baseurl }}{% endraw %}/prerequisites-redirect">set up the prerequisites</a>!</p>

{% include cmake-general.markdown %}

## <span class="step">Option 1:</span> Configure visually with the ccmake tool ##

{% include ccmake.markdown %}

## <span class="step">Option 2:</span> Configure from the command line ##

{% include cmake-cli.markdown %}

----

{% include cmake-gui-note.markdown %}

## <span class="step">Optional:</span> Configure to use GCC compiler ##

If you like to use the GCC compiler and you have it [already installed]({% raw %}{{ site.baseurl }}{% endraw %}/mac-prerequisites) you have to tell it CMake:

<pre class="terminal bootcamp">
    <span class="codeline">$ cmake -DCMAKE_C_COMPILER=/usr/local/bin/gcc-4.5 -DCMAKE_CXX_COMPILER=/usr/local/bin/g++-4.5</span>
</pre>

{% include next-steps-cmake.markdown %}
