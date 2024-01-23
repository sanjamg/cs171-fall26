---
layout: home
title: Home
nav_exclude: false
permalink: /:path/
seo:
  type: Course
  name: CS 171
---

# Welcome to CS 171!

{% for module in site.modules %}
{{ module }}
{% endfor %}
