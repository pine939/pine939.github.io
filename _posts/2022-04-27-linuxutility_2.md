---
title: "[필수 유틸리티] Chapter 02. VIM"
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
date: 2022-04-27
last_modified_at: 2022-04-27
---

# Chaper 02. VIM

### Section 01 ~ Section 03 vim 기본 

* 이동
  * 단어 단위 이동 : **w, b**
  * 문단 단위 이동 : **{, }**
  * 행의 시작과 끝 : **^, $**
  * 문서의 시작과 끝 : **gg, G**
* 삭제
  * 한 단어 삭제 : **dw**
* 잘라내기
  * vim에서 문자열을 잘라내면 17개의 레지스터에 차곡차곡 저장됩니다.
  * 레지스터 값 보기 : **:reg**
* 블록 지정
  * 행 앞에 탭 삽입 : **>**
  * 행 앞에 탭 제거 : **<**
* 문자열 치환
  * 문서 전체에서 old를 new로 치환 : **:%s/old/new/g**
  * 문서 전체에서 old를 new로 확인하며 치환 : **:%s/old/new/gc**

* 정규 표현식 
* 여러 파일의 편집
  * vim에서 여러 파일을 동시에 열면 버퍼에 파일들을 저장합니다.
  * 편집 버퍼 보기 : **:buffer**
  * b1, b2, ... 로 버퍼를 이동할 수 있습니다.
  * 보통 .vimrc에 map으로 저장하여 사용합니다.
* 반복되는 문자열 저장해서 쓰기
  * vim에서는 앞의 17개 레지스터 외 a-z까지 26개의 네임 레지스터를 제공합니다.
  * 반복되는 문자열을 이 레지스터에 저장하여 사용할 수 있습니다.
  * a레지스터에 3줄 복사 : **"a3yy**
  * a레지스터에 저장된 내용 붙여넣기 : **"ap**
* 마킹
  * 마킹할 때 : **m[임의의 알파벳]**
    * 전역 마킹(A-Z) : 현재 파일을 포함한 다른 파일 간의 마킹이 가능합니다.
    * 지역 마킹(a-z) : 현재 파일 내에서만 마킹이 가능합니다.
  * 마킹한 위치로 돌아갈 때 : **`[마킹한 알파벳]**
  * 마킹 정보 보기 : **:marks**
* 쉘 명령어 이용하기
  * **:![명령어]**
* 자동 완성
  * **ctrl + p**
  * **ctrl + n**

  ### Section 04. ctags, cscope, 기타 플러그 인

  * ctags 
    * 프로그래밍 소스 코드 태그들의 데이터베이스(tags)를 생성하는 유닉스 명령입니다.
    <pre>
    ctags -R
    </pre>
    * vim에서 set 명령어로 tags 파일 경로를 설정할 수 있습니다.
    <pre>
    :set tags=./tags,/usr/tags
    </pre>
    * tj(tag jump) 명령어로 tags 파일에서 코드를 검색할 수 있습니다.
    <pre>
    :tj start_kernel
    </pre>
* cscope 
  * 지역변수, 전역변수, 함수가 사용된 곳을 알 수 있는 소스 분석 프로그램입니다.
  * **cscope.files** 에 파일 리스트를 만들고, **cscope -i cscope.files** 명령어로 **cscope.out**(cscope 심볼 데이터베이스)를 만듭니다.
  * cs 명령어로 cscope를 사용할 수 있습니다.
  <pre>
  : cs find [질의 종류] [심볼]
  : cs find s start_kernel  # Find this C Symbol
  : cs find g start_kernel  # Find thid definition
  : cs find d start_kernel  # Find functions called by this function
  : cs find c start_kernel  # Find functions calling this function
  </pre>
* Plugin
  * https://www.vim.org/scripts/index.php 에서 다운로드 받아 사용할 수 있습니다.