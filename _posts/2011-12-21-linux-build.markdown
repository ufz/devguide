---
layout: default
title: Build the project with Make or Eclipse
description:
---

<p class="intro">This guide will show you how to build the project on <strong>Linux</strong>. There are also guides for <strong><a href="{{site.baseurl}}/win-build">Windows</a> and <a href="{{site.baseurl}}/mac-build">OSX</a></strong>.</p>

{% include make.markdown %}

## <span class="step">Option 2:</span> Build with Eclipse ##

To let CMake generate the Eclipse project files change the generator argument to the [CMake run][cmake]:

        cmake [your configuration options] -G"Eclipse CDT4 - Unix Makefiles" ../sources

Or with ccmake

        ccmake -G"Eclipse CDT4 - Unix Makefiles" ../sources

Start the Eclipse ide. From the menu choose *File / Import*. In the import dialog choose *General / Existing projects into workspace* and click *Next*. In *Select root directory* select your build directory and make sure that *Copy project into workspace* is unchecked. Click Finish.
