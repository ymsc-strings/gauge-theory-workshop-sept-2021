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
    - Hao Wang, Fudan
    - Peihe Yang, Tianjin
    - Jiang Jiaqun, Shanghai

---

<ul>
    <!-- speakers are in _data/navigation.yml -->
    {% for s in site.data.navigation.speakers %}
        <li> {{ s.name }} </li>
    {% endfor %}
    {% for s in page.other_participants %}
        <li> {{ s }} </li>
    {% endfor %}
</ul>