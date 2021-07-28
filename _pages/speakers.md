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

<ul>
    <!-- speakers are in _data/navigation.yml -->
    {% for s in site.data.navigation.speakers %}
        <li> {{ s.name }} </li>
    {% endfor %}
</ul>