---
title:
layout: default
permalink: /env/
published: true
---


<div class="ProjectContainer">

	<div class="gallery">


  {% for article in site.env %}

  {% if env.redirect %}
  <div class="projectTile">
          <a href="{{ env.redirect }}" target="_blank">
          <span>
              <h2>{{ env.title }}</h2>
              <br/>
              <p>{{ env.description }}</p>
          </span>
          </a>
  </div>

  {% else %}

  <div class="projectTile">
          <a href="{{ article.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>{{ env.title }}</h2>
              <br/>
              <p>{{ env.description }}</p>
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
