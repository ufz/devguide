##<span class="step">Overview:</span> CMake ##

For configuring a build the open source [CMake](http://www.cmake.org) tool is used. *CMakeLists.txt* files replace traditional Makefiles or IDE project files. First a build-directory is needed. This can be placed arbitrary. The CMake tool is run inside this build-directory with a reference to the source code-directory of the project and user-chosen options. CMake then generates either Makefiles or project files for IDE such as Visual Studio or Eclipse inside the build directory. Also all the compiled files will be generated in this directory. This leaves the actual source code clean from intermediate files which are generated from the source code. Nothing inside the build directory will ever be version controlled because its contents can be regenerated at every time from the source code.

Because of the separation of the source code and all stuff that is generated as a part of the build process it is no problem to have several build configurations (e.g. a serial configuration and a parallelized MPI-enabled configuration) all referring to the same source code.

When you want to start over with a new configuration simply delete the build-directory, create a new one and reconfigure.

For a list of available options see the [CMake configuration options]({% raw %}{{ site.baseurl }}{% endraw %}/configure-cmake-options) page.
