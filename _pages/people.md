---
title: "People"
layout: gridlay
excerpt: "People"
sitemap: false
permalink: /people/
---

## Group Members

{% assign number_printed = 0 %}
{% for member in site.data.people %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-9 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/peopic/{{ member.photo }}" class="img-responsive" width="22%" style="float: left" />
  <h4>{{ member.name }}</h4>
  {{ member.info }}<br>
  
  {% if member.group_member == 1 %}
  <i>Email: {{ member.email }}</i><br>
  {% endif %}

  {% if member.number_educ == 1 %}
  <li> {{ member.education1 }} </li>
  {% endif %}
  
  {% if member.number_educ == 2 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  {% endif %}
  
  {% if member.number_educ == 3 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  {% endif %}
  
  {% if member.number_educ == 4 %}
  <p>
  {{ member.education1 }} <br>
  {{ member.education2 }} <br>
  {{ member.education3 }} <br>
  {{ member.education4 }} <br>
  </p>
  {% endif %}
  
  {% if member.number_educ == 5 %}
  <li> {{ member.education1 }} </li>
  <li> {{ member.education2 }} </li>
  <li> {{ member.education3 }} </li>
  <li> {{ member.education4 }} </li>
  <li> {{ member.education5 }} </li>
  {% endif %}
  
  {% if member.group_member == 1 %}
  <p>{{ member.statement }} </p>
  {% endif %}

</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}
