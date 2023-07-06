# Array Methods

In this module, we will learn to search arrays, combine elemetnts an transform elements using row functions

### Contents
[1. Search and Locate](#search-and-locate)  
[2. Manipulation](#manipulation)  
[3. Apply Functions](#apply-functions)

### Search and Locate
- *.incudes()* is the array method to search for an item in an array. It will return `ture` or `false` depending on whether the item is found.
``` js
var color = ["red","green","blue"]
color.includes("red") // true
```

- *.indexOf()* is the array method to find index of element. If no element is found then it will return -1.
``` js
var color = ["red","green","blue"]
console.log(color.indexOf("red")) // 0
```

- *.lastIndexOf()* is the array method to find index of element, similar to *.indexOf()* method but in reverse order (from end of array). If no element is found then it will return -1.
``` js
var color = ["red","green","red","blue"]
console.log(color.lastIndexOf("red")) // 2
```

------------------------------------------
### Manipulation
- Removing first element :- *`.shift()`* is method similar to *`.pop()`*, which removes 1st element from an array and log it to console.
``` js
var color = ["red","green","red","blue"]
color.shift() // "red"
```
- Adding to start :- *`.unshift()`* is method similar to *`.push()`*, which add element to start of array.
``` js
var color = ["red","green","blue"]
color.unshift("black") // ["black","red","green","blue"]
```

- Reversing an array :- *`.reverse()`* method reverses an array.
``` js
var color = ["red","green","blue"]
color.reverse()
// ["blue","green","red"]
```

- Repacing elements - *`.splice()`* replaces a section of array with new element. This method will takes 3 arguements, start index, number of items to be removed and new item (or items) to insert. If the third arguement is black then it will only delete the elements.
``` js
var num = [1,0,0,0,0,3,4,5]
num.splice(1,4,2)
// [1,2,3,4,5]

// Alternatively
var num = [1,0,0,0,0,3,4,5]
num.splice(1,4,2,2,2,2)
// [1,2,2,2,2,3,4,5]
```

- Joining elements :- *`.join()`* method combines all of the elements of an array into a string. It can optionally take a string as an arguement, and will insert that string between each element as it joins the array. If no arguement is given, it will insert comma. The original is not modified.
``` js
var marr = ['a','b','c','d'];
var nar = marr.join("->");
console.log(nar);
// a->b->c->d
```
------------------
### Apply Functions