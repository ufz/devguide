---
layout: default
title: CMake configuration options
description: Description of CMake configuration options
categories: beginner
---

Some of these options are enabled by default ("*Defaults* to *ON*") otherwise they must be expicitly set to *ON*.

## General ##

CMake switches to enable / disable parts of OGS.

- `OGS_BUILD_CLI` - Builds the simulator. *Defaults* to *ON*.
- `OGS_BUILD_GUI` - Builds the [Data Explorer](https://svn.ufz.de/ogs/attachment/wiki/WikiStart/DataExplorer-Manual.pdf?format=raw)
- `OGS_BUILD_TESTS` - Builds the test executables. *Defaults to *ON*.
- `OGS_DONT_USE_QT` - Disables all Qt specific code
- `OGS_NO_EXTERNAL_LIBS` - Disables any external dependencies
- `OGS_LIBS_DIR` - Search path for compiled third-party libraries such as *Geotiff* or *shapelib* (mainly used on Windows)

## Debugging ##

- `CMAKE_BUILD_TYPE` - Defaults to `Debug` which builds with debugging infos
- `OGS_PROFILE` - Builds with profiling flags (`-pg`)
- `OGS_CMAKE_DEBUG` - Prints out the values of all defined CMake variables at CMake configuration time
- `OGS_BUILD_INFO` - Informations on the build such as Git commit info, platform, build date and compiler options are embedded into the executables. *Defaults* to *ON*.

## Optimization ##

- `CMAKE_BUILD_TYPE` - Set to `Release` to build with optimization flags

## Logging ##

- `OGS_DISABLE_LOGGING` - Disables all logog output messages. This really strips out all logog-code (useful for performance testing).

## Testing ##

- `OGS_COVERAGE` - Enables code coverage measurements with gcov/lcov. [More ...][{{site.baseurl}}/linux-coverage]

## Documentation ##

Source code documentation is generated with [Doxygen](http://www.stack.nl/~dimitri/doxygen). If Doxygen is found a new make target `doc` is created. Simply build that target and the documentation is generated in the *docs*-subfolder of the build directory.

- `DOCS_GENERATE_DIAGRAMS` - Use the DOT tool to generate class diagrams
- `DOCS_GENERATE_CALL_GRAPHS` - Generate call dependency graphs
- `DOCS_GENERATE_COLLABORATION_GRAPHS` - Generate collaboration graphs

    *These options all depend on the [DOT](http://www.graphviz.org/) tool.*

- `DOCS_GENERATE_DOCSET` - Generate [Apple documentation sets](http://gentlebytes.com/appledoc-docs-examples-basic/), e.g. for use with [Dash](http://kapeli.com/dash/) (*Mac only*)