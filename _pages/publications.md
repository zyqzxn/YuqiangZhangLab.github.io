---
title: "Publications | 论文"
layout: gridlay
excerpt: "Publications"
sitemap: false
permalink: /publications/
---

<p></p>

(* Corresponding author; XXX ACMRSG members are in bold )

<p></p>

{% for publi in site.data.publist %}

{% if {{ publi.year_flag }} == 1 %}

<b>{{ publi.year }}</b>
<p></p>
{{ publi.authors }}, <b>{{ publi.title }}</b>, <em>{{  publi.journal }}</em>, <a href="{{ publi.url }}">{{ publi.display }}</a>
<br /> 

{% endif %}

{% endfor %}
