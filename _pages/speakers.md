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

<ul>
    {% assign sorted_speakers = site.data.navigation.speakers | sort: 'name' %}
    {% for s in sorted_speakers %}
        <li> {{ s.name }}, <small>{{ s.from }}</small> </li>
    {% endfor %}
</ul>