---
title: "Zhu Lab - Team"
layout: gridlay
excerpt: "Zhu Lab: Team members"
sitemap: false
permalink: /team/
---

##

# Group Members

 **We are  looking for new Research Assissants, PhD students, Postdocs, and Master students to join the team** [(see openings)]({{ site.url }}{{ site.baseurl }}/vacancies) **!**


{% assign number_printed = 0 %}
{% for member in site.data.team_members %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-8 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="30%" style="float: left" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.info }}<br>email: <{{ member.email }}></i>
  <ul style="overflow: hidden">

  {% if member.number_educ == 1 %}
  {{ member.education1 }}<br>
  {% endif %}

  {% if member.number_educ == 2 %}
  {{ member.education1 }}<br>
  {{ member.education2 }}<br>
  {% endif %}

  {% if member.number_educ == 3 %}
  {{ member.education1 }}<br>
  {{ member.education2 }}<br>
  {{ member.education3 }}<br>
  {% endif %}

  {% if member.number_educ == 4 %}
  {{ member.education1 }}<br>
  {{ member.education2 }}<br>
  {{ member.education3 }}<br>
  {{ member.education4 }}<br>
  {% endif %}

  {% if member.number_educ == 5 %}
  {{ member.education1 }}<br>
  {{ member.education2 }}<br>
  {{ member.education3 }}<br>
  {{ member.education4 }}<br>
  {{ member.education5 }}<br>
  {% endif %}

  </ul>
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
