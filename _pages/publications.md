---
title: "Publications | 论文"
layout: gridlay
excerpt: "Publications"
sitemap: false
permalink: /publications/
---

<p></p>

(* Corresponding author; ACMRSG members are shown in bold )

<p></p>

{% for publi in site.data.publist %}


{{ publi.authors }}, <b>{{ publi.title }}</b>, <em>{{  publi.journal }}</em>, <a href="{{ publi.url }}">{{ publi.display }}</a>
<br /> 

{% endfor %}
