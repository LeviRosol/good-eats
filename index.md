---
layout: default
title: Levi's Good Eats
---

# Levi's Good Eats
Weeknight-friendly recipes and cook cards.

<!-- Latest (most recent 5 recipes across all collections) -->
## Latest
<ul>
{% assign all = site.recipes | sort: 'date' | reverse %}
{% for r in all limit:5 %}
  <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
{% endfor %}
</ul>

<!-- By category (based on folder names or front-matter tags) -->
## Entrees
<ul>
{% for r in site.recipes %}
  {% if r.path contains '/entrees/' %}
    <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

## Sides
<ul>
{% for r in site.recipes %}
  {% if r.path contains '/sides/' %}
    <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

## Sauces & Basics
<ul>
{% for r in site.recipes %}
  {% if r.path contains '/basics/' %}
    <li><a href="{{ r.url | relative_url }}">{{ r.title }}</a></li>
  {% endif %}
{% endfor %}
</ul>

<!-- Optional: tag cloud -->
{% if site.tags %}
## Tags
<p>
{% for tag in site.tags %}
  <a href="{{ '/tags/#' | append: tag[0] | relative_url }}" style="margin-right:10px;">#{{ tag[0] }}</a>
{% endfor %}
</p>
{% endif %}
