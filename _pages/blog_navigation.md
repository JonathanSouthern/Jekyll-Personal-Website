---
layout: default
title: Blogs
permalink: /blog/
heading: Blogs
subheading: Read what I have to say!
---
<div style="height:100%; background-color: #184559">
      <div id="blog-posts" class="row justify-content-center">
        {% for post in site.posts %}
        <div
          class="card col-lg-3 col-md-4 col-sm-12"
          data-clickable="true"
          data-href="{{ post.url }}"
        >
          <img
            src="../assets/img/{{ post.image }}"
            class="card-img-top"
            alt="..."
          />
          <div class="card-body">
            <h5 class="card-title">{{ post.title }}</h5>
            <small class="text-muted"
              >{{ post.tag }} • {{ post.date-custom }}</small
            >
            <p class="card-text">{{ post.description | truncatewords: 30 }}</p>
            <p class="text-right text-muted">Read More ➜</p>
          </div>
        </div>
        {% endfor %}
      </div>
    </div>
