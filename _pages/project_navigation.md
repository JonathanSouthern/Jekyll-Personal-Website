---
layout: default
title: Projects
permalink: /project/
heading: Projects
subheading: See the work I've done!
---

<div class="ui divided inverted items">
  {% for post in site.posts %}
    <div class="item">
      <div class="image">
        <img src="../assets/img/{{ post.image }}">
      </div>
      <div class="content">
        <a class="header">{{post.title}}</a>
        <div class="description">
          <p>{{ post.description | truncatewords: 150 }}</p>
        </div>
        <div class="extra">
          <div class="ui label">{{ post.tag }} </div>
        </div>
      </div>
    </div>
  {% endfor %}
</div>