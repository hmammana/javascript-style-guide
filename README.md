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
- Operators
- Variables
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
### [WIP]

## Variables
### [WIP]

```js
// Bad
var foo;
var bar;
var foobar;

// Good
var foo,
    bar,
    foobar;
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

for (i; i < len; i += 1) {
    console.log('foobar');
}

// Good
var x;

for (x in foo) {
    console.log('foobar');
}
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
