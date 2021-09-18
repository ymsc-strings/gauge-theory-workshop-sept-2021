---
title: "Participants"
permalink: /participants.html
layout: single
classes: wide
toc: false
sidebar:
    - nav: sitemap
    - nav: contact
other_participants:
    - Xiaobin Li, SWJT Chengdu
    - Hao Wang, Fudan University
    - Peihe Yang, Tianjin University
    - Jiang Jiaqun, Fudan University

---

{% comment %}
    speakers are in \_data/navigation.yml
    other_participants are in above claims
{% endcomment %}

<ul>
    {% assign sorted_speakers = site.data.navigation.speakers | sort: 'name' %}
    {% for s in sorted_speakers %}
        <li> {{ s.name }} </li>
    {% endfor %}
    {% assign sorted_participants = page.other_participants | sort %}
    {% for s in sorted_participants %}
        <li> {{ s }} </li>
    {% endfor %}
</ul>
