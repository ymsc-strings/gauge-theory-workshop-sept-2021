---
title: "Gauge Theory Workshop"
permalink: /index.html
layout: single
classes: wide
toc: false
sidebar:
    - nav: sitemap
    - nav: contact
---

* Dates: 24-26 Sept 2021
* Venue: Yau Mathematical Sciences Center, Tsinghua University
* Contact Information
    <ul>
        {% for child in site.data.navigation.contact[0].children %}
            <li>
            <div>{{child.title}}</div>
            <a href="mailto:{{ child.mail }}">{{ child.mail }}</a>
            </li>
        {% endfor %}
    </ul>