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
    - name: Xiaobin Li
      from: SWJT Chengdu
    - name: Hao Wang
      from: Fudan University
    - name: Peihe Yang
      from: Tianjin University
    - name: Jiang Jiaqun
      from: Fudan University
    - name: Junya Yagi
      from: YMSC Tsinghua University
    - name: Babak Haghighat
      from: YMSC Tsinghua University

---

{% comment %}
    speakers are in \_data/navigation.yml
    other_participants are in above claims
{% endcomment %}

{% assign sorted_speakers = site.data.navigation.speakers | sort: 'name' %}
{% assign sorted_participants = page.other_participants | sort: 'name' %}

<table>
<tbody>
    {% for s in sorted_speakers %}
        <tr>
            <td> {{ s.name }} </td>
            <td> {{ s.from }} </td>
        </tr>
    {% endfor %}
    {% for s in sorted_participants %}
        <tr>
            <td> {{ s.name }} </td>
            <td> {{ s.from }} </td>
        </tr>
    {% endfor %}
</tbody>
</table>

{% comment %}
<ul>
    {% for s in sorted_speakers %}
        <li> {{ s.name }}, {{ s.from }}</li>
    {% endfor %}
    {% for s in sorted_participants %}
        <li> {{ s }} </li>
    {% endfor %}
</ul>
{% endcomment %}
