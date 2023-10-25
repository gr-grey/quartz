---
title: JavaScript
date: 2023-10-25
summary: ""
tags:
  - learning
  - javascript
  - "front end"
---

These are course notes from [Programming with JavaScript - Introduction to Javascript](https://www.coursera.org/learn/programming-with-javascript/home/week/1) ,  offered by Meta on Coursera.

## Basic grammar

```javascript
var person = "Vera";
let person1 = "Gary";
const person2 = "liu";

let person3 = person1 + ' ' + person2;// Gary liu

console.log("Print stuff", "like a name", person);
// same as using template literals
console.log(`Print stuff like a name ${person}`);

var stringVar = "hello"; // or 'hello'
var numVar = 1;
var boolVar = true; // or false
var nullVar = null; // object
var aVar; // undefined
var arrVar = [1, '2', 3]; // object

5 > 4 > 3; // 5>4 returns true, coverted to 1, 1>3 returns false

```

### Common methods
- `console.log` print
- `var let const` declare variables
- `typeof` return data types
- Operators
	- assignment `= += -= *= /=`
	- arithmetic `+ - * / % **`
	- comparison `> >= < <= != == ===`
	- logical `&& || !`

### Datatypes
- string 
- number, bigInt
- boolean
- undefined, has only one value, undefined.
- object: null, array

Details of array are in the [gory details - array](#array).

### Functions, conditions, loops

```javascript
function hello () {
	console.log("hello world");
}

for (var i=0; i<100; i++) {
	console.log(i);
//  Nested loops
	for (var j = 0; j < 10; j++) {
		console.log(j);
	}
}

var cubes = 'ABCDEFG';
//styling console output using CSS with a %c format specifier
for (var i = 0; i < cubes.length; i++) {
    var styles = "font-size: 40px; border-radius: 10px; border: 1px solid blue; background: pink; color: purple";
    console.log("%c" + cubes[i], styles)
}

// if statement

var score = 50;
if (score > 40) {
	console.log("You've passed the exam.");
} else if (score > 30) {
	console.log("Didn't pass. Try again.");
} else {
	console.log("maybe get a tutor.");
}

//
var place = 1;
switch (place) {
	case 1: // first place
		console.log("Gold");
		break;
	case 2:
		console.log("Silver");
		break;
	case 3:
		console.log("Bronze");
		break;
	default:
		console.log("😎");
}
```

### Weird things in JS

- Semicolon `;` at the end of each statement is not necessary (I've never encountered an error when forgot), but recommended. 
- `console.log(str1, str2)` with multiple arguments, will add a space between them, but if `console.log(str1 + str2)` it won't add the space (since it's one string variable now).
- You can call a variable before declaring it, the variable will be *undefined*. As long as it was declared by `var`later, no error will be invoked.
- Implicit datatype converting: 
	- `+` operator works with *number* datatype, it'll turn the number into a string first.
	- `true` is converted to 1, false is converted to 0
	- converts types when comparing with `==`, `'1' == 1` is true, `true == 1` is true, but when using `===`, both of them are false (since types are different).
- Arrays are object does not support comparison operator. `[1] == [1]` returns false.

## History and random things

JavaScript was created in 10 days by one person, Brendan Eich.
Originally called LiveScript, then was changed to JavaScript because the Java language was the cool kid at the time. Despite the similarity in name, Java and JavaScripts are in no way related.

It was born with a single purpose: browser. To build websites.
When it comes to websites, it's the one language that rules all.
It's the one and only, a central pillar of web dev 🛠️.

It has evolved over time, but was made to be backwards compatible, which might be why it's behaves so weirdly - patches upon patches, new stuff appear but has to work with old examples, like most things biology 🧠. 

Every browser comes with a *JavaScript Engine*, which is like a compiler of sorts - interpret JavaScript and turn the codes into actual webpages. 

Then came *Node.js*, a JavaScript Engine without a browser, built by Ryan Dahl in 2009.
Now JS code can run freely and do all the things other languages like Python can already do 👻 (and probably not as well as them).
This is huge, as it allows us to use JS to build other stuff other than webpages, like the back end of webpages.

Now JavaScript runs on browsers, servers, PCs, raspberry pies, any device that can run a JavaScript engine (Node.js).

*jQuery* is an old man that has seen its glorious days. It was the most popular JS library for over a decade, built to solve the compatibility issues among different browsers.

*React* came in 2011, is sort of a successor to jQuery.

Other contenders: Knockout, Backbone, Angular, Ember, Vue, Alpine.

---
JavaScript is a weird language, with too many exceptions to remember.

Start building simple apps as soon as possible.

Work on open source project as early as you can.

Start a blog (like this one) as early as you can.

## Gory details

---

#### String

Strings are defined using single quotes (`'`), double quotes (`"`), or backticks (`` ` ``). 
Strings are iterable, array like.

- `length` 
- `charAt(index)` Returns the character at the specified index
- `concat(string2, string3, ..., stringX)` 
- `startsWith(substring)` 
- `endsWith(substring)` 
- `includes(substring)` 
- `indexOf(substring)` Returns the index of the first occurrence of a specified substring.
- `lastIndexOf(substring)` Returns the index of the last occurrence of a specified substring.
- `substr(startIndex, length)`Returns the part of the string between the start index and a number of characters after it.
- `match(regexp)` Searches for a match between a regular expression and the string.
- `replace(searchFor, replaceWith)` Searches for a specified substring or regular expression and replaces it with another substring.
- `slice(startIndex, endIndex)` Extracts a section of the string and returns it as a new string.
- `substring(startIndex, endIndex)`Returns the part of the string between the start and end indexes.
- `split(separator)` Splits the string into an array of strings based on a separator.
- `toLowerCase()` Converts all the alphabetic characters in a string to lowercase.
- `toUpperCase()` Converts all the alphabetic characters in a string to uppercase.
- `trim()` Removes whitespace from both ends of a string.

**Styling in Console**

You can use `%c` in `console.log` to style console output using CSS-like declarations.

```javascript
console.log("%cThis is a styled message", "color: red; font-size: 20px;");
```

**Template Literals** are
enclosed by backticks, that allow you to *embed expressions* within strings, *multi-line strings*, and *string interpolation*.

```javascript
const name = "John";
console.log(`Hello, ${name}`);  // Output: "Hello, John"
```

#### Array

Arrays are object can't be compared directly. `[1] == [1]` returns false.

**Attribues**: arr.length

**Methods**
 - Adding/Removing Elements:
	- `push(element1, ..., elementN)`: Adds elements to the end of the array.
	- `unshift(element1, ..., elementN)`: Adds elements to the beginning of the array.
	- `pop()`: Removes the last element from the array.
	- `shift()`: Removes the first element from the array.
	- `splice(start, deleteCount, item1, ..., itemX)`: Adds/Removes elements from the array.
-  Iterating:
	- `forEach(callbackFn)`: Executes a function for each array element.
	- `map(callbackFn)`: Creates a new array based on the results of calling a function on every array element.
	- `filter(callbackFn)`: Creates a new array with all elements that pass the test implemented by the provided function.
	- `reduce(callbackFn[, initialValue])`: Applies a function against an accumulator and each element in the array to reduce it to a single value.
	- `some(callbackFn)`: Checks if at least one element in the array passes the test implemented by the provided function.
	- `every(callbackFn)`: Checks if all elements in the array pass the test implemented by the provided function.
- Searching and Location:
	- `indexOf(element[, fromIndex])`: Returns the first index at which a given element can be found in the array.
	- `lastIndexOf(element[, fromIndex])`: Returns the last index at which a given element can be found in the array.
	- `find(callbackFn)`: Returns the first element that satisfies the provided testing function.
	- `findIndex(callbackFn)`: Returns the index of the first element that satisfies the provided testing function.
	- `includes(element[, fromIndex])`: Determines whether an array includes a certain element.
- Slicing and Joining:
	- `slice([begin[, end]])`: Returns a shallow copy of a portion of an array.
	- `concat(array2, array3, ..., arrayX)`: Merges two or more arrays.
	- `join([separator])`: Joins all elements of the array into a string.
- Sorting and Reversing:
	- `sort([compareFn])`: Sorts the elements of an array.
	- `reverse()`: Reverses the elements of an array.
-  Others:
	- `flat([depth])`: Creates a new array with all sub-array elements concatenated recursively up to the specified depth.
	- `flatMap(callbackFn)`: Maps each element using a mapping function, then flattens the result into a new array.
	- `fill(value[, start[, end]])`: Fills all the elements of an array from a start index to an end index with a static value.
	- `copyWithin(target, start[, end])`: Shallow copies part of an array to another location in the same array.


---


## Additional resources

### Basic grammar

[Mozilla Developer Network Expressions and Operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators) 

[Mozilla Developer Network Operator Precedence and Associativity](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Operator_Precedence "Mozilla Developer Network Operator Precedence and Associativity") 

[JavaScript Primitive Values](https://developer.mozilla.org/en-US/docs/Glossary/Primitive) 

[ECMA262 Specification](https://tc39.es/ecma262/) 

[jQuery Official Website](https://jquery.com/) 

[React Official Website](https://reactjs.org/) 

[StackOverflow Developer Survey 2021 Most Popular Technologies](https://insights.stackoverflow.com/survey/2021#technology-most-popular-technologies)

[Emojis](http://unicode.org/emoji/charts/full-emoji-list.html#1f600)