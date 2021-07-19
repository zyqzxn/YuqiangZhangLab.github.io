---
title: "People | 成员"
layout: gridlay
excerpt: "People"
sitemap: false
permalink: /people/
---

### Current group members

{% assign number_printed = 0 %}
{% for member in site.data.people %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/peopic/{{ member.photo }}" class="img-responsive" width="26%" style="float: left" />
  <h4>{{ member.name }}</h4>
  {{ member.info }}<br>
  
  {% if member.group_member == 1 %}
  <i>Email: {{ member.email }}</i><br>
  {% endif %}

  {% if member.number_educ == 1 %}
  <p>
  {{ member.education1 }} <br>
  </p>
  {% endif %}
  
  {% if member.number_educ == 2 %}
  <p>
  {{ member.education1 }} <br>
  {{ member.education2 }} <br>
  </p>
  {% endif %}
  
  {% if member.number_educ == 3 %}
  <p>
  {{ member.education1 }} <br>
  {{ member.education2 }} <br>
  {{ member.education3 }} <br>
  </p>
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
  <p>
  {{ member.education1 }}  
  {{ member.education2 }}  
  {{ member.education3 }}  
  {{ member.education4 }}  
  {{ member.education5 }}
  </p>
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

<p></p>

### Alumni List

<div class="row">
<div class="col-sm-10 clearfix">

{% for alumni in site.data.alumni %}

  {{ alumni.name }}, {{ alumni.info }}, Now: {{ alumni.now }}.
  
{% endfor %}

</div>
</div>

