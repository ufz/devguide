---
layout: default
title: Profile your code
description:
---

<p class="intro">This guide will show you how to profile your ogs run on <strong>Windows</strong>. There is also a guide for <strong><a href="{% raw %}{{ site.baseurl }}{% endraw %}/linux-profiling">Linux and OSX</a></strong>.</p>

{% include profiling-intro.markdown %}

## Profiling OGS ##

For profiling OGS the profiler included in Visual Studio is used.

To profile your ogs run follow these steps:

- Select *Release* configuration
- Right click on a *Start Up project* in the Solution Explorer and select *Profile Guided Optimization / Instrument*
- After the build finished, click *Profile Guided Optimization / Run Instrumented Optimized Application*
- Find the created files (*.pgc, *.pgd) under the Release directory.
- Open the Visual Studio command prompt and type:
<pre class="terminal bootcamp">
	<span class="codeline">pgomgr /merge (a file name of *.pgc) (a file name of *.pgd)</span>
	<span class="codeline">pgomgr /summary (a file name of *.pgd) > profile_result.txt</span>
</pre>
- Have a look at *profile_result.txt*, it contains a summary of the profiling
