---
layout: default
title: Blogs
permalink: /blog/
heading: Blogs
subheading: Read what I have to say!
---
<div style="height:100%; background-color: #184559">
  <div class="ui stackable cards">
      {% for post in site.posts reversed  %}
      <a class="ui centered card inverted stackable raised" href="{{ post.url }}" >
        <div class="image">
          <img src="{{ post.thumbnail }}">
        </div>
        <div class="content">
          <div class="header">{{post.title}}</div>
          <div class="meta">{{ post.tag }} • {{ post.date-custom }}</div>
          <div class="description">{{ post.description | truncatewords: 30 }} </div>
        </div>
      </a>
      {% endfor %}
  </div>
</div>



