---
layout: post
date: 2019-09-22
title: RoboJackets Software Training Week 1
tags: [RoboJackets, Software]
comments: false
---

# 1-01 Work with Data

- Static type checking - you cannot change the data type after its declaration
- The "auto" keyword
    ```c
    auto my_variable = 1;
    ```
    the commputer will automatically determine the data type and in this case, int


# 1-03 Pratical Functions

- Main function that serves as the entrance to the function
    ```c
    // file scope (only declarations allowed)

    double percentageAOfTotal(int part_a, int part_b){
        return (part_a * 100.0) / (part_a+part_b);
    }

    int main(){
        return 0
    }
    ```


# 1-04 Terminals

- std::cout
```c
std::cout << "Hello, world!" << std::endl;
```