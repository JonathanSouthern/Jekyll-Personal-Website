---
layout: default
title: Blogs
permalink: /blog/
heading: Blogs
subheading: Read what I have to say!
---
<!-- TAG SELECTOR -->
<ul class="nav nav-pills dark my-3 justify-content-center" id="blog-navigation" role="tablist">
  <li class="nav-item">
    <a class="nav-link active" id="all-tab" data-toggle="pill" href="#all" role="tab" aria-controls="all" aria-selected="true">All</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="personal-tab" data-toggle="pill" href="#personal" role="tab" aria-controls="personal" aria-selected="false">Personal</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="technical-tab" data-toggle="pill" href="#technical" role="tab" aria-controls="technical" aria-selected="false">Technical</a>
  </li>
</ul>
<div class="tab-content" id="pills-tabContent">
  <!-- ALL POSTS -->
  <div class="tab-pane fade show active" id="all" role="tabpanel" aria-labelledby="all-tab">
    <div class="mx-auto px-3 py-5">
      <ul class="list mb-5 mx-auto">
        {% for post in site.posts %}
          <li >
            <a href="{{ post.url }}">{{post.title}}</a>
            <span>{{ post.date-custom }}</span>
          </li>
        {% endfor %}
      </ul>
    </div>
  </div>
  <!-- PERSONAL POSTS -->
  <div class="tab-pane fade" id="personal" role="tabpanel" aria-labelledby="personal-tab">
    <div class="mx-auto px-3 py-5">
      <ul class="list mb-5 mx-auto">
        {% for post in site.posts %} 
          {% if post.tags contains "personal" %}
            <li>
              <a href="{{ post.url }}">{{post.title}}</a>
              <span>{{ post.date-custom }}</span>
            </li>
          {% endif %}
        {% endfor %}
      </ul>
    </div>
  </div>
  <!-- TECHINCAL POSTS -->
  <div class="tab-pane fade" id="technical" role="tabpanel" aria-labelledby="technical-tab">
    <div class="mx-auto px-3 py-5">
      <ul class="list mb-5 mx-auto">
        {% for post in site.posts %} 
          {% if post.tags contains "technical" %}
            <li>
              <a href="{{ post.url }}">{{post.title}}</a>
              <span>{{ post.date-custom }}</span>
            </li>
          {% endif %}
        {% endfor %}
      </ul>
    </div>
  </div>
</div>





