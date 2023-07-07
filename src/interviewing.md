In this topic, we will solve former **Google** Interview question using `JavaScript` skiils we gained so far.

> Given a dictionary of words and a string, such as `supercalifragilisticexpialidocious`, could you write an algorithm to find the longest word in the dictionary that is a sebsequence of the string?

> Write a *function* that takes a *`string`* (*stringSequence*) and an *array* of *`string`* (*dictionary*). The function should return the longest *`string`* in dictionary that is a *subsequence* of *stringSequence*.

A subsequence is of a *`string`* is a *`string`* if all of it's characters appear and are in same order.  
For ex. `hello` is subsequence of `help love everyone`. But `abe` is not a subsequence of `bale`.
___
#### The Longest Word
- Lets start by tackling how to find longest word. We can figure out how to find subsequence later. How will we find longest string in an array? We can write a *`function`* that takes array of strings and return longest *`string`*.  
We need to know length of each string. We can loop through each *`string`* of an *`array`*.

    Here is the code implementatoin
    ``` js
    function findLongest(array){
        var longString = '' // empty string to store output

        // looping through array
        for (var string of array){
            if (string.length > longString.length){
                longString = string;
            }
        }
        return longString;
    }
    ```

#### String Catrography
- To check if a word in the *`array`* (*dictionary*) is a subSequence of the stirng (*stringSequence*), it is important to know what characters are in stringSequence and where they appear. We can turn `string` into an object. Each character in the *`string`* will become a propert, with the indices where they appear stored in *`array`*.

    Here is the code
    ``` js
    function mapString(string){
        var object = {} // empty object to store output

        // looping through  string
        for (let i=0;i<string.length;i++){
            letter = string[i]; //each letter of string
            if (object[letter]){
                object[letter].push(i);
                /*if letter is in map,
                append letter index in array*/
            }
            else{
                object[letter] = [i];
                //create an array to store the index
            }
        }
        return object;
    }
    ```

#### Comparing Letters
- Now we can compare object of the *`string`* with a *`string`* in dictionary to find out if the dictionary string is a sebsequence. Let's write a *`function`* that checks if all the characters in a *`string`* exist as properties in the object, and returns `true` or `false`. We will make sure their order later.
    Here is the code:
    ``` js
    function compareLetters(string, object){
        for (let letter of string){
            if (object[letter]){
                //do nothing if letter
                //exists in object as a property
            }
            else{
                //if letter does not exist,
                //return `false`
                return false;
            }
        }

        return true;
    }
    ```

#### Check the Order
- In order for a *`string`* (dictionaryWord) to be a subsequence of another *`string`* (stringSequence), all of it's letters must appear in same order. Previously written *`function`* only checks it all of the lerrers appear. Let's write *`function`* that would check order as well.

    Here is the code:
    ``` js
    // a helper function to find index of elements
    function findNextIndex(array, minIndex){
        for (let index of array){
            if (index>=minIndex){
                return index+1;
            }
        }
        return false;
    }
    //updating 'compareLetters()' function
    function isSubsequence(string, object){
        let minIndex = 0;
        for (let letter of string){
            if (object[letter]){
                minIndex = findNextIndex(object[letter],minIndex);
                if (minIndex === false){
                    return false;
                }
            }
            else{
                return false;
            }
        }
        return true;
    }
    ```
#### Putting it all together

``` js
function longestMatch(string, dictionary){
    let object = mapString(string);
    //array to store all matcher
    let matchess = []

    for(var word of dictionary){
        if (isSubsequence(word, object)){
            matches.push(word);
        }
    }
    return longestWord(matches);
}

var string = "javascript";
var dictionary = ['art','vascular','javas','vat']
console.log(longestMatch(string,dictionary));
//avast
```
---
---