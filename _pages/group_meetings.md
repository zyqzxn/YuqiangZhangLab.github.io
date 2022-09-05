---
title: "Group meettings | 组会"
layout: textlay
excerpt: "Group Meetings"
sitemap: false
permalink: /group_meetings/
---

## Group Meeting Schedule

Group meettings are held every other week.   

The normal time/place is W. 1900 in CoE North 901.  

<b>Schedule is subject to change, please check frequently. </b>

{% for meeting in site.data.group_meetings %}

<b>{{ meeting.date}}</b>  {{ meeting.presenter}}
<br /> 

{% endfor %}