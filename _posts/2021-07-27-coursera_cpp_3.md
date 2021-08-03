---
title: "Object-Oriented Data Structures in C++ (3)"
excerpt: "Lifecycle C++ object"

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
date: 2021-07-27
last_modified_at: 2021-07-27
---

### Summary

* study lifecycle cpp object by taking coursera class.
* lecture
  * https://www.coursera.org/learn/cs-fundamentals-1/home/week/3
  * if you want to take this class, you should sign up/in coursera.
* keyword
  * Constructors and Destructors
  * Methods and Operators
  * Access through pointers and references

### Lecture
#### 3.1 Class Constructors

* Automatic Default Constructor
  * Every class we've seen so far has a constructor.
  * It initialize all member variables to their default values.
* Custom Default Constructor
  * The simplest constructor.
  * It specifies the state of the object when the object is constructed.
  * A member function with the *same name of the class, taking zero parameters and no return type.*
* Custom Constructors
  * more fancy than default constructors.
  * allow user code to specify arguments.
* *If any custom constructor is defined, an automatic default constructor is not defined.*

### 3.2 Copy Constructors

* Automatic Copy Constructor
  * If you don't write custom copy constructor, c++ compiler provides an automatic copy constructor for your class.
  * It can copy the contents of all member variables.
* Custom Copy Constructor
  * It has exactly one argument.
    * *The argument must be const reference of the same type as the class.*
  ```cpp
  Cube::Cube(const Cube &obj)
  ```
  * Copy Constructor Invoke
    * Constructor Example
    ```cpp
    Cube() {
        std::cout << "default constructor invoked!" << std::endl;
    }
    Cube(const Cube & obj) {
        std::cout<< "copy constructor invoked!" << std::endl;
    }
    ```
    * Example 1
      * Code
      ```cpp
      void test(Cube cube) {
          // Nothing
      }
      int main() {
          Cube c;
          test(c);  // copy the obj through 'test' function.
          return 0;
      }
      ```
      * Result
      ```
      default constructor invoked!
      copy constructor invoked!
      ```
    * Example 2
      * Code
      ```cpp
      Cube test() {
          Cube c;
          return c;  // copy1
      }
      int main() {
          Cube c2 = test();  // copy2
          return 0;
      }
      ```
      * Result
      ```
      default constructor invoked!
      copy constructor invoked!
      copy constructor invoked!
      ```
    * Example 3
      * Code
      ```cpp
      int main() {
          Cube c;
          Cube myCube = c;
      }
      ```
      * Result
      ```
      default constructor invoked!
      copy constructor invoked!
      ```
    * Example 4
      * Code
      ```cpp
      int main() {
          Cube c;
          Cube myCube;
          myCube = c;
      }
      ```
      * Result
      ```
      default constructor invoked!
      default constructor invoked!
      ```
        * They've already been created by default constructor.
        * A constructor's job is to actually create the object itself.
        * we're just doing copying. (assignment)
        * So, there's no copy constructor.

### 3.3 Copy Assignment Operator

* Custom Assignment Operator
```cpp
Cube & operator=(const Cube &obj)
```
  * It is a public function of the Class.
  * It has the name *"operator="*
  * It has a return value of reference of class type.
  * It has exactly one argument

### 3.4 Variable Storage

* Every variables are stored ...
```
directly in memory,
accessed via a pointer,
or accessed by a reference.
```
* Direct Storage
  * The type, size of a variable has no modifiers.
* Storage by Pointer
  * The type of a variable is modified with an asterisk (*).
  * A pointer takes a "memory address width" of memory. (by your system)
  * The pointer "points" to the allocated space of the object. 
* Storage by Reference
  * A reference is a special type of variable which **aliases** existing memory by name.
  * A reference **does not store memory itself(It takes zero bytes of memory to create a reference variable)**, it is only an alias to another variable.
  ```
  * It is denoted by the type with an ampersand(&).


## Reading

## Graded Activities