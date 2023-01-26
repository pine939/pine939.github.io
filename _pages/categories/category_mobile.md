---
title: "Mobile"
layout: archive
permalink: categories/mobile
author_profile: true
sidebar:
  nav: docs
---

{% assign posts = site.categories.mobile %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
