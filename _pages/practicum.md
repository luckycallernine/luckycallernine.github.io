---
title:
layout: default
permalink: /practicum/
published: true
---


<div class="PracticumContainer">

	<div class="gallery">


  {% for project in site.practicum %}

  {% if practicum.redirect %}
  <div class="practicumTile">
          <a href="{{ practicum.redirect }}" target="_blank">
          <span>
              <h2>{{ practicum.title }}</h2>
              <br/>
              <p>{{ practicum.description }}</p>
          </span>
          </a>
  </div>

  {% else %}

  <div class="practicumTile">
          <a href="{{ practicum.url | prepend: site.baseurl | prepend: site.url }}">
          <span>
              <h2>{{ practicum.title }}</h2>
              <br/>
              <p>{{ practicum.description }}</p>
          </span>
          </a>
  </div>

  {% endif %}

  {% endfor %}

	</div>

</div>
