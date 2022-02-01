# The Basics Of Java Script

## What is java script?
It's what we have to deal with when programming for the web.

## Why?
Tradition I guess.

## How do I get set up with this mess then?
1. Create a folder to hold your files. (optional but recommended)
2. Create two files, one named `index.html` and one named `main.js`.
3. For `index.html` use this template or copy from the repository.
```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>Document</title>
        <script src="./main.js"></script>
    </head>
    <body>
    </body>
</html>
```
4. For `main.js` use this template or copy from the repository
    - You can stuff any javascript code fragments in here to see them run with your own eyes.
```javascript
console.log("Yay.");
```
5. Simply open `index.html` in your browser of choice.
6. Open developer tools (usually f12) and get to the console.
7. You should see `Yay.` printed somewhere. If not then refresh the page.
8. Congrats! You're set up to suffer :3

# A Technical Introduction

## Basic syntax
Instructions in javascript *should* be terminated with a semicolon. If you don't do this then whatever who cares. Code blocks (as you'll see later) should always be wrapped with curly braces `{}`. 

## Comments
Comments help you and other developers know what the hell is going on. For single line comments use `//` two forward slashes. For multi line comments surround what you want to comment out with `/* {CODE OR SOMETHING HERE */`

### Examples:
```javascript
// This is a comment
function code_block(){
    console.log("Yep.");
}
/*
    This 
    is 
    a 
    multi 
    line 
    comment    
*/
```

## Variables
Variables are how you keep track of data. You *theorhetically* assign anything to them. Numbers, letters, objects. Anything! Since this language is not type checked, it is quite simple to create one. You will always use the equal sign to assign a variable to something. There are three kinds of variables you will encounter. 
- `var`: Ol' nasty. Not recommended to use anymore because data can fly all over the place and make a mess. I will get upset if you use this one anywhere.
- `let`: Your new best friend. Please use this one. Please. We can talk about why this one is prefered later if you wish.
- `const`: Immutable. Unshakable. Invincible. You cannot change the value of this once it has been declared. 

### Examples:
```javascript
//A global variable called first_name that has a string value
var first_name = "Freddy Fast Bear";

//A variable called age that has a number value
let age = 10;

//A constant variable called is_my_cat_cute that has a boolean value
const is_my_cat_cute = true;

//A variable that is declared but not initialised to anything
let a;

//Variables can even take on the value of other variables
//Set a equal to age
a = age; 
//note: we do not need to put var, let or const infront of a again as it is already declared. javascript will get very angry if you do this.
```

## Data Types
As seen above, varibales can hold many different types of data. Let us see what we can stuff into them.
- ***STRING***: Holds a set of characters. Usually denoted with quotation marks.
- ***NUMBER***: Holds a numerical value. Can be floating point (number with decimal)
- ***BOOLEAN***: `true` or `false`.
- ***NULL***: No value. Useful for absolutely making sure something isn't defined
- ***UNDEFINED***: If a value is not given to a variable when it is declared it will default to this. Very useful for checking if something is defined or not.
- ***OBJECT***: A collection of properties. We will talk about this one later

## The Logger
This is your friend. Use it whenever you want to quickly see what value a variable has. You can do this with `console.log()`

### Example:
```javascript
let name = "Willy Willson";
console.log(name);
```

## String Concatination
Sometimes it's helpful to output your data in a meaningful way. To debug stuff or whatever. Since javascript does what it wants, you can just add strings together to get an even bigger one. Use a `+` to mash strings together. 

### Example
```javascript
let string1 = "some characters and";
let string2 = "some more characters";
console.log("this is a string literal: " + string1 + " " + string2);
```