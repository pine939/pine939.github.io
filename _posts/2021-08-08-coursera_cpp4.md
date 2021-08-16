---
title: "Object-Oriented Data Structures in C++ (4)"
excerpt: "Template"

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
date: 2021-08-08
last_modified_at: 2021-08-15
---

## Lecture

* url
  * https://www.coursera.org/learn/cs-fundamentals-1/home/week/4
* you can take this class if you sign up/in coursera.

## Summary

* oop design
* template
* class hierarchies and inheritance

## Lecture

### Template Types

* **Template Type** is a special type in c++ that can take on other different types when it is initialized.
* Template Type
  * we can initialize the template using "< >"
  ```cpp
  std::vector<char> c;
  std::vector<int> i;
  std::vector<uiuc::Cube> cube;
  ```

### Tower of Hanoi 

* skip

### Templates and Classes

* Template Functions 
  * template variable is defined by declaring it before the beginning of a class or function.
  ```cpp
  template <typename T>
  int max_test(T a, T b) {  // the type of a, b can be anything! 
    if (a > b) {
      return a;
    }
    return b;
  }
  ```

### Inheritance


## Graded Activities