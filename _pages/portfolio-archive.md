---
title: PORTFOLIO
layout: collection
permalink: /portfolio/
author_profile: true
sidebar:
  nav: docs
---

## Skill
---

* Programming Language
  * C
  * C++
  * Python
* OS
  * Linux
* SCM
  * Git, Bitbucket
* ITS
  * Redmine

## Work Experience
---

| Time | Company | Job Position | Description |
| --- | ----- | -----| ----- |
| 2018.01 ~ Current | Wins | Software Deveoper | 정보보호 소프트웨어(IPS, ESM) 연구개발 업무|
| 2017.07 ~ 2017.08 | Thinkware | Software Developer (Intern) | 네이게이션 검색 성능 연구 |

## Project
---

<table>
    <tr>
        <th> Title </th>
        <th> Company </th>
        <th> Skills </th>
        <th> Time </th>
    </tr>
    {% for portfolio in site.portfolio reversed %}

    {% if portfolio.categories contains "project" and portfolio.categories.size == 1 %}
    <tr>
        <td>
            {% assign content = portfolio.content | strip_newlines %}
            {% if content != ""  or portfolio.redirect_to %}
                <a href="{{ portfolio.url }}">{{ portfolio.title }}</a>
            {% else %}
                {{ portfolio.title }}
            {% endif %}
        </td>
        <td>{{ portfolio.company }}</td>
        <td>{{ portfolio.skills | join: ", " }}</td>
        <td>{{ portfolio.time }}</td>
    </tr>
    {% endif %}
    {% endfor %}
</table>

## Etc
---

* 정보처리기사
* 리눅스 마스터 2급
