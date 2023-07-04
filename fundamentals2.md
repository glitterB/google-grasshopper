# Fundamentals II

Contents 

[1. String Manipulation](#string-manipulation)  
[2. Alternative Options](#alternative-options)  
[3. Functions](#function)  
[4. Array Manipulation](#array-manipulation)

------------------------------------------------------------
## String Manipulation  
String manupulation involves finding length of the string, searching inside and replacing elements of strings.

- Finding length of the string :- String has property *.length*, which is used to find it's length (spaces and symbols included).
``` js
var str = "JavaScript";
console.log(str.length); //10
```
- Searching for specific value :- String has method *.includes()*, which is used to search for specific value (subset) in the string.
``` js
var str = "I Love JavaScript";
if (str.includes('Love')){
    console.log('YES');
}
```
- Replacing a value :- String has method *.replace(arg1, arg2)*, which is used to replace *arg1* with *arg2*, where *arg1* is value which is searched within a string and is replaced with *arg2*.
``` js
var str = "I Love JavaScript";
str.replace("JavaScript","Python");
console.log(str) // "I love Python"
```

---------------------------------------------
## Alternative Options
In `JavaScript`, there are various alternative approaches, such as while defining a variable.

- Variable Scope :-
`JavaScript` has two types of variables, *GLOBAL* and *LOCAL*. The Scope of a variable is the section of code where it can be used. A *let* can be used for declaring a local variable where as *var* is used to declare a global variable
``` js
var x = 100;
if (x>0){
    let x = 25;
}
console.log(x); //100
```
since the x inside the block of *if* statement is declared using *let* keyword, hence it is a local variable. The *console.log* statement will print 100 because it is outside of code block and used *var x = 100*.

- Ternary Operator :- Ternary operator used a question mark *?* and a colon *:* to replace entire *if ... else* statement, with single line of code.
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
A function saves ablock of code. We can run it wheneve we reference the function's name. The code inside *{ }* will run when the function's name is called. Function is defined with a keyword *functoin* followed by function's name. Function may have a *return* keyword which tells function to stop executing and return a value.
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








[^1]: A parameter is a variable in a function definition. It is a placeholder and hence does not have a concrete value.  
[^2]: An argument is a value passed during function calling.  
[^3]: When a function is passed as an arguement is a Callback Function.
