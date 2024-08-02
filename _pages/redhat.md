---
title: Red
layout: default
permalink: /redhat/
published: true
---

<div class="ProjectContainer">

    <div class="gallery">

{% for article in site.redhat %}

{% if article.redirect %}

  <div class="projectTile">
          <a href="{{ article.redirect }}" target="_blank">
          <span>
              <h2>{{ article.title }}</h2>
              <br/>
              <p>{{ article.description }}</p>
          </span>
          </a>
  </div>

{% else %}

  <div class="projectTile">
          <a href="{{ article.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>{{ article.title }}</h2>
              <br/>
              <p>{{ article.description }}</p>
          </span>
          </a>
  </div>

{% endif %}

{% endfor %}

    </div>

</div>
