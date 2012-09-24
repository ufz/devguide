---
layout: default
title: Build configuration with CMake
description: How to configure a build with CMake
---

<p class="intro">This guide will show you how to configure your build configuration on <strong>Linux</strong>. There are also a guides for <strong><a href="{{site.baseurl}}/win-configure-cmake">Windows</a></strong> and <strong><a href="{{site.baseurl}}/mac-configure-cmake">Mac OS X</a></strong>. It is assumed that you have already <a href="{{site.baseurl}}/prerequisites-redirect">set up the prerequisites</a>!</p>

{% include cmake-general.markdown %}

## <span class="step">Option 1:</span> Configure visually with the ccmake tool ##

{% include ccmake.markdown %}

## <span class="step">Option 2:</span> Configure from the command line ##

{% include cmake-cli.markdown %}

----

{% include cmake-gui-note.markdown %}

{% include next-steps-cmake.markdown %}