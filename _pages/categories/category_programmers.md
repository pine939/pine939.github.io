---
title: "Programmers"
layout: archive
permalink: categories/programmers
author_profile: true
sidebar:
  nav: docs
---

{% assign posts = site.categories.programmers %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}