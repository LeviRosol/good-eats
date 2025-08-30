---
layout: posts
title: Basics
permalink: /recipes/basics/
---
<ul>
{% assign basics = site.recipes | where_exp:'r','r.url contains "/recipes/basics/"' | sort:'title' %}
{% for r in basics %}
  <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
{% endfor %}
</ul>
