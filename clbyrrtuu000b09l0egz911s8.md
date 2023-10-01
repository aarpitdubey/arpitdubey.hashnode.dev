---
title: "Decoding Arrays In Java Script"
seoTitle: "Arrays, Array Properties, Operation, Function, Method, Javascript"
datePublished: Thu Dec 22 2022 07:35:49 GMT+0000 (Coordinated Universal Time)
cuid: clbyrrtuu000b09l0egz911s8
slug: decoding-arrays-in-java-script
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1671695579087/RV-o1X-Fg.gif
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1671700040449/do5d3vfnm.gif
tags: ineuron, hiteshchoudharylco, ineuron-hiteshchaudhary-webdev-javascript-lco-learncodeonline, ineuron-hiteshchaudhary-webdev-javascript-lco-learncodeonline-lco-css-learncodeonline-cssselectors-hiteshchoudharylco-code-with-hitesh-choudhary, ineuronfullstackjavascriptbootcam20

---

Hola! Coders 👨‍💻 Hope you all are doing well, In this article, I'm going to give an introduction to arrays, their properties, operations, and methods let's see what the agenda of this blog is :

# **Agenda**

*   Introduction to Arrays
    
*   Array Properties
    
*   Array Operations
    
*   Inbuilt Array Functions
    
*   Array Methods
    
    ## Introduction to Arrays
    
    **Array**: An array is an object that can store multiple values at once.
    
    For example,
    

```javascript
const words = ['hello', 'world', 'ineuron'];

//for iterating items through the array

for(let word in words)
    console.log(`${parseInt(word)+1} : ${words[word]}`); 

// It will give/show the array on console/Terminal.
```

Here, the variable name **<mark>"words"</mark>** is an array. The array is storing 3 values.

# **Create an Array**

You can **<mark>create an array</mark>** using two ways:

**1\. Using an array literal**

The easiest way to create an array is by using an array literal `[]`. For example,

```javascript

const courses = ["Full Stack Javascript Bootcamp 2.0", "Full Stack Datascience", "Full Stack Blockchain Developer", "Full Stack Java Developer", "Full stack Big Data Developer"];
```

**2.** **Using the new keyword**

You can also create an array using JavaScript `new` keyword.

```javascript
const courses = new Array("Full Stack Javascript Bootcamp 2.0", "Full Stack Datascience", "Full Stack Blockchain Developer", "Full Stack Java Developer", "Full stack Big Data Developer");
```

In both of the above examples, we have created an array having two elements.

**<mark>Note: It is recommended to use an array literal to create an array.</mark>**

Here are more examples of arrays:

```javascript

// empty array
const emptyArray = [ ];

// array of numbers
const evenNumberArray = [2, 4, 6, 8];

// array of strings
const stringArray = ["Full Stack Javascript Bootcamp 2.0", "Full Stack Datascience", "Full Stack Blockchain Developer"];

// array with mixed data types
const newData = ["Full Stack Javascript Bootcamp 2.0", "Full Stack Datascience", 17700, true];
```

You can also store **<mark>arrays, functions and other objects</mark>** inside an array. For example,

```javascript

const newData = [
    {'task1': 'exercise'},
    [1, 2 ,3],
    function hello() { console.log('hello')}
];
```

## **Access Elements of an Array**

You can **<mark>access</mark>** elements of an array **<mark>using indices&nbsp;(0, 1, 2 …)</mark>**. For example,

```javascript

const myArray = ['h', 'e', 'l', 'l', 'o'];

// first element
console.log(myArray[0]);  // "h"

// second element
console.log(myArray[1]); // "e"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671692474734/X2FMydglo.png align="center")

> Array indexing in JavaScript
> 
> **<mark>Note: Array's index starts with 0, not 1</mark>**<mark>.</mark>

## **Add an Element to an Array**

You can use the built-in method `push()` and `unshift()` to add elements to an array.

The `push()` the method **<mark>adds an element at the end of the array</mark>**. For example,

```javascript

let dailyActivities = ['eat', 'sleep'];

// add an element at the end
dailyActivities.push('exercise');

console.log(dailyActivities); //  ['eat', 'sleep', 'exercise']
```

The `unshift()` the method **<mark>adds an element at the beginning of the array</mark>**. For example,

```javascript

let dailyActivities = ['eat', 'sleep', 'code'];

//add an element at the start
dailyActivities.unshift('work');

console.log(dailyActivities); // ['work', 'eat', 'sleep', 'code']
```

## **Change the Elements of an Array**

You can also **<mark>add elements or change the elements by accessing the index value.</mark>**

```javascript

let dailyActivities = [ 'eat', 'sleep'];

// this will add the new element 'exercise' at the 2 index
dailyActivities[2] = 'exercise';

console.log(dailyActivities); // ['eat', 'sleep', 'exercise']
```

Suppose an array has two elements. If you try to add an element at index 3 (fourth element), the third element will be undefined. For example,

```javascript

let dailyActivities = [ 'eat', 'sleep'];

// this will add the new element 'exercise' at the 3 index
dailyActivities[3] = 'exercise';

