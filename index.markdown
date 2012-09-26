---
layout: default
title: Welcome to the OpenGeoSys developer guide
---

<div class="bootcamp-help">
  <h1>OGS developer guide <span>New to OGS development? This will get you started.</span>
  </h1>
  <div class="bootcamp-body">
  <ul>
    <li class="setup">
      <a href="https://help.github.com/articles/set-up-git">
        <div class="image">&nbsp;</div>
        <div class="desc">
          <h2>Setup Git</h2>
        </div>
      </a>
    </li>
    <li class="fork-a-repo">
      <a href="{{site.baseurl}}/prerequisites-redirect">
        <div class="image">&nbsp;</div>
        <div class="desc">
          <h2>Prerequisites</h2>
        </div>
      </a>
    </li>
    <li class="create-a-repo">
      <a href="{{site.baseurl}}/configure-cmake-redirect">
        <div class="image">&nbsp;</div>
        <div class="desc">
          <h2>Configure</h2>
        </div>
      </a>
    </li>
    <li class="be-social">
      <a href="{{site.baseurl}}/build-redirect">
        <div class="image">&nbsp;</div>
        <div class="desc">
          <h2>Build</h2>
        </div>
      </a>
    </li>
  </ul>
  </div> <!-- /bootcamp-body -->
</div>

<div class="next-steps">
  <p>If you are new to OpenGeoSys please pass through our 4 steps tutorial:</p>
  <ol>
    <li>In <a href="https://help.github.com/articles/set-up-git">Set Up Git</a> you will learn how to install the Git client which will let you access the version control system</li>
    <li>In <a href="{{site.baseurl}}/prerequisites-redirect">Set Up Prerequisites</a> you will be guided the installation process of other required tools such as an IDE and CMake</li>
    <li>Now it is time to <a href="{{site.baseurl}}/configure-cmake-redirect">Configure your build</a> with CMake to get the configuration and feature set of OpenGeoSys you need</li>
    <li>Finally you can <a href="{{site.baseurl}}/build-redirect">Build OpenGeoSys</a> to create the executable</li>
  </ol>
</div>

----

**Note:** This guide is primarily suited for [OpenGeoSys-6](https://github.com/ufz/ogs) but most of it applies in the same way to [OGS-5](https://svn.ufz.de/ogs).

<!-- <div class="list-module">
  <h2>Popular Guides</h2>
  <div class="list-body">
    <ul>
      {% for post in site.categories.popular reversed %}
        <li>
          <a href="{{ post.url }}" id="{{ cat }}">
            <h3>{{ post.title }}</h3>
            <p>{{ post.description }}</p>
          </a>
        </li>
      {% endfor %}
    </ul>
  </div>
</div> -->
