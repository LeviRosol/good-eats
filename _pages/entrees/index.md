---
layout: posts
title: Entrees
permalink: /recipes/entrees/
---
<ul>
{% assign entrees = site.recipes | where_exp:'r','r.url contains "/recipes/entrees/"' | sort:'title' %}
{% for r in entrees %}
  <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
{% endfor %}
</ul>
