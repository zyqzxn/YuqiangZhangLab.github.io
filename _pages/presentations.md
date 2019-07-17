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

{% for talk in site.data.talklist %}

  {% if talk.invited_talk == 1 %}
  {{ talk.title }}, presented by {{ talk.presenter }} at <i>{{ talk.meeting }}</i>, <u>{{ talk.date }}</u>, {{ talk.location }}. <b>(Invited)</b>
  {% endif %} 

  {% if talk.invited_talk == 0 %}
  {{ talk.title }}, presented by {{ talk.presenter }} at <i>{{ talk.meeting }}</i>, <u>{{ talk.date }}</u>, {{ talk.location }}.
  {% endif %} 
  
{% endfor %}
</div>

<div class="col-sm-6 clearfix">

### Posters

{% for poster in site.data.posterlist %}

  {{ poster.title }}, presented by {{ poster.presenter }} at <i>{{ poster.meeting }}</i>, <u>{{ poster.date }}</u>, {{ poster.location }}.
  
{% endfor %}
</div>
</div>
