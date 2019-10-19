---
layout: post
date: 2019-10-03
title: RoboJackets Software Training Week 3
tags: [RoboJackets, Software]
comments: false
---

# 3-01 Basic Containers and Arrays
```c
std::array<int, 5> my_init_array; //an array of length 5, data type of int
my_init_array = {};  //initialize an empty array
```
cannot use variable as the length during declaration
```c
my_init_array.at(8);  //will throw an exception but will not crash the program
my_init_array.size();  //will return the length of the array
```

## Vectors
```c
std::vector<datatype> var_name; //does not have fixed size

var_name.push_back(element);  //put the element at the start of the array
```

# 3-02 Maps

```c
std::map<std::string, int> number_representations;  //declare a map
number_representation = {{std::string, int}, {..., ...}};  //initialize the map

number_representation["something"].first;  //return the string key
number_representation["something"].second;  //return the integer value

number_representation["something"];  //If "something" does not exist, it will not throw an error, and insert the key into the map with default value of 0
number_representation.at("something");  //If "something" does not exist, it crash your program

number_representation.count("something");  //Count the occurance of "something" key in the map
```

# 3-04 STL Iterators

```c
std::vector<int> my_vector = {1,2,3,4,5};
for(auto it=my_vector.begin(); it!=vector.end(); it++){
    // This create an iterator that will loop through my_vector
}
```