console.log(dailyActivities); // ["eat", "sleep", undefined, "exercise"]
```

If you try to add elements to high indices, the indices in between will have an undefined value.

## **Remove an Element from an Array**

You can use the `pop()` **<mark>method to remove the last element from an array.</mark>** The `pop()` the **<mark>method also returns the returned value</mark>**. For example,

```javascript

let dailyActivities = ['work', 'eat', 'sleep', 'exercise'];

// remove the last element
dailyActivities.pop();
console.log(dailyActivities); // ['work', 'eat', 'sleep']

// remove the last element from ['work', 'eat', 'sleep']
const removedElement = dailyActivities.pop();

//get removed element
console.log(removedElement); // 'sleep'
console.log(dailyActivities);  // ['work', 'eat']
```

If you need to remove the first element, you can use the `shift()` method. <mark>The&nbsp;</mark>   `shift()`   <mark>&nbsp;, </mark> **<mark>the method removes the first element and also returns the removed element</mark>**. For example,

```javascript

let dailyActivities = ['work', 'eat', 'sleep'];

// remove the first element
dailyActivities.shift();

console.log(dailyActivities); // ['eat', 'sleep']
```

## **Array length**

You can <mark>find the length of an element (the number of elements in an array) using the&nbsp;</mark>   `length`   <mark>&nbsp;property</mark>. For example,

```javascript
const dailyActivities = [ 'eat', 'sleep'];

// this gives the total number of elements in an array
console.log(dailyActivities.length); // 2
```

## **Array Operations**

In JavaScript, there are various array methods available that make it easier to perform useful calculations.

Some of the commonly used JavaScript array methods are:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671564830412/C_Xl4dzGs.png align="center")

#### **Example: JavaScript Array Methods**

```javascript

let dailyActivities = ['sleep', 'work', 'exercise']
let newRoutine = ['eat'];
let ages = [4, 9, 16, 25, 36, 49];

// sorting elements in the alphabetical order
dailyActivities.sort();
console.log(dailyActivities); // ['exercise', 'sleep', 'work']

//finding the index position of string
const position = dailyActivities.indexOf('work');
console.log(position); // 2

// slicing the array elements
const newDailyActivities = dailyActivities.slice(1);
console.log(newDailyActivities); // [ 'sleep', 'work']

// concatenating two arrays
const routine = dailyActivities.concat(newRoutine);
console.log(routine); // ["exercise", "sleep", "work", "eat"]

// filter an array
const adults = ages.filter(checkAdult);
function checkAdult(age) {
  return age >= 18;
}
console.log(adults); // [25, 36, 49]

//map a function to an array
const ages_sqrt = ages.map(Math.sqrt)
console.log(ages_sqrt); // [2, 3, 4, 5, 6, 7]
```

> **Note: If the element is not in an array, indexOf() gives -1.**

## **Working on JavaScript Arrays**

In JavaScript, <mark>an array is an object. And, the indices of arrays are object keys.</mark>

Since arrays are objects, the array elements are stored by reference. Hence, <mark>when an array value is copied, any change in the copied array will also reflect in the original array.</mark> For example,

```javascript

let arr = ['h', 'e'];
let arr1 = arr;
arr1.push('l');

console.log(arr); // ["h", "e", "l"]
console.log(arr1); // ["h", "e", "l"]
```

You can also store <mark>values by passing a named key in an array</mark>. For example,

```javascript

let arr = ['h', 'e'];
arr.name = 'John';

console.log(arr); // ["h", "e"]
console.log(arr.name); // "John"
console.log(arr['name']); // "John"
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671690172393/My5N64hix.png align="center")

**Array indexing in JavaScript**

However, it is not recommended to store values by passing arbitrary names in an array.

Hence in JavaScript, you should <mark>use an array if values are in an ordered collection.</mark> Otherwise, it's better to use an object with `{ }`.

<mark>A multidimensional array is an&nbsp;array&nbsp;that contains another array.</mark> For example,

```javascript

// multidimensional array
const data = [[1, 2, 3], [1, 3, 4], [4, 5, 6]];
```

## **Create a Multidimensional Array**

Here is how you can create multidimensional arrays in JavaScript.

**Example 1**

```javascript

let studentsData = [['Jack', 24], ['Sara', 23], ['Peter', 24]];
```

**Example 2**

```javascript

let student1 = ['Jack', 24];
let student2 = ['Sara', 23];
let student3 = ['Peter', 24];

// multidimensional array
let studentsData = [student1, student2, student3];
```

Here, both example 1 and example 2 create a multidimensional array with the same data.

## **Access Elements of an Array**

You can <mark>access</mark> the elements of a multidimensional array <mark>using indices&nbsp;</mark>   **<mark>(0, 1, 2 …)</mark>**<mark>. </mark> For example

```javascript


let x = [
['Jack', 24],
['Sara', 23],
['Peter', 24]
];

// access the first item
console.log(x[0]); // ["Jack", 24]

// access the first item of the first inner array
console.log(x[0][0]); // Jack

// access the second item of the third inner array
console.log(x[2][1]); // 24
```

