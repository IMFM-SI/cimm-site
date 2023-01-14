---
layout: page
title: Research projects
---

# Research projects

{% assign projects = site.projects | sort: "start" %}
{% for project in site.projects reversed %}

{% if project.url %}
## [{{ project.title }}]({{ project.url }})
{% else %}
## {{ project.title }}
{% endif %}

<ul class="project-info">
    {% if project.sicris %}
    <li>
        <a href="{{ project.sicris }}">SICRIS</a>
    </li>
    {% endif %}
    <li>
        <span>
        {% if project.principal_investigators.size > 1 %}
            Principal investigators:
        {% else %}
            Principal investigator:
        {% endif %}
        </span>
        <ul class="inline-list">
        {% for pi in project.principal_investigators %}
        <li>{{ pi | markdownify | remove: '<p>' | remove: '</p>' }}</li>
        {% endfor %}
        </ul>
    </li>
    {% if project.pg_investigators %}
    <li>
        <span>Member(s) participating in the project:</span>
        <ul class="inline-list">
        {% for pgi in project.pg_investigators %}
        <li>{{ pgi }}</li>
        {% endfor %}
        </ul>
    </li>
    {% endif %}
    <li>
        <span>Funding:</span> {{ project.funding | markdownify | remove: '<p>' | remove: '</p>' }}
    </li>
    <li>
        <span>Project start:</span> {{ project.start | date: "%-d %B %Y" }}
    </li>
    <li>
        <span>Project end:</span> {{ project.end | date: "%-d %B %Y" }}
    </li>
</ul>

{{ project.content | markdownify }}

{% endfor %}