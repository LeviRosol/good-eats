---
layout: posts
title: Menus
permalink: /recipes/menus/
---
<ul>
{% assign menus = site.recipes | where_exp:'r','r.url contains "/recipes/menus/"' | sort:'title' %}
{% for r in menus %}
  <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
{% endfor %}
</ul>
