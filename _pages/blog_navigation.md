---
layout: default
title: Blogs
permalink: /blog/
heading: Blogs
subheading: Read what I have to say!
---
<div style="height:100%; background-color: #184559">
    <div class="blog-navigation-wrapper">
      <div class="ui stackable cards">
          {% for post in site.posts %}
          <a class="ui centered card inverted stackable raised" href="{{ post.url }}" >
            <div class="image">
              <img src="../assets/img/{{ post.image }}">
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
</div>



