---
title: "Publications | 论文"
layout: gridlay
excerpt: "Publications"
sitemap: false
permalink: /publications/
---

<p></p>

(* Corresponding author; PPP ACMRSG members are in bold )

<p></p>

{% for publi in site.data.publist %}


    <b>{{ publi.year }}</b>
    <br />  
    {{ publi.authors }}, <b>{{ publi.title }}</b>, <em>{{  publi.journal }}</em>, <a href="{{ publi.url }}">{{ publi.display }}</a>
    <br /> 


{% endfor %}
