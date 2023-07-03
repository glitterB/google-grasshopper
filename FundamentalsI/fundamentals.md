# Fundamentals I

Contents 

[1. String](#string)  
[2. Variables](#variables)  
[3. Array](#arrays)  
[4. Variables](#variables) 

---
   
## String  
A string is a type of data in `JavaScript`, which is used to represent characters (*or words or sentences*).  
For ex.
```js
   "This is string"
   "A string"
   "To be or not to be; that is a question."
```   
A string is represented in single (*' '*) or double (*" "*) quotes.

---

## Variables
Variables allow us to reference the same piece of information multiple times. In `JavaScript`, variables can be defined using **var** and then giving a unique name.   
For ex.
``` js
var x = 10;
var name = "JavaScript";
```
We can reassign value of variable. When reassigning a variable, the **var** is not necessary.  
For ex.
``` js
x = 110;
name = "JavaScript is awesome";
```
Sometimes, variables can be assigned to other variables  
For ex.
``` js
x = 110;
y = x;
```
The variable y is given a value 110 since x is assigned with 110.

---

## Arrays
In `JavaScript`, an array is a list of items. The items can be different data types (*int, float, string, other array etc.*). An array inside another array is called array nesting.  
For ex.
``` js
var colors = ["red","green","blue","black"]
```