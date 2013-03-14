CMake can be run from the shell by invoking the `cmake` command inside a build directory. You can pass any CMake variable or option with `-DVARIABLE_NAME=VALUE` (note the **-D** in front!). You can also pass the generator you want to use (e.g. *Unix Makefiles* or *Visual Studio 10 Win64*-project files) with the `-G` parameter (to see all available generators just run cmake without any parameters), although in most cases the appropriate generator will be chosen automatically. The last parameter to the CMake command is the path to the source code directory. A typical call would look like this:

<pre class="terminal bootcamp">
	<span class="codeline">$ cmake ../sources<span>Configures the project with one option and generates unix makefiles.</span></span>
</pre>

**Important**: Please run CMake at least twice to correctly configure the project. 