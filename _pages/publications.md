---
title: "Publications | 论文"
layout: gridlay
excerpt: "Publications"
sitemap: false
permalink: /publications/
---

<p></p>

(<b>*</b> Corresponding author; PPP <b>#</b> First author was advised by Lei Zhu )

<p></p>

{% for publi in site.data.publist %}

  {{ publi.authors }}, <b>{{ publi.title }}</b>, <em>{{  publi.journal }}</em>, <a href="{{ publi.url }}">{{ publi.display }}</a>
  <br /> 

{% endfor %}
