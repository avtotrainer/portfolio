---
title: ᲒᲐᲠᲔᲛᲝ
layout: default
permalink: /envi/
published: true
---


<div class="ProjectContainer">

	<div class="gallery">


  {% for article in site.envi %}

  {% if envi.redirect %}
  <div class="projectTile">
          <a href="{{ envi.redirect }}" target="_blank">
          <span>
              <h2>{{ envi.title }}</h2>
              <br/>
              <p>{{ envi.description }}</p>
          </span>
          </a>
  </div>

  {% else %}

  <div class="projectTile">
          <a href="{{ article.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>სათაური: {{ envi.title }}</h2>
              <br/>
              <p>აღწერა: {{ envi.description }}</p>
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
