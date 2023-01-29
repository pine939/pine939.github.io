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
| 2022.05 ~ |<a href="https://www.ahnlab.com/kr/site/main.do">Ahnlab</a>| Software Developer | 정보보호 소프트웨어(EDR) 연구개발 |
| 2018.01 ~ 2022.04 | <a href="http://wins21.com/main/main.html">Wins</a> | Software Deveoper | 정보보호 소프트웨어(IPS, ESM) 연구개발 업무|
| 2017.07 ~ 2017.08 | <a href="http://www.thinkware.co.kr/">Thinkware</a> | Software Developer (Intern) | 네이게이션 검색 성능 연구 보조 |

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

* Google Developers Machine Learning Bootcamp
  * [program url](https://events.withgoogle.com/google-developers-mlb-kr-2021/)
* Object-Oriented Data Structures in C++
  * [certificate](https://coursera.org/verify/74Z7YA3QY8HE)
* 리눅스 마스터 2급
* 정보처리기사