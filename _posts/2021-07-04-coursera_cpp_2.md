---
title: "Object-Oriented Data Structures in C++ (2)"
excerpt: "Pointer, Memory"

categories:
  - 'cpp'
tags:
  - coursera
  - lecture
  - oop

toc: true
toc_sticky: true
sidebar:
  nav: docs
date: 2021-07-04
last_modified_at: 2021-07-19
---

## Summary

* study by lecture and some articles.
* lecture url
  * https://www.coursera.org/learn/cs-fundamentals-1/home/week/2
  * (if you want to take this class, may be you need to sign in)
* main topic
* Pointers and dereferencing
* Local (stack) memory
* Allocated (heap) memory

## Lectures
### 2.1 Stack Memory and Pointers
### 2.2 Heap Memory
### 2.3 Heap Memory Puzzle

* 완강! 간단한 내용이지만 7/21 정리 예정

## Readings

* Making Comments in C++ Code
  * too easy but very important.
* Headers and Source Files
  * .h 
  ```c++
  #pragme once
  class test {
    public:
      double test_volume();
      double get_length();
      void set_length(double l);
  };
  ```
    * Note *the #pragma once* at the begining.
    * Instructions begining '#' are special commands for compiler, called *preprocessor directives*.
    * this instruction(pragma once) prevents the header file from being included multiple times in some projects, which would cause errors.
  * .cpp
    * implementation files.
    * Include directives insert the headers.
    * *Compiler* generates object files.
    * *Linker* combines file into an executable.
    