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
    - gname: Xiaobin
      fname: Li
      from: SWJT Chengdu
    - gname: Hao
      fname: Wang
      from: Fudan University
    - gname: Peihe
      fname: Yang
      from: Tianjin University
    - gname: Jiaqun
      fname: Jiang
      from: Fudan University
    - gname: Babak
      fname: Haghighat
      from: YMSC Tsinghua University
    - gname: Fengjun
      fname: Xu
      from: BIMSA
    - gname: Jirui
      fname: Guo
      from: YMSC Tsinghua University
    - gname: Wei
      fname: Cui
      from: BIMSA
    - gname: Ken
      fname: Kikuchi
      from: YMSC Tsinghua University
    - gname: Qingsheng
      fname: Zhang
      from: Peking University
    - gname: Mauricio
      fname: Romo
      from: YMSC Tsinghua University
    - gname: Rui
      fname: Dong
      from: BIMSA
    - gname: Hao
      fname: Zou
      from: BIMSA
    - gname: Hongfei
      fname: Shu
      from: BIMSA

---

{% comment %}
    speakers are in \_data/navigation.yml
    other_participants are in above claims
{% endcomment %}

{% assign sorted_speakers = site.data.navigation.speakers | sort:'gname' | sort: 'fname' %}
{% assign sorted_participants = page.other_participants | sort:'gname' | sort: 'fname' %}

<table>
<tbody>
    {% for s in sorted_speakers %}
        <tr>
            <td> {{ s.gname }}&nbsp;{{ s.fname }} </td>
            <td> {{ s.from }} </td>
        </tr>
    {% endfor %}
    {% for s in sorted_participants %}
        <tr>
            <td> {{ s.gname }}&nbsp;{{ s.fname }} </td>
            <td> {{ s.from }} </td>
        </tr>
    {% endfor %}
</tbody>
</table>
