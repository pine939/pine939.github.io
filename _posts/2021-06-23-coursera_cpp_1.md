---
title: "Object-Oriented Data Structures in C++ (1)"
excerpt: "Introduction, Class, STD"

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
date: 2021-06-23
last_modified_at: 2021-07-02
---

## Summary

* Lecture
  * https://coursera.org/share/e8050dce1663013e44c5be982086249a
* 1.1 Introduction
* 1.2 Classes
* 1.3 Standard Library (std)

## Contents
### 1.1 Introduction

* skip

### 1.2 Classes

* skip

### 1.3 Standard Library (std)

* A set of commonly used functionality and data structures to build upon.
* It's somtimes called the c++ standard template library (stl).
* It's divided up into a number of separate files, and we make use of them by including them in any of out c++ programs.

#### Standard Library Organization

* All functionality used from the std will be part of the std namespace.
  * namespace allow us to avoid name conflicts for commonly used names.
* it can be imported into the global space with "using":
  ```cpp
  using std::cout
  ```
  * we can convert typing std cout into just typing cout.

#### Using uiuc namespace

* we have encapsulated the Cube class into the uiuc namespace.
* add curly brace, and we're going to do that inside of both header and the cpp file.

### Quiz

* A class can consist of multiple member data variables of different types, but each type must be specified when the class is defined.
* Even if the functions are declared in the class and implemented in a separate .cpp file, they are still part of the class. 
* Namespaces allow different libraries to use the same label for a class or variable because they can each define a unique namespace to differentiate them when they are used together in a program.

### Challenge

* skip