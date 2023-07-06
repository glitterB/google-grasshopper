# Fundamentals II

Contents 

[1. String Manipulation](#string-manipulation)  
[2. Alternative Options](#alternative-options)  
[3. Functions](#function)  
[4. Array Manipulation](#array-manipulation)

------------------------------------------------------------
## String Manipulation  
String manupulation involves finding length of the string, searching inside and replacing elements of strings.

- *`.length`* :- This property is used To find length of the String (spaces and symbols included).
``` js
var str = "JavaScript";
console.log(str.length); //10
```
- *`.includes(arg)`* :- This method is used to search for specific value in the string.
``` js
var str = "I Love JavaScript";
if (str.includes('Love')){
    console.log('YES'); // YES
}
```
- *`.replace(arg1, arg2)`* :- Thsi method is used to replace a value, where *`arg1`* is value which is searched within a string and is replaced with *`arg2`*.
``` js
var str = "I Love JavaScript";
str.replace("JavaScript","Python");
console.log(str) // "I love Python"
```

---------------------------------------------
## Alternative Options
In `JavaScript`, there are various alternative approaches, such as while defining a variable, etc.

- Variable Scope :-
`JavaScript` has two types of variables, *GLOBAL* and *LOCAL*. The Scope of a variable is the section of code where it can be used. A *`let`* can be used for declaring a local variable where as *`var`* is used to declare a global variable.
``` js
var x = 100;
if (x>0){
    let x = 25;
}
console.log(x); //100
```
Since the *`x`* inside the block of *`if`* statement is declared using *`let`* keyword, hence it is a local variable. The *`console.log`* statement will print `100` because it is outside of code block and used *`var x = 100`*.

- Ternary Operator :- Ternary operator used a question mark *`?`* and a colon *`:`* to replace entire *`if ... else`* statement, with single line of code.
``` js
let x = 100;
if (x==100){
    console.log("Century!");
}
else{
    console.log("Not Yet");
}
//equivalant ternary opetaror
x==100 ? console.log("Century!") : console.log("Not Yet");
```
-------------------------------------------------
## Function
A function saves a block of code. We can run it whenever we reference the function's name. The code inside *`{ }`* will run when the function's name is called. Function is defined with a keyword *`function`* followed by function's name. Function may have a *`return`* keyword which tells function to stop executing and return a value.
``` js
function half(n){
    //this function will return
    //the half value of input number (n)
    return n/2;
}
```
Creating a function is called as **Function Declaration** and we use Parameters.[^1] A function will not run unless used and this is known as **Function Call** using Arguements.[^2] A function can be called inside another function.
- Recursion :- Recursion function is the function that call itself, enabling the function to fun again. This makes function work like loops. Function will keep calling itself untill the end condition is met.
``` js
function facto(n){
    /*
    This is a function which calculates
    Factorial of the input number using recursion
    */

    if (n<=1){
        return 1;
    }
    return n*facto(n-1);
}
```

---------------------------
## Array Manipulation
Array maniplation are used to extract data, update elements and use array methods with **Callback Functions**.[^3]

- *`.length`* :- This property of an array will count total number of items in an array.
``` js
var color = ['red','green','blue']
console.log(color.length) //3
```
- *`.slice(arg1, arg2)`* :- This method of an array will create a new array by copying a subset of another array. It takes 2 arguement, `arg1`: an array index where to start copying and `agr2` : an index where to end (*end excluded*).
``` js
var color = ['red','green','blue']
console.log(color.slice(0,2))
//The output - 'red','green'
```

- *`.push(arg1)`* :- This method adds an element (*`arg1`*) at the end of the array.
``` js
var colors = ['red','green','blue']
colors.push('black')
console.log(colors)
//The output - ['red','green','blue','black']
```
- *`.pop()`* :- RThis method removes an element from the end of the array and returns it.
``` js
var colors = ['red','green','blue']
last = colors.pop()
console.log(colors)
//The output - ['red','green']
console.log(last) //'blue'
```

- Copying all the elements from an array :- `JavaScript` has a special operator *`. . .`* which copies all the elements form an array to another array.

``` js
var colors = ['red','green','blue']
var newColors = [...colors, 'black','brown','violet']
console.log(newColors);
//The output - ['red','green','blue','black','brown','violet']
```

- *`.filter()`* :- This method is used to select items of an array that passes certain test. Each array element is used as arguement in callback function,[^3] and if it returns true, the item passes the filter. Otherwise, item will be filtered out.
``` js
function even(n){
    if (n%2==0){
        return true
    }
    return false
}
arr = [1,2,3,4,5,6,7,8,9,10]
console.log(arr.filter(even))
// [2,4,6,8,10]
```
- *`.forEach()`* :- This method loops through each element in an array and uses it as an arguement for specified callback function.[^3] (*Note: `.forEach()` method does not return a new array*)
``` js
function even(n){
    if (n%2==0){
        console.log('Even')
    }
    else{
        console.log("Odd")
    }
}
arr = [1,2,3,4]
console.log(arr.forEach(even))
/*
OUTPUT:-
Odd
Even
Odd
Even
*/
```
---
---
[^1]: A parameter is a variable in a function definition. It is a placeholder and hence does not have a concrete value.  
[^2]: An argument is a value passed during function calling.  
[^3]: When a function is passed as an arguement is a Callback Function.
