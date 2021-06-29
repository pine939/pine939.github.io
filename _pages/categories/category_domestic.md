---
title: "Review domestic journal/conference"
layout: archive
permalink: categories/domestic
author_profile: true
sidebar:
  nav: docs
---

{% assign posts = site.categories.domestic %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
