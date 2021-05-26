---
layout: default
title: Blogs
permalink: /blog/
heading: Blogs
subheading: Read what I have to say!
---
<div class="mx-auto px-3 py-5">
  <ul class="list mb-5 mx-auto">
    {% for post in site.posts %}
      <li >
        <a href="{{ post.url }}">{{post.title}}</a>
        <span>{{ post.date-custom }}</span>
        <!-- <div class="card text-white bg-dark w-75 h-100" href="{{ post.url }}" >
          <img class="card-img-top" src="{{ post.thumbnail }}">
          <div class="card-body">
            <h5 class="card-title">{{post.title}}</h5>
            <p class="card-text">{{ post.description | truncatewords: 30 }} </p>
          </div>
          <div class="card-footer">
                <small class="text-muted">{{ post.tag }} • {{ post.date-custom }}</small>
          </div>
          <a href="{{ post.url }}" class="stretched-link"></a>
        </div> -->
      </li>
    {% endfor %}
  </ul>
</div>



