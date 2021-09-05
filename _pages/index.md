---
title: "Fields, Strings and Geometries"
permalink: /index.html
layout: single
classes: wide
toc: false
sidebar:
    - nav: sitemap
    - nav: contact
---

* Dates: 24-26 Sept 2021
* Venue: 3rd floor lecture hall of Jinchunyuan West Building 近春园西楼三楼报告厅
* Hotel: Tsinghua Jiasuo hotel 清华甲所宾馆
* Contact Information
    <ul>
        {% for child in site.data.navigation.contact[0].children %}
            <li>
            <div>{{child.title}}</div>
            <a href="mailto:{{ child.mail }}">{{ child.mail }}</a>
            </li>
        {% endfor %}
    </ul>