---
layout: default
title: Welcome to the OGS developer guide
---

<div class="bootcamp-help">
  <h1>OGS developer guide <span>New to OGS development? This will get you started.</span>
  </h1>
  <div class="bootcamp-body">
  <ul>
    <li class="setup">
      <a href="/devguide/set-up-git-redirect">
        <div class="image">&nbsp;</div>
        <div class="desc">
          <h2>Set Up Git</h2>
        </div>
      </a>
    </li>
    <li class="create-a-repo">
      <a href="/devguide/create-a-repo">
        <div class="image">&nbsp;</div>
        <div class="desc">
          <h2>Create A Repo</h2>
        </div>
      </a>
    </li>
    <li class="fork-a-repo">
      <a href="/devguide/fork-a-repo">
        <div class="image">&nbsp;</div>
        <div class="desc">
          <h2>Fork OGS Repo</h2>
        </div>
      </a>
    </li>
    <li class="be-social">
      <a href="/devguide/be-social">
        <div class="image">&nbsp;</div>
        <div class="desc">
          <h2>Be social</h2>
        </div>
      </a>
    </li>
  </ul>
  </div> <!-- /bootcamp-body -->
</div>

<div class="list-module">
  <h2>Popular Guides</h2>
  <div class="list-body">
    <ul>
      {% for post in site.categories.popular reversed %}
        <li>
          <a href="/devguide{{ post.url }}" id="{{ cat }}">
            <h3>{{ post.title }}</h3>
            <p>{{ post.description }}</p>
          </a>
        </li>
      {% endfor %}
    </ul>
  </div>
</div>
