---
title: "Confirmed Speakers"
permalink: /speakers.html
layout: single
classes: wide
toc: false
sidebar:
    - nav: sitemap
    - nav: contact

---

{% comment %}
    speakers are in \_data/navigation.yml
{% endcomment %}

{% assign max_name_len = 0 %}
{% assign max_from_len = 0 %}
{% for s in site.data.navigation.speakers %}
    {% if s.name.size > max_name_len %}
        {% assign max_name_len = s.name.size %}
    {% endif %}
    {% if s.from.size > max_from_len %}
        {% assign max_from_len = s.from.size %}
    {% endif %}
{% endfor %}

<style type="text/css">
    div.speaker{
        width: {{ max_name_len }}ex;
        display:inline-block;
    }
    div.speakerfrom{
        width: {{ max_from_len }}ex;
        display:inline-block;
    }
</style>

<ul>
    {% assign sorted_speakers = site.data.navigation.speakers | sort: 'name' %}
    {% for s in sorted_speakers %}
        <li> <div class="speaker"> {{ s.name }} </div> <div class="speakerfrom"> {{ s.from }} </div> </li>
    {% endfor %}
</ul>