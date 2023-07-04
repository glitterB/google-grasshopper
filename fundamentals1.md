# Fundamentals I

Contents 

[1. String](#string)  
[2. Variables](#variables)  
[3. Array](#array)  
[4. Conditional Statement](#ifelse)  
[5. Operators](#opers)  
[6. Loops](#loops)  
[7. Object Expression](#obj)

------------------------------------------------------------
## String  
A string is a type of data in `JavaScript`, which is used to represent characters (*or words or sentences*).  
For ex.
```js
   "This is string"
   "A string"
   "To be or not to be; that is a question."
```   
A string is represented in single (*' '*) or double (*" "*) quotes.

--------------------------------------------------------
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

-------------------------------------------------------
## <span style="color:red" id='array'>Arrays</span>
In `JavaScript`, an array is a list of items. The items can be different data types (*int, float, string, other array etc.*). An array inside another array is called array nesting.  
For ex.
``` js
var colors = ["red","green","blue","black"]
```
To access elements of an array, we use **Indexing**. An array is indexed fron 0. 1st element has an index 0.  
For ex.  
colors[0] accesses 1st element (*i.e. "red"*)

------------------------------------------------------------
## <span style="color:blue" id='ifelse'>Conditional Statement</span>
Conditional statement allows us to run a specific section of code when a test is true. The code inside parenthese ie ( ) is the test. If the test is true, then the code inside block { } runs. Otherwise, code will not run.
``` js
var x = 10;
if (x==10){
   console.log(x);
}
```

We can use multiple *if* statements. We can also use *if..else* statement, which allows us to control which code runs when test is true, and what code runs when the test is false.
``` js
var x = 10;

if (x==10){
   console.log(x);
else if (x==5){
   console.log(x*2);
}
else{
   console.log("Invalid!")
}
}
```

-------------------------------------------------------
## <span style="color:red" id='opers'>Operators</span>
<table>

   <tr>
    <th>Operator Category</th>
    <th>Operator Syntax</th>
    <th>Desctiption</th>
  </tr>

  <tr>
    <td>Mathematical</td>
   <td>
   <table>
   <tr><td>+<td></tr>
   <tr><td>-<td></tr>
   <tr><td>*<td></tr>
   <tr><td>/<td></tr>
   <tr><td>++<td></tr>
   <tr><td>--<td></tr>
   </table>
   </td>

   <td>
   <table>
   <tr><td>Addition<td></tr>
   <tr><td>Subtarction<td></tr>
   <tr><td>Multiplication<td></tr>
   <tr><td>Division<td></tr>
   <tr><td>Imcrement<td></tr>
   <tr><td>Decrement<td></tr>
   </table>
   </td>
    
  </tr>

  <tr>
    <td>Logical</td>
   <td>
   <table>
   <tr><td>!<td></tr>
   <tr><td>&&<td></tr>
   <tr><td>||<td></tr>
   </table>
   </td>

   <td>
   <table>
   <tr><td>Not<td></tr>
   <tr><td>And<td></tr>
   <tr><td>Or<td></tr>
   </table>
   </td>
    
  </tr>

  <tr>
    <td>Comparator</td>
   <td>
   <table>
   <tr><td>== / ===<td></tr>
   <tr><td>< / ><td></tr>
   <tr><td><= / >=<td></tr>
   </table>
   </td>

   <td>
   <table>
   <tr><td>Equal to<td></tr>
   <tr><td>Less than / Greater than<td></tr>
   <tr><td>Less than or equal to / Greater than or equal to<td></tr>
   </table>
   </td>
    
  </tr>
  
</table>

--------------------------------------------------
## <span style="color:red" id='loops'>Loops</span>
A loop repeats section of code within curly brackets { }. In `JavaScript`, a *for...of* loop goes through each element in an array or string, repeating the code for each element.  
``` js
var basket = ['apples','banana','mango','pineapples']
for (var fruit of basket){
   console.log(fruit)
}
```
The code given above will print name of fruits stored in *basket* array.

`JavaScript` also supports a classic *for loop*, which repeats the same code inside the block { } a specified number of times. It is defined in 3 Parts,  
1. Define loop Variable *(for var i=0;)*  - This part happend before the loop starts,  
2. Test of loop *(i<10;)* - This part determines if the loop should keep repeating,  
3. Update the loop variable *(i++)* - This part updates looping variable each time loop repeats.

``` js
//this loop will print numbers from 0 to 9
for (var i=0;i<10;i++){
   console.log(i)
}
```
`JavaScript` also supports nested loops i.e. we can use loop within a loop.  
For ex.
``` js
//this loop will print table of numbers from 1 to 10
for (var i=1;i<=10;i++){
   for (var j=i;j<=i*10;j+=i){
      console.log(j)
   }
}
```

## <span style="color:red" id='obj'>Object Expression</span>
An object in `JavaScript` can store multiple pieces of informatoin inside one variaboe. Dot *(.)* notation is used to access a property of an object *(object.property)*.
``` js
var object = {
   property1 = 1,
   property2 = 10,
   property3 = 100,
}
```