# Hello world
- We can use a <script> tag to add Javascript code to a page.
- The type and language attributes are not required.
- A script in an external file can be inserted with <script src="path/to/script.js"></script>

## Tasks
- [x] Show an alert
    - create a page that shows a message "I'm Javascript"
- [x] Show an alert with an external script

# Code structure
- Statements
    - Statements are syntax constructs and commands that perform actions.

- Semicolons
    - A semicolon may be omitted in most cases when a line break exists.

- Comments
    - As time goes on, programs become more and more complex. It becomes necessary to add comments which describe what the code does and why.

    - Comments can be put into any place of a script. They don’t affect its execution because the engine simply ignores them.

    - One-line comments start with two forward slash characters //.

    - Multiline comments start with a forward slash and an asterisk /* and end with an asterisk and a forward slash */.

# "use strict" - modern mode
- The directive looks like a string: "use strict" or 'use strict'. When it is located at the top of a script, the whole script works the “modern” way.

> ### NOTE
> Pleas make sure that "use strict" is at the top of your scripts, otherwise strict mode may not be enabled.
> Modern JavaScript supports “classes” and “modules” – advanced language structures (we’ll surely get to them), that enable use strict automatically. So we don’t need to add the "use strict" directive, if we use them.

# Variables
- A variable
- Variable naming
- Constants

- We can declare variables to store data by using the var, let, or const keywords.

    - let – is a modern variable declaration.
    - var – is an old-school variable declaration. Normally we don’t use it at all, but we’ll cover subtle differences from let in the chapter The old "var", just in case you need them.
    - const – is like let, but the value of the variable can’t be changed.

- Variables should be named in a way that allows us to easily understand what’s inside them.

# Data types
- A value in JavaScript is always of a certain type. For example, a string or a number.

- There are eight basic data types in JavaScript. Here, we’ll cover them in general and in the next chapters we’ll talk about each of them in detail.
    1. Number
    2. BigInt
    3. String
    4. Boolean(logical type)
    5. "null" value
    6. "undefined" value
    7. Objects
    8. Symbols

## typeof operator
- The typeof operator returns the type of the operand. It’s useful when we want to process values of different types differently or just want to do a quick check.
- Syntax - typeof variableName

# Interaction : alert, prompt, confirm
1. alert
- The mini-window with the message is called a modal window. The word “modal” means that the visitor can’t interact with the rest of the page, press other buttons, etc, until they have dealt with the window. In this case – until they press “OK”.

2. prompt
- It shows a modal window with a text message, an input field for the visitor, and the buttons OK/Cancel.

    title
        The text to show the visitor.
    default
        An optional second parameter, the initial value for the input field. 

3. confirm
- The function confirm shows a modal window with a question and two buttons: OK and Cancel.

- The result is true if OK is pressed and false otherwise.

## Tasks
- [x] create a web page that asks for a name and outputs it

# Type conversions
- Most of the time, operations and functions automatically convert the values given to them to the right type.
- For example, alert automatically converts any value to a string to show it. Mathematical operations convert values to numbers.
- There are also cases when we need to explicitly convert a value to the expected type.

## String conversion
- String conversion happens when we need the string form of the value.
- We can String(value) function to convert a value to a string.

```js
let value = true;
alert(typeof value);    // boolean

value = String(value);      // now value is a string
alert(typeof value);
```

## Numeric conversion
- Numeric conversion in mathematical functions and expressions happens automatically.
- We use Number(value) function to explicitly convert a value to a number.

```js
let str = "124";
alert(typeof str);      // string

let num = Number(str);      // becomes a number 124
alert(typeof num);
```

## Boolean conversion
- Boolean conversion is the simplest one.
- It happens to logical operations but can also be performed explicitly with a call to Boolean(value).

- The conversion rules:
    - Values that are intuitively "empty", like 0, an empty string, null, undefined, and NaN becomes false.
    - Other values become true.