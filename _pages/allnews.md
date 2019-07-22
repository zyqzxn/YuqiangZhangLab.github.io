---
title: "News | 新闻"
layout: textlay
excerpt: "News"
sitemap: false
permalink: /allnews.html
---

### News

{% for article in site.data.news %}
<p><u>{{ article.date }}</u> <br>
{{ article.headline }}</p>
{% endfor %}
