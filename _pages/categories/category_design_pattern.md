---
title: "Design"
layout: archive
permalink: categories/design_pattern
author_profile: true
sidebar:
  nav: docs
---

{% assign posts = site.categories.design_pattern %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}