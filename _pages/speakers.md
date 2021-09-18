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

{% comment %}
    I cannot add two Integers?!
{% endcomment %}

{% assign max_name_len = 0 %}
{% assign max_from_len = 0 %}
{% for s in site.data.navigation.speakers %}
    {% if s.gname.size > max_name_len %}
        {% assign max_name_len = s.gname.size %}
    {% endif %}
    {% if s.from.size > max_from_len %}
        {% assign max_from_len = s.from.size %}
    {% endif %}
{% endfor %}


<style type="text/css">
    div.speaker{
        width: 21ex;
        display:inline-block;
    }
    div.speakerfrom{
        width: {{max_from_len}}ex;
        display:inline-block;
    }
</style>

<ul>
    {% assign sorted_speakers = site.data.navigation.speakers | sort:'gname' | sort: 'fname' %}
    {% for s in sorted_speakers %}
        <li> <div class="speaker"> {{ s.gname }}&nbsp;{{ s.fname }} </div> <div class="speakerfrom"> {{ s.from }} </div> </li>
    {% endfor %}
</ul>