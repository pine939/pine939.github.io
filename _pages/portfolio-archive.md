---
title: Portfolio
layout: single
permalink: /portfolio/
author_profile: true
sidebar:
  nav: docs
---

## Skill

* Programming Language
  * C
  * C++
  * Python
* OS
  * Linux
* SCM
  * Git
* ITS
  * Redmine

## Work Experience

| Time | Company | Job Position | Description |
| --- | ----- | -----| ----- |
| 2018.01 ~ Current | <a href="http://wins21.com/main/main.html">Wins</a> | Software Deveoper | 정보보호 소프트웨어(IPS, ESM) 연구개발 업무|
| 2017.07 ~ 2017.08 | <a href="http://www.thinkware.co.kr/">Thinkware</a> | Software Developer (Intern) | 네이게이션 검색 성능 연구 |

## Project

<table>
    <tr>
        <th> Time </th>
        <th> Company </th>
        <th> Skills </th>
        <th> Title </th>
    </tr>
    {% for portfolio in site.portfolio reversed %}

    {% if portfolio.categories contains "project" and portfolio.categories.size == 1 %}
    <tr>
        <td>{{ portfolio.time }}</td>
        <td>{{ portfolio.company }}</td>
        <td>{{ portfolio.skills | join: ", " }}</td>
        <td>
            {% assign content = portfolio.content | strip_newlines %}
            {% if content != ""  or portfolio.redirect_to %}
                <a href="{{ portfolio.url }}">{{ portfolio.title }}</a>
            {% else %}
                {{ portfolio.title }}
            {% endif %}
        </td>
    </tr>
    {% endif %}
    {% endfor %}
</table>

## Education

* 2013 ~ 2018, B.S in Computer Engineering at University of MyongJi, Yongin, Korea

## Etc

* 정보처리기사
* 리눅스 마스터 2급