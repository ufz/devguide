---
layout: default
title: Profile your code
description:
---

<p class="intro">This guide will show you how to profile your ogs run on <strong>Linux and OSX</strong>. There is also a guide for <strong><a href="/win-profiling">Windows</a></strong>.</p>

{% include profiling-intro.markdown %}

## Profiling OGS ##

For profiling OGS [gprof](http://www.cs.utah.edu/dept/old/texinfo/as/gprof_toc.html) is used. Also have a look at [this grpf tutorial](http://linux.about.com/library/cmd/blcmdl1_gprof.htm). The graphs are generated with the [gprof2dot](http://code.google.com/p/jrfonseca/wiki/Gprof2Dot) python script.

To profile an OGS run you have to configure with the `-DOGS_PROFILE=ON` CMake-option. This adds the `-pg` compiler option. While the program is running a file with the name *gmon.out* is created. Make also sure to configure with the optimized release option (`-DCMAKE_BUILD_TYPE=Release`).

## Generate nice graphs ##

![gprof2dot generated graph](/images/profiling.png)

### Prerequisites ###

- Python
- [dot](http://www.graphviz.org/)-tool

### Usage ###

You have to gprof with ogs executable as an argument. The you need to pipe the output to the gprof2dot-script and then you need to pipe the scripts output to the dot tool. The next listing shows the entire setup:

<pre class="terminal bootcamp">
	<span class="codeline">$ cd build<span>Go to your build directory</span></span>
	<span class="codeline">$ cmake [path to source-directory] [other cmake options] -DOGS_PROFILE=ON -DCMAKE_BUILD_TYPE=Release<span>Configure your build as explained above</span></span>
	<span class="codeline">$ ./bin/ogs [path to the benchmark]<span>run ogs, this creates the gmon.out-file in the build-directory</span></span>
	<span class="codeline">$ gprof ./bin/ogs | [path to source-directory]/scripts/gprof2dot.py -s | dot -Tpng -o output.png<span>this creates the graph as a png-file</span></span>
</pre>
