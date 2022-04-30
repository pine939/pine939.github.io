---
title: "오픈소스 프로젝트"
layout: archive
permalink: categories/opensource
author_profile: true
sidebar:
  nav: docs
---

{% assign posts = site.categories.opensource %}
{% for post in posts %} {% include archive-single.html type=page.entries_layout %} {% endfor %}