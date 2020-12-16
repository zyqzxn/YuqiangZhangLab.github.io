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
  <b>{{ publi.title }}</b>
  <br />  
{% endif %}

{% if year_flag == 0 %}
  {{ publi.authors }}, <b>{{ publi.title }}</b>, <em>{{  journal }}</em>, [<a href="{{ publi.link.url }}">{{ publi.link.display }}]</a>
  <br />
{% endif %}

{% endfor %}
