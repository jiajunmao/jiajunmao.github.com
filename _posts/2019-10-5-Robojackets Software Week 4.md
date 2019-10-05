---
layout: post
date: 2019-10-05
title: RoboJackets Software Training Week 4
tags: [RoboJackets, Software]
comments: false
---

# 4-01 References

Indirection - multiple name for the same piece of data
 - Diffrent handles pointing to the same data
 - Any read/write change will change the data returned for all the handles

 ```c
 int my_data = 10;
 int& my_reference = my_data; //must initialize during declaration
 ```

 Dangling Reference - the object is destroyed before the reference is destroyed
 ```c
 std::string& f(){   //returning a reference to the data, in this case it refers to the s in the function
     std::string s = "Example";
     return s;
 }

 std::string& r = f();  //when the line is run, it will compile. But after initialization, scope f is cleaned up and f is destroyed

 std::cout << r:  //COMPILE ERROR
 ```

 # 4-02 Pointers

Pointer
 - Mutability (you can change where it is pointing to)
 - Nullability (can point to nothing)

```c
int real_variable = 10;
int* point_variable = &real_variable;  //pointer to an int
(*pointer_variable) += 5;  //indrect operator
std::cout << (*pointer_variable) << std::endl;

(*my_object_pointer).my_function();  //equivalent
my_object_pointer -> my.function();  //equivalent

my_pointer == nullptr;  //nullptr constant
```

Pointer to your own class or struct
```c
int MyType::* ptr_to_member = &MyType::member_name;  //point to a int member of MyType
MyType my_instance;
std::cout << my_instance.*ptr_to_member << std::endl;
```

Pointer to a function
```c
int(*ptr_to_function) (int arg1, int arg2);
int f(int a, int b) { return a+b; }

ptr_to_function = &f;  //point to f
```

# 4-03 Const

Const - mark something as constant and immutable

```c
const int * u1;  //VARIABLE pointer to a CONSTANT integer
int const * u2;  //VARIABLE pointer to a CONSTANT integer
int * const u3;  //CONSTANT pointer to a VARIABLE integer
int const * const u4;  //CONSTANT pointer to a CONSTANT variable
const int * const u5;  //CONSTANT pointer to a CONSTANT variable
```

Constant functions
```c
int change_variable() const;  //means that no variable can be changed in the scope of the function
int change_variable(const int z);  //means that you cannot change z in the scope of the function
```

Constant object
```c
const MyType something;  //means that the object cannot change its member varialbe

//But if variable declared mutable, then const object can change its member variable

class MyType
{
    mutable int j;
}
```

