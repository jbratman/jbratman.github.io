---
layout: archive
title: "Projects - Work In Progress"
permalink: /projects/
entries_layout: grid
author_profile: true
sort_by: date
sort_order: reverse
---

{% assign entries = site.portfolio | sort: 'date' | reverse %}
{% for post in entries %}
  {% include archive-single.html type="grid" %}
{% endfor %}

