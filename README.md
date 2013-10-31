# JavaScript Style Guide

MercadoLibre JavaScript Style Guide.

## Intro
The main goal of this guide is to set standards for writing and scaffolding our JavaScript files and modules, helping the readability and maintainability of our code. By doing this, we can significantly reduce the time required to understand any front-end implementation.

By writing clean code, we are able to:

- achieve a code that’s easier to understand;
- detect errors and potential problems;
- easily identify what code can be reused;
- build or update any functionality on any code already implemented;
- work on any file regardless of who wrote it.

> "Consistent code, even when written by a team, should look like one person wrote it."
by [Addy Osmani](http://addyosmani.com/blog/javascript-style-guides-and-beautifiers/)

## Table of contents

- Scaffolding
- Comments 
- [Spacing](#spacing)
- [Commas & Semicolons](#commas--semicolons)
- [Literals](#literals)
- [Operators](#operators)
- [Variables](#variables)
- Functions
- Hoisting
- [Loops](#loops)
- Events
- Control Flow / Conditionals
- Modules

## Scaffolding
### [WIP]

## Comments 
### [WIP]

## Spacing
- Use 4 spaces for indentation. Don't use tabs.
- Don't mix spaces and tabs.
- Don't put whitespace at the end of line or on blank lines.

```js
// Bad
function foo() {
----console.log('foobar');
};

// Bad
function foo() {
··console.log('foobar');
};

// Bad
function foo() {
    console.log('foobar');····
};··

// Good!
function foo() {
····console.log('foobar');
};
```

## Commas & Semicolons

### Commas
- Put the comma at the end of the line.
- Don't put the comma at the end of the last property.
    
```js
// Bad
var map = {
    'foo': 'foo'
  , 'bar': 'bar'
  , 'foobar': 'foobar'
};

// Bad
var map = {
    'foo': 'foo',
    'bar': 'bar',
    'foobar': 'foobar',
};

// Good :)
var map = {
    'foo': 'foo',
    'bar': 'bar',
    'foobar': 'foobar'
};
```

### Semicolons

- Always put a semicolon at the end of the line.
    ```js
    // Bad
    (function () {
        var foo = 'foobar'
        return foo
    }())

    // Good
    (function () {
        var foo = 'foobar';
        return foo;
    }());
    ```

- Don't put semicolons at the end of
    - loops statements (`for`, `for...in`, `while`, `do...while`)

        ```js
        // Bad
        for (var i = 0; i < 10; i += 1) {
            console.log('foobar');
        };

        // Good
        for (var i = 0; i < 10; i += 1) {
            console.log('foobar');
        }
        ```
        
    - conditionals statements (`if...else`, `switch`)

        ```js
        // Bad
        if (foo !== undefined) {
            console.log('foobar');
        };

        // Good
        if (foo !== undefined) {
            console.log('foobar');
        }
        ```
        
    - funcions declarations

        ```js
        // Bad
        function foo() {
            console.log('foobar');
        };

        // Good
        function foo() {
            console.log('foobar');
        }
        ```

## Literals

- Use the array literal notation.
    ```js
    // Bad
    var foo = new Array();

    // Good
    var foo = [];
    ```

- Use the object literal notation.
    ```js
    // Bad
    var foo = new Object();

    // Good
    var foo = {};
    ```

## Operators

### Logical

- Use one space between operators.
    ```js
    // Bad
    foo||bar;

    // Good
    foo·||·baz;
    ```

### Arithmetic

- Use the assignment operator instead the increment or decrement operator.
    ```js
    // Bad
    foo++;

    // Good
    foo += 1;
    ```

- Use one space between operators.
    ```js
    // Bad
    (1+2)*3;

    // Good
    (1·+·2)·*·3;
    ```

## Variables

- Don't use global variables.
- Name it in *lowerCamelCase*.
- Use one space before and after assignment.
    ```js
    // Bad
    var foo='bar';

    // Good
    var foo·=·'bar';
    ```

- Declare many variables in one statement. Use different lines for each variable.
    ```js
    // Bad
    var foo;
    var bar;
    var baz;

    // Bad
    var foo, bar, baz;

    // Good
    var foo,
        bar,
        baz;
    ```

- Begin with $ the name of variables that contains a jQuery/Zepto element.
    ```js
    // Bad
    var container = $('#foo');

    // Good
    var $container = $('#foo');
    ```

- Define all variables on top.
    ```js
    // Bad
    var foo;
    bar();
    var baz = 'example';

    // Good
    var foo,
        baz;
    bar();
    baz = 'example';
    ```

## Functions
### [WIP]

## Hoisting
### [WIP]

## Loops

### for

- Declare variables outside of the for statement.
- Dont't use the increment operator.
- Don't calculate the length on each iteration.
- Don't put semicolon at the end of the for statement.
- Put a space between 'for' and '('.
- Put a space between ')' and '{'.

```js
// Bad
for(i = 0; i < foo.length; i++){
    console.log('foobar');
};

// Bad
for(var i = 0; i < foo.length; i++){
    console.log('foobar');
};

// Bad
for(x in foo){
    console.log('foobar');
};

// Bad
for(var x in foo){
    console.log('foobar');
};

// Good
var i = 0,
    len = foo.length;

for·(i; i < len; i += 1)·{
    console.log('foobar');
}

// Good
var x;

for·(x in foo)·{
    console.log('foobar');
}
```

### while
- Don't calculate the length on each iteration.
- Don't put semicolon at the end of the for statement.
- Put a space between 'while' and '('.
- Put a space between ')' and '{'.

```js
// Bad
var i = 0;

while(i < foo.length){
    console.log('foobar');
    i++;
};

// Good
var i = 0;

while·(i < foo.length)·{
    console.log('foobar');
    i += 1;
}
```

### do...while
- Put semicolon at the end of the do...while statement.
- Don't calculate the length on each iteration.
- Put a space between 'do' and '{'.
- Put a space between '}' and 'while'.
- Put a space between 'while' and '('.
- Put a space between ')' and '{'.

```js
// Bad
var i = 0;

do{
   i++;
   document.write(i);
}while (i < 5)

// Good
var i = 0;

do·{
   i += 1;
   document.write(i);
}·while·(i < 5);
```

### forEach
- Use `forEach` statement to iterate an array.

```js
arr.forEach(function (x) {
    console.log(x);
});
```

## Events
### [WIP]

## Control Flow / Conditionals
### [WIP]

## Modules
### [WIP]


## License

Licensed under the MIT license.

Copyright (c) 2013 MercadoLibre, http://www.mercadolibre.com/
