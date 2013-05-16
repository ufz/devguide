---
layout: default
title: Code coverage measurements with gcov/lcov
description:
categories: advanced
---

<p class="intro">This guide will show you how to produce code coverage measurements with gcov/lcov. This is not available on <strong>Windows</strong>!</p>

Code coverage reports tell you which code parts are actually executed and how often each line / function / class is stepped over. This is useful to check if the test examples / unit tests cover the code.

## Requirements

The following tools are very likely to already be installed on Linux / Mac OS X:

- [gcov](http://gcc.gnu.org/onlinedocs/gcc/Gcov.html)
- [lcov](http://ltp.sourceforge.net/coverage/lcov.php)
- [genhtml](http://linux.die.net/man/1/genhtml)
- GCC compiler (for Mac [see here](/mac-prerequisites))

## To get started

- Configure CMake with `OGS_COVERAGE=ON`
- Run a coverage-make-target, to get a list type `make help | grep coverage`
- Following the on-screen instructions open the generated coverage report in a browser:

![](http://d.pr/i/Nl8p+)

## How it works

- The code is compiled with special [coverage compiler flags](https://github.com/ufz/ogs/blob/master/scripts/cmake/cmake/CodeCoverage.cmake#L35)
- In [scripts/cmake/Coverage.cmake](https://github.com/ufz/ogs/blob/master/scripts/cmake/Coverage.cmake) new make-targets are prepared for the executables which should be coverage tested (see the function `SETUP_TARGET_FOR_COVERAGE` for more details)

## CTest

Note that there is also a new make-target for *ctest*: `ctest_coverage`. This runs all CTest-tests which add up on each other so that you get the real test coverage over all tests.
