---
title: "Algospot"
layout: archive
permalink: categories/algospot
author_profile: true
sidebar:
  nav: docs
---

{% assign posts = site.categories.algospot %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}