You can think of a multidimensional array (in this case, x), as a table with 3 rows and 2 columns.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1671691211567/1dLLFP9fd.png align="center")

Accessing multidimensional array elements.

### Add an Element to a Multidimensional Array

You can use  Array's `push()`   <mark>&nbsp;method&nbsp;or an indexing notation to add elements to a multidimensional array.</mark>

**Adding Element to the Outer Array**

```javascript

let studentsData = [['Jack', 24], ['Sara', 23],];
studentsData.push(['Peter', 24]);

console.log(studentsData); //[["Jack", 24], ["Sara", 23], ["Peter", 24]
```

Adding Element to the Inner Array

```javascript


// using index notation
let studentsData = [['Jack', 24], ['Sara', 23],];
studentsData[1][2] = 'hello';

console.log(studentsData); // [["Jack", 24], ["Sara", 23, "hello"]]
```

```javascript


// using push()
let studentsData = [['Jack', 24], ['Sara', 23],];
studentsData[1].push('hello');

console.log(studentsData); // [["Jack", 24], ["Sara", 23, "hello"]]
```

You can also use  <mark>Array's&nbsp;</mark>   `splice()` <mark>method&nbsp;to add an element at a specified index.</mark> For example,

```javascript


let studentsData = [['Jack', 24], ['Sara', 23],];

// adding element at 1 index
studentsData.splice(1, 0, ['Peter', 24]);

console.log(studentsData); // [["Jack", 24], ["Peter", 24], ["Sara", 23]]
```

## **Remove an Element from a Multidimensional Array**

You can use  <mark>Array's&nbsp;</mark>   `pop()` <mark>method&nbsp;to remove the element from a multidimensional array.</mark> For example,

**Remove Element from Outer Array**

```javascript


// remove the array element from outer array
let studentsData = [['Jack', 24], ['Sara', 23],];
studentsData.pop();

console.log(studentsData); // [["Jack", 24]]
```

**Remove Element from Inner Array**

```javascript


// remove the element from the inner array
let studentsData = [['Jack', 24], ['Sara', 23]];
studentsData[1].pop();

console.log(studentsData); // [["Jack", 24], ["Sara"]]
```

You can also use <mark>the&nbsp;</mark>   `splice()`   <mark>&nbsp;method to remove an element at a specified index.</mark> For example,

```javascript


let studentsData = [['Jack', 24], ['Sara', 23],];

// removing 1 index array item
studentsData.splice(1,1);
console.log(studentsData); // [["Jack", 24]]
```

## **Iterating over Multidimensional Array**

You can iterate over a multidimensional array using  <mark>Array's </mark> `forEach()` <mark>method&nbsp;to iterate over the multidimensional array.</mark> For example,

```javascript


let studentsData = [['Jack', 24], ['Sara', 23],];

// iterating over the studentsData
studentsData.forEach((student) => {
    student.forEach((data) => {
        console.log(data);
    });
});
```

**Output**

```plaintext

Jack
24
Sara
23
```

<mark>The first&nbsp;</mark>   `forEach()`   <mark>&nbsp;the method is used to iterate over the outer array elements and the second&nbsp;</mark>   `forEach()`   <mark>&nbsp;is used to iterate over the inner array elements.</mark>

You can also use <mark>the&nbsp;</mark>   `for...of`   <mark>&nbsp;loop to iterate over the multidimensional array.</mark> For example,

```javascript


let studentsData = [['Jack', 24], ['Sara', 23],];

for (let i of studentsData) {
  for (let j of i) {
    console.log(j);
  }
}
```

You can also use the for loop to iterate over a multidimensional array. For example,

```javascript


let studentsData = [['Jack', 24], ['Sara', 23],];

// looping outer array elements
for(let i = 0; i < studentsData.length; i++){

    // get the length of the inner array elements
    let innerArrayLength = studentsData[i].length;

    // looping inner array elements
    for(let j = 0; j < innerArrayLength; j++) {
        console.log(studentsData[i][j]);
   
```

## forEach

*   Iterates through the elements in an array.
    
*   Executes a callback for each element.
    
*   Does not return a value.
    

```javascript
const a = [1, 2, 3];
const doubled = a.forEach((num, index) => {
  // returning 2 x values of each element 
    return num * 2;
});

console.log(doubled);

// doubled = undefined
```

## map

*   Iterates through the elements in an array.
    
*   "Maps" each element to a new element by calling the function on each element, creating a new array as a result.
    

```javascript
const a = [1, 2, 3];
const doubled = a.map(num => {
  return num * 2;
});

console.log(doubled);

// doubled = [2, 4, 6]
```

<mark>The main difference between&nbsp;</mark>   `.forEach` <mark>and&nbsp;</mark>   `.map()` <mark>is that&nbsp;</mark>   `.map()` <mark>returns a new array.</mark> If you need the result, but do not wish to mutate the original array, `.map()` is a clear choice. If you simply need to iterate over an array, `forEach` is a fine choice.