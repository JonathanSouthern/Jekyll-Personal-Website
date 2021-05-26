---
layout: default
title: Projects
permalink: /project/
heading: Projects
subheading: See the work I've done!
---
<div class="row row-cols-1 row-cols-md-3 g-4 align-items-center justify-content-center">
  {% for post in site.posts %}
    <div class="col">
      <div class="card text-white bg-dark w-75 h-100" href="{{ post.url }}" >
        <img class="card-img-top" src="{{ post.thumbnail }}">
        <div class="card-body">
          <h5 class="card-title">{{post.title}}</h5>
          <p class="card-text">{{ post.description | truncatewords: 30 }} </p>
        </div>
        <div class="card-footer">
              <small class="text-muted">{{ post.tag }} • {{ post.date-custom }}</small>
        </div>
        <a href="{{ post.url }}" class="stretched-link"></a>
      </div>
    </div>
  {% endfor %}
</div>
