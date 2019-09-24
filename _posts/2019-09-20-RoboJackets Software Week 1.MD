---
layout: post
date: 2019-09-20
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

- std::cout (need #include <iostream>)
    ```c
    //set precision to the output if precision is NEEDED
    std::cout << std::setprecision(10);
    //set precision to the output if precision might NOT be NEEDED
    std::cout << std::setprecision(10) << std::fixed;
    //print out Hello World
    std::cout << "Hello, world!" << std::endl;
    ```


# 1-05 Control  statements

- Jump statement
    - break - break the loop and exit
    - continue - skip the iteration 


# 1-06 C++ objects

Object - group together data and behavior

- instance declaration
    ```c
    SimPerson p1 = SimPerson();
    ```
- access instance elements
    ```c
    p1.eat();
    p1.hunger;
    ```

# 1-07 Running the program

- g++ command generate the executable binary file
- Errors
    - Runtime error and compilation error
    - Runtime error will not report error but give out weird results
