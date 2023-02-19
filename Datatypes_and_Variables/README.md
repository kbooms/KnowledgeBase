# Datatypes and Variables

## What we will learn
- A basic overview of a Java program
- How to display basic output
- Some of the primitive data types used to store program data in variables
- How variables are declared and used in code

*please see glossary of terms at the end for more information*

## A brief overview of Variables
Typical programs like web applications need to store and manipulate data.  
Variables have three characteristics:  
- A variable must identify what **type of data** it stores
- A variable must be declared before it's used
- A variable must be given a unique name
  
We've mentioned already that variables must be declared, but it also must have data initialized within it before it can be used.  
  
Declaring a variable `Datatype variableName;`  
Initializing data `variableName = initialData;`  
  
However variable can be declared and initialized on the same line  
Example code format `Datatype variableName = someData;`
  
## Data types
Every variable, when created, is defined with a data type. The data type classifies the variable and indicates the particular type of data that a particular variable holds.  
In Java, there are two classifications of data types: **primitive** and **reference** data types. Primitive data types store values such as `42`, `true`, or `a`. These data values consume a fixed amount of memory. A reference type stores complex data, such as entries in an address book, or product inventory in a computer system.  
*We'll learn more about reference variables in a later lesson. For now we will focus on primitive types.*  

Here are the 8 primitive datatypes supported by Java Language, as well as the range of data they may contain  

| Datatype | Range |
| ------------ | ------------ |
| `boolean` | `true` or `false` |
| `byte` | -128 to 127 **or** -2<sup>7</sup> to 2<sup>7</sup>-1 |
| `short` | -32,768 to 32,767 **or** -2<sup>15</sup> to 2<sup>15</sup> -1 |
| `int` | -2,147,483,648 to 2,147,483,647 **or** -2<sup>31</sup> to 2<sup>31</sup>-1 |
| `long` | -2<sup>63</sup> to 2<sup>63</sup>-1 |
| `float` | -3.4 x 10<sup>38</sup> to 3.4 x 10<sup>38</sup> |
| Key_ | Value_ |
| Key_ | Value_ |