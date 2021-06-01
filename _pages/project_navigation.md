---
layout: default
title: Projects
permalink: /project/
heading: Projects
subheading: See the work I've done!
---
<h3 class="row">Professional</h3>
<div class="row card-deck">
  {% for project in site.categories['project'] %}
    {% if project.tags contains "professional" %}
      <div class="col-12 col-md-4">
        <div class="card text-white bg-dark">
          <img class="card-img-top" src="{{ project.thumbnail }}">
          <div class="card-body">
            <h5 class="card-title">{{project.title}}</h5>
          </div>
          <a href="{{ project.url }}" class="stretched-link"></a>
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>

<h3 class="row mt-5">Personal</h3>
<div class="row card-deck mb-5">
  {% for project in site.categories['project'] %}
    {% if project.tags contains "personal" %}
      <div class="col-12 col-md-4">
        <div class="card text-white bg-dark" >
          <img class="card-img-top" src="{{ project.thumbnail }}">
          <div class="card-body">
            <h5 class="card-title">{{project.title}}</h5>
          </div>
          <a href="{{ project.url }}" class="stretched-link"></a>
        </div>
      </div>
    {% endif %}
  {% endfor %}
</div>
