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
last_modified_at: 2021-07-20
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

* Variable
  * Every c++ variable has four things
  ```
  name
  type
  value
  location in memory (memory address)
  ```
* Stack Memory
  * By default, every variable in C++ is located in *Stack Memory*
  * The stack memory's lifecycle is tied to the function. (*Stack Frame exists only so long as the function is running.*)
  * The stack memory grows down toward zero.
  * The memory address in your computer, they are going to be different because the layout of memory is might different as randomized.
* Pointer
  * It's a variable that stores the memory address of data.
  * given a pointer value, a level of indirection can be removed with dereference operator '*'.
  ```cpp
  int num = 5;
  int *p = &num;
  int value_in_num = *p;
  *p = 40
  ```
  *  Be sure to initialize variables and do not access addresses to invalid memory.

### 2.2 Heap Memory
### 2.3 Heap Memory Puzzle

* 완강! 간단한 내용이지만 7/21 정리 예정

## Readings

* Making Comments in C++ Code
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
* Compiling and Running a C++ Program    
* Useful Bash Terminal Commands
* C++ Syntax Notes : If-Else, Type Casting 
  * [refer 1](http://www.cplusplus.com/doc/tutorial/typecasting/)
  * [refer 2](https://en.cppreference.com/w/cpp/language/implicit_conversion)
* C++ Syntax Notes : Block Scope, loops
