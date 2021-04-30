---
title: "Presentations | 报告"
layout: gridlay
excerpt: "Presentations"
sitemap: false
permalink: /presentations/
---

<div class="row">
<div class="col-sm-6 clearfix">

### Talks

{% for talk in site.data.talks %}

  {% if talk.invited_talk == 1 %}
  {{ talk.title }}, presented by {{ talk.presenter }} at <b>{{ talk.meeting }}</b>, <u>{{ talk.date }}</u>, {{ talk.location }}. <b>(Invited)</b>
  {% endif %} 

  {% if talk.invited_talk == 0 %}
  {{ talk.title }}, presented by {{ talk.presenter }} at <b>{{ talk.meeting }}</b>, <u>{{ talk.date }}</u>, {{ talk.location }}.
  {% endif %} 
  
{% endfor %}
</div>

<div class="col-sm-6 clearfix">

### Posters

{% for poster in site.data.posters %}

  {{ poster.title }}, presented by {{ poster.presenter }} at <b>{{ poster.meeting }}</b>, <u>{{ poster.date }}</u>, {{ poster.location }}.
  
{% endfor %}
</div>
</div>
