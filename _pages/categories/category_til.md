---
title: "Today I Learn"
layout: archive
permalink: categories/til
author_profile: true
sidebar:
  nav: docs
---

{% assign posts = site.categories.til %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}
