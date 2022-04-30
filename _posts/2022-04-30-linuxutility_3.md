---
title: "[필수 유틸리티] Chapter 03. 컴파일과 링킹"
excerpt: "유닉스, 리눅스 프로그래밍 유틸리티 북러닝 요약입니다."

categories:
  - 'utility'
tags:
  - bookstudy
  - linux
  - utility

toc: true
toc_sticky: true
sidebar:
  nav: docs
date: 2022-04-30
last_modified_at: 2022-04-30
---

# Chapter 03. 컴파일과 링킹 

## Section 01. 컴파일의 의미 

* 사람이 작성한 고급 언어를 기계 언어로 번역하는 과정입니다.

## Section 02. 알아두면 정말 유용한 C 소스 컴파일 과정 

* 컴파일 과정을 이해 함으로써 컴파일 시 발생하는 문제 해결 능력을 기를 수 있습니다. 
* gcc 는 호출을 하고 실제 일은 전처리기(cpp0), 컴파일러(cc1), 어셈블러(as), 링커(ld, collect2) 바이너리들이 수행합니다.
* 전처리기 (.c --> .i)
* 컴파일러 (.i --> .s)
* 어셈블러 (.s --> .o)
* 링크 (.o --> 실행파일)

## Section 03. gcc를 사용해서 원하는 컴파일 하기

* 전처리기, 컴파일러, 어셈블러, 링커의 여러 옵션을 알아봅니다.

## Section 04. 라이브러리를 만들어 보자.

* 정적 라이브러리 만들기
* 동적 라이브러리 만들기

## Section 05. 바이너리 유틸리티 사용 

* objcopy, objdump 등 바이너리 유틸리티를 알아봅니다.

## Section 06. 인라인 어셈블리의 사용 

* __asm__volitile (blah,...) 간단한 어셈블리 문법을 알아봅니다.