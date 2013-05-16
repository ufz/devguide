You can clone the OGS main repository with this git shell command:

<pre class="terminal bootcamp">
	<span class="codeline">$ git clone git://github.com/ufz/ogs.git sources<span>Creates a clone of the main OGS git repository</span></span>
</pre>

This creates a new subdirectory *sources/* in which the OGS source code repository is
cloned.

<div class="more-info">
    <h4 class="compressed">You want to checkout OGS-5 from Subversion?</h4>
    <div class="more-content">
        <p>Before checking out the source code make sure to configure your SVN-client properly: <a href="{% raw %}{{ site.baseurl }}{% endraw %}/configure-svn">Configure Subversion</a></p>
        <p>You can checkout the source directory of the OGS Subversion-Trunk with this shell command:</p>
            <pre class="terminal bootcamp">
                <span class="codeline">$ svn co https://svn.ufz.de/svn/ogs/trunk/sources</span>
            </pre>
        <p>Alternatively you can do the checkout with graphical tools like <a href="http://tortoisesvn.tigris.org/" target="blank">TortoiseSVN</a>.</p>
    </div>
</div>
