## <span class="step">Option 1:</span> Build with Make ##

To build with the *make* tool on the shell go to your [previously created][cmake] build directory and type `make`:

        cd build
        make

To speedup the compilation process append the number of cores of your cpu to the make command. E.g. for 8 cores:

        make -j 8



[cmake]: {% raw %}{{ site.baseurl }}{% endraw %}/linux-configure-cmake
