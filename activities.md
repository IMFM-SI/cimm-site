---
layout: page
title: Activities
---

{% assign activities_by_year = site.data.activities %}

# Activities

[Seminar za računalniško matematiko - Sredin seminar](https://www.fmf.uni-lj.si/sl/raziskave/seminar-za-racunalnisko-matematiko/)

Jump to year:

<ul class="inline-list">
{% for activities_hash in activities_by_year reversed %}
{% assign year = activities_hash[0] %}
<li><a href="#{{ year }}">{{ year }}</a></li>
{% endfor %}
</ul>

{% for activities_hash in activities_by_year reversed %}

## {{ activities_hash[0] }}

<dl class="activities-list">

{% assign activities = activities_hash[1] | sort: "start_date" %}
{% for activity in activities reversed %}

<dt>
{% if activity.end_date %}
  {% assign start = activity.start_date | split: "-" %}  
  {% assign end = activity.end_date | split: "-" %}
  {% if start[0] == end[0] and start[1] == end[1] and start[2] == end[2] %}
  {{ activity.start_date | date: "%-d %B %Y" }}
  {% elsif start[0] == end[0] and start[1] == end[1] %}
  {{ activity.start_date | date: "%-d" }}-{{ activity.end_date | date: "%-d %B %Y" }}
  {% elsif start[0] == end[0] %}
  {{ activity.start_date | date: "%-d %B" }} - {{ activity.end_date | date: "%-d %B %Y" }}
  {% else %} 
  {{ activity.start_date | date: "%-d %B %Y" }} - {{ activity.end_date | date: "%-d %B %Y" }}
  {% endif %}
{% else %}
  {{ activity.start_date | date: "%-d %B %Y" }}
{% endif %}
</dt>
<dd>{{ activity.description | markdownify | remove: '<p>' | remove: '</p>' }}</dd>

{% endfor %}

</dl>

{% endfor %}