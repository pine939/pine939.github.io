---
title: "ELK Stack"
layout: archive
permalink: categories/elkstack
author_profile: true
sidebar:
  nav: docs
---

{% assign posts = site.categories.elkstack %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}