---
layout: post
date: 2019-09-21
title: RoboJackets Software Training Week 2
tags: [RoboJackets, Software]
comments: false
---

# 2-01 Header Files and Includes
- Use angled brackets <...> for header files that come with the compiler
- Use double quotes for user defined header files
```c
#include <iostream>
#include "data.h"
```

## Header File
- Give header file the same name as their files
- Do not include cpp file
- Do not include unnecessary header files
- Components
    - Header guard
    - Includes
    - Declarations of global variables, functions, etc.

### Header guards
Prevent compile errors for duplicate definitions (pragma once)
```c
//some_file.h
#pragma once

//your code here
```


# 2-02 Declaration
Declaration - a function exists somewhere
- Declaration for functions - tells compiler what the function does
- Declaration for variables - tells compiler where the variable is stored

- Multiple occurance
 - Multiple DECLARATION is fine
 - Multiple DEFINITION is not

Initialization
- seperate from declaration and definition
- Provides the variable with its initial value
- Not initialized = indeterminate value


# 2-03 Scope and Namespace
```c
namespace name_of_namespace{

}

int main(){
    std::cout << name_of_namespace.something << std::endl;
}
```

Name space can be nested
```c
namespace my_namespace{
    namespace space2{
        
    }
}

int main(){
    std::cout << my_namespace::space2::something << std::endl;
}
```


# 2-05 C++ Encapsulation
```c
class Example{
    public:
        Example()
            : example_data_1(4),  //Member initialization list
                example_data_2(5.6);
        Example(int data_1)
            : example_data_1(data_1)
                example_data_2(data1 + 1.6)
        {

        }
        

        int example_data_1;
        double example_data2;
};

int main(){
    Example e1;   //Constructor will be called IFF there is a default constructor
    Example e2 = Example(2);
    Example e3 = Example();
}
```

Destructor
- called the object is destroyed
- Clean up anything the object was using

```c
class Example{
    public:
        ~Example(){   //Destructor

        }
}
```


# 2-06 Undefined Behavior
```c
int main(){
    int x;
    std::cout << x << std::endl; //x is not intialized
}
```

Undefined Behavior
- Crash your program
- Give garbage (meaningless result)
- Work exactly as you expect
 