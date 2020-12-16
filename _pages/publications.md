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

{% for publi in site.data.publist_SUSTech %}

{% if year_flag == 1 %}
  <b>{{ publist_SUSTech.year }}</b>
  <br />  
{% endif %}

{% if year_flag == 0 %}
  {{ publist_SUSTech.authors }}, <b>{{ publist_SUSTech.title }}</b>, <em>{{  journal }}</em>, [<a href="{{ publist_SUSTech.url }}">{{ publist_SUSTech.display }}]</a>
  <br />
{% endif %}

{% endfor %}
