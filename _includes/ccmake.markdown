A better way of running cmake on the command line is to use the `ccmake` tool. This is a shell tool but with some graphical user interface. To use it just run `ccmake` inside your build directory with the generator you want to use the and also path to the source code as parameters:

<pre class="terminal bootcamp">
	<span class="codeline">$ ccmake -G "Unix Makefiles" ../sources <span>Runs ccmake</span></span>
</pre>

First press the *C*-key for *Configure*. You are now presented the available configuration options. You can navigate in the list with the cursor keys and toggle / alter options with the *Enter*-key. You may also press the *T*-key to toggle (previously hidden) advanced options. Press the *C*-key again and again until the *Generate*-option becomes visible. Press the *G*-key to generate the project files and exit ccmake.