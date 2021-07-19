---
title: "Publications | 论文"
layout: gridlay
excerpt: "Publications"
sitemap: false
permalink: /publications/
---

<p></p>

(<b>*</b> Corresponding author; ACMRSG members are in bold )

<p></p>

{% for publication in site.data.publications %}

{{ publication.authors }}: <b>{{ publication.title }}</b>, <u><em>{{  publication.journal }}</em></u>, {{ publication.year }}. <a href="{{ publication.url }}">{{ publication.display }}</a>
<br /> 

{% endfor %}
