---
layout: post
date: 2019-10-19
title: RoboJackets Software Training Week 5
tags: [RoboJackets, Software]
comments: false
---

# 5-01

## Lifetimes and rules
- After you create and before you destroy it
- Pointers and references do not change the lifetime
- Lifetime of pointer/reference should be contained by the object it references/points to

# 5-02

## unique pointer

```c
std::unique_ptr<int> x;  //created a null unique pointer
x = std::make_unique<int>(5); //pointed the pointer to 5
x = nullptr; //5 is destroyed, pointer set to null

//get data out of the scope
std::unique_ptr<int> x;
{
    std::unique_ptr<int> y = std::make_unique<int>(5);
    x = std::move(y); //move the x pointer to 5
}


## shared pointer
multiple component accessing the same object

```c
Component a;
Component b;
Component c;
Component d;

{
    std::shared_ptr<Logger> logger = std::make_shared<Logger>();
    a.setLogger(logger);
    b.setLogger(logger);
    c.setLogger(logger);
    d.setLogger(logger);
} //logger will get destroyed only when all a,b,c,d are all destroyed
```