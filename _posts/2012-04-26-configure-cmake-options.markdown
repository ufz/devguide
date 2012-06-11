---
layout: default
title: CMake configuration options
description: Description of CMake configuration options
categories: beginner
---

## General ##

- `OGS_DONT_USE_QT` - Disables all Qt specific code

## Debugging ##

- `CMAKE_BUILD_TYPE` - Defaults to `Debug` which builds with debugging infos
- `OGS_PROFILE` - Builds with profiling flags (`-pg`)
- `OGS_CMAKE_DEBUG` - Prints out the values of all defined CMake variables at CMake configuration time.

## Optimization ##

- `CMAKE_BUILD_TYPE` - Set to `Release` to build with optimization flags

## Documentation ##

Source code documentation is generated with [Doxygen](http://www.stack.nl/~dimitri/doxygen). If Doxygen is found a new make target `doc` is created. Simply build that target and the documentation is generated in the *docs*-subfolder of the build directory.

- `DOCS_GENERATE_DIAGRAMS` - Use the DOT tool to generate class diagrams
- `DOCS_GENERATE_CALL_GRAPHS` - Generate call dependency graphs
- `DOCS_GENERATE_COLLABORATION_GRAPHS` - Generate collaboration graphs

*These options all depend on the [DOT](http://www.graphviz.org/) tool.*