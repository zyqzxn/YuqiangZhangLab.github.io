---
title: "Air Quality Modeling and Remote Sensing Group - Presentations"
layout: gridlay
excerpt: "Presentations"
sitemap: false
permalink: /presentations/
---

## Presentations

{% for preli in site.data.prelist %}

  {% if preli.invited_talk == 1 %}
  {{ preli.title }}, presented by {{ preli.presenter }} at <i>{{ preli.meeting }}</i>, <u>{{ preli.date }}</u>, {{ preli.location }}. <b>(Invited Talk)</b>
  {% endif %} 

  {% if preli.normal_talk == 1 %}
  {{ preli.title }}, presented by {{ preli.presenter }} at <i>{{ preli.meeting }}</i>, <u>{{ preli.date }}</u>, {{ preli.location }}. (Talk)
  {% endif %} 

  {% if preli.poster == 1 %}
  {{ preli.title }}, presented by {{ preli.presenter }} at <i>{{ preli.meeting }}</i>, <u>{{ preli.date }}</u>, {{ preli.location }}. (Poster)
  {% endif %}   
  
{% endfor %}