---
layout: single
time: "2016.10 ~ 2016.11"
title: "OpenDNS API를 사용한 악성 사이트 방어 프로그램"
skills: [C, Python, PHP, HTML, CSS, JQuery]
company: "-"
categories: [project]
author_profile: true
sidebar:
  nav: "docs"
---

## 개요

* 정보보호 해커톤 출전작

## 기술

* Language
  * C, Python, PHP, HTML, CSS, JQuery
* Environment
  * Amazon EC2 Linux
  * Apache Web Server
* Tools
  * Cisco OpenDNS API
  * Geolocation: MaxMind API
  * Visualization: ZingChart, Leaflet

## 역할

* DNS Packet에서 IP와 요청 도메인 정보 추출 
* OpenDNS API 결과값을 분석하여 악성 사이트를 판별하는 로직 설계 및 구현
  * attack, threat_type, securerank2, dga_score값 등을 추출
* 악성 사이트 정보 시각화 
  * MaxMind API를 사용하여 서버 위치 표기
  * Free Visualization Tools를 사용하여 악성 도메인 통계정보 표기