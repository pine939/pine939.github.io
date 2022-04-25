---
title: "[필수 유틸리티] Chapter 01. 튜토리얼"
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
date: 2022-04-25
last_modified_at: 2022-04-25
---

* 리눅스 환경에서 프로그램을 개발할 때, 기본적으로 필요한 유틸리티를 정리한 도서입니다.
* 해당 장 에서는 프로그램 작성부터 배포까지 주로 어떤 유틸리티를 사용하는지 알아봅니다. 
* 이후 공부할 장 들에서 자세한 내용을 확인할 예정입니다.

# Section 01. 간단한 소스 프로그램 작성 

* **vi(vim) 편집기**를 이용해 프로그램을 작성할 수 있다.

# Section 02. gcc로 컴파일하여 실행 파일 생성

* **gcc** 컴파일러를 사용해 컴파일 할 수 있다.
<pre>
gcc -W -Wall -O2 -o like like.c
gcc -W -Wall -O2 -o like like.c love.c  // 새로운 소스코드를 추가하여 컴파일 할 수 있다.
gcc -W -Wall -O2 -o like like.c love.c -lm  // 라이브러리를 링크할 수 있다.
</pre>

# Section 03. make를 사용한 프로젝트 관리 

* gcc 컴파일러 명령어를 자동화 시키는 **Makefile**을 작성할 수 있다. 
<pre>
CC        = gcc
CFLAGS    = -W -Wall -O2
LDFLAGS   = -lm

like : like.c love.c
  $(CC) $(CFLAGS) -o $@ $^ $(LDFLAGS)

clean : 
  @rm -rf *.o like
</pre>

# Section 04. 문제 발생, 벌레를 잡아라

* **gdb**를 사용하여 프로그램의 문제점을 찾아낼 수 있다. 
<pre>
info f name  // name 변수의 주소 값을 알아낼 수 있다.
x/s 알아낸 주소  // p name 과 동일. 알아낸 주소에 저장된 값.
</pre>

# Section 05. 국제화와 다국어 지원

* gettext를 사용해 프로그램 입/출력을 다양한 언어로 구성할 수 있다.

# Section 06. 프로젝트 관리 

* 다수의 개발자들과 프로젝트를 관리하기 위해 **git,cvs** 등을 사용할 수 있다.

# Section 07. autotools를 사용한 이식성 높은 빌드 

* **autotools(autoconf, automake)** 을 사용해 환경이 달라도 편리하게 빌드할 수 있다.

# Section 08. RPM 패키징 

* 소스코드를 배포하지 않고, 바이너리 패키지 형태로 사용자들이 손쉽게 프로그램을 사용할 수 있도록 한다.