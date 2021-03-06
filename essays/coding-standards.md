---
layout: essay
type: essay
title: Code to Read
date: 2017-02-07
labels:
  - ESLint
  - Intellij
  - Learning
  - JavaScript
---

## Functional and Practical

As a complete beginner, understanding a block of code can be difficult, but block itself should not be difficult to read. The way a programmer formats their code is important to writing readable code. Seeing text all bunched up together can be confusing to the eye as you try to parse through what a function does.

```
//Toobunchedup
function HelloWorld(){console.log("Hello World!");}
```

The opposite is also true as excessive spaces and blank lines end up taking too much space that could be given to other windows or more code on the screen. There is a balance that should be followed so that code blocks can be more pleasing to the eye.

```
// Unnecessary s p a c i n g
function HelloWorld()
{
	console.log( "Hello World!" ); 
}
```
```
//Just right
function HelloWorld() {
	console.log("Hello World!");
}
```

In addition to proper spacing, functions and variables should be named appropriately so that anyone reading it could understand what it does with minimal commentation. For example,

```
function a(a, b) {
	let c = 0;
	let d = [a, b];
	c = a + b;
	d.push(c);
	return d;
}
```

The function above is named the same as a variable it takes in which will make it confusing if we will also be calling the function. The variables names also don't tell us anything useful which takes more time to parse through the code. Let's see what it looks like with more proper names.

```
function numberList(num1, num2) {
	let num3 = 0;
	let numList = [num1, num2];
	num3 = num1 + num2;
	numList.push(num3);
	return numList;
}
```

Now, when you simply look at this code you can understand that we are dealing with a bunch of numbers and it returns a list of them. This saves us a few seconds that could add up if we were reading a project that consisted of hundreds of thousands of lines of code.

## JavaScript and ESLint

As of this writing I have just learned about ESLing coding standards. During my practice, I found that linters aren't happy with '++' notations and ForOf loops. The ForOf I understand why because we have Underscore.js to help us make most for and if loops obsolete. The '++' notation I find odd however, as using '+=' as the alternative just makes the code longer. From my understanding it has something to do with the way JavaScript may call certain functions and there for is a potential violation hazard that should just be avoided altogether. In any case, this is nothing to be really upset about as ESLint seems to be more or less how I would normally format my code anyway. It tells you to have proper indents, put spaces before {} after a function, and warns you that a variable or function name should be rewritten to meet standards.

```
//Wrong
function Testnums()

//Correct
function TestNums()
```

With time, I may find ESLint to be a bit nit picky about how some naming conventions should be rewritten like flagging 'nums' when really writing 'numbers' will take much longer. That being said, it is so far the only issue that I have so far. As I do more programming assignments I'll see if ESLint likes working with me or not.
