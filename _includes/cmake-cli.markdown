CMake can be run from the shell by invoking the `cmake` command inside a build directory. You can pass any CMake variable or option with `-DVARIABLE_NAME=VALUE`. You can also pass the generator you want to use (e.g. *Unix Makefiles* or *Visual Studio 8 2005*-project files) with the `-G` parameter (to see all available generators just run cmake without any parameters). The last parameter to the CMake command is the path to the source code directory. A typical call would look like this:

<span class="codeline">$ cmake -DOGS_FEM_MPI=ON -G "Unix Makefiles" ../sources<span></span>Configures the project with one option and generates unix makefiles.</span>

**Important**: Please run CMake at least twice to correctly configure the project. 