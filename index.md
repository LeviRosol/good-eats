---
layout: home
---

Weeknight-friendly recipes and cook cards.

## Recent Additions
<ul>
{% assign latest = site.recipes | sort: 'modified_time' | reverse %}
{% for r in latest limit:5 %}
  <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
{% endfor %}
</ul>

## Entrees (A–Z)
<ul>
{% assign entrees = site.recipes | where_exp:'r','r.url contains "/recipes/entrees/"' | sort:'title' %}
{% for r in entrees %}
  <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
{% endfor %}
</ul>

## Sides (A–Z)
<ul>
{% assign sides = site.recipes | where_exp:'r','r.url contains "/recipes/sides/"' | sort:'title' %}
{% for r in sides %}
  <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
{% endfor %}
</ul>

## Sauces & Basics (A–Z)
<ul>
{% assign basics = site.recipes | where_exp:'r','r.url contains "/recipes/basics/"' | sort:'title' %}
{% for r in basics %}
  <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
{% endfor %}
</ul>
