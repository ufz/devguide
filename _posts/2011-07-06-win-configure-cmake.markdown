---
layout: default
title: Build configuration with CMake
description: How to configure a build with CMake
---

<p class="intro">This guide will show you how to configure your build configuration on <strong>Windows</strong>. There are also guides for <strong><a href="{% raw %}{{ site.baseurl }}{% endraw %}/linux-configure-cmake">Linux and OSX</a></strong>. It is assumed that you have already <a href="{% raw %}{{ site.baseurl }}{% endraw %}/prerequisites-redirect">set up the prerequisites</a>!</p>

{% include cmake-general.markdown %}

## <span class="step">Option 1:</span> Configure visually with CMake-GUI ##

{% include cmake-gui.markdown %}

## <span class="step">Option 2:</span> Configure from the command line ##

First, you need to open Git Bash (not the Windows command line), found in the start menu in the git-folder.

<img src="{% raw %}{{ site.baseurl }}{% endraw %}/images/bootcamp/bootcamp_1_win_gitbash.jpg" width="558" height="300" alt="Open the terminal" />

{% include git-bash-intro.markdown %}

{% include cmake-cli.markdown %}

----

{% include cmake-gui-note.markdown %}

{% include next-steps-cmake.markdown %}
