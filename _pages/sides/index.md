---
layout: posts
title: Sides
permalink: /recipes/sides/
---
<ul>
{% assign sides = site.recipes | where_exp:'r','r.url contains "/recipes/sides/"' | sort:'title' %}
{% for r in sides %}
  <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
{% endfor %}
</ul>
