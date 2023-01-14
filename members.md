---
layout: page
title: Members - Gen
---

# Members

{% assign members_by_family_name = site.members | sort: "family_name" %}
{% for member in members_by_family_name %}

## {{ member.name }} {{ member.family_name }}

{{ member.content | markdownify }}

<ul class="member-profile-links">
    {% if member.sites != null %} 
    {% for site in member.sites %}
    {% assign url = site | split: "://" %}
    <li class="icon-links"><i class="fas fa-home"></i> <a href="{{ url[0] }}://{{ url[1] }}">{{ url[1] }}</a></li>
    {% endfor %}
    {% endif %}
    {% if member.orcid_id != null %}
    <li class="icon-links"><i class="ai ai-orcid"></i> <a href="https://orcid.org/{{ member.orcid_id }}">{{ member.orcid_id }}</a></li>
    {% endif %}
    {% if member.genealogy != null %}
    <li class="icon-links"><i class="fas fa-sitemap"></i> <a href="https://www.genealogy.math.ndsu.nodak.edu/id.php?id={{ member.genealogy }}">Mathematics Genealogy</a></li>
    {% endif %}
    <li class="icon-links"><i class="fas fa-scroll"></i>
        <ul class="inline-list">
            {% for link in member.links %}
                {% assign link_type = link[0] %}
                <li><a href="{{ site.data.biblinks[link_type]['url'] }}{{ link[1] }}">{{ site.data.biblinks[link_type]['name'] }}</a></li>
            {% endfor %}
        </ul>
    </li>
</ul>

{% endfor %}