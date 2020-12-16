---
title: "Publications | 论文"
layout: gridlay
excerpt: "Publications"
sitemap: false
permalink: /publications/
---

<p></p>

(<b>*</b> Corresponding author; <b>#</b> First author was advised by Lei Zhu )

<p></p>

{% for publi in site.data.publist %}

{% if year_flag == 1 %}
  <b>{{ publist.year }}</b>
  <br />  
  {{ publist.authors }}, <b>{{ publist.title }}</b>, <em>{{  journal }}</em>, [<a href="{{ publist.url }}">{{ publist.display }}]</a>
  <br />
{% endif %}

{% if year_flag == 0 %}
  {{ publist.authors }}, <b>{{ publist.title }}</b>, <em>{{  journal }}</em>, [<a href="{{ publist.url }}">{{ publist.display }}]</a>
  <br />
{% endif %}

{% endfor %}
