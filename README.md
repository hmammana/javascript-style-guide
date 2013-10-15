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
- We use 4 spaces over tabs for indentation.
- We don't put whitespace at the end of line or on blank lines.
- We don't mix spaces and tabs.

## Commas & Semicolons

### Commas
- We put the comma at the end of the line.
    
    ```js
    // Good :)
    var foo,
        bar,
        foobar;

    // Good :)
    var map = {
        'foo': 'foo',
        'bar': 'bar',
        'foobar': 'foobar'
    };
    
    // Bad :(
    var foo
      , bar
      , foobar;

    // Bad :(
    var map = {
        'foo': 'foo'
      , 'bar': 'bar'
      , 'foobar': 'foobar'
    };
    ```

### Semicolons

- We always put a semicolon at the end of the line.
    ```js
    // Good :)
    (function () {
        var foo = 'foobar';
        return foo;
    }());

    // Bad :(
    (function () {
        var foo = 'foobar'
        return foo
    }())
    ```

- We don't put semicolons at the end of
    - loops statements (`for`, `for...in`, `while`, `do...while`)

        ```js
        // Good :)
        for (var i = 0; i < 10; i += 1) {
            console.log('foobar');
        }
        
        // Bad :(
        for (var i = 0; i < 10; i += 1) {
            console.log('foobar');
        };
        ```
        
    - conditionals statements (`if...else`, `switch`)

        ```js
        // Good :)
        if (foo !== undefined) {
            console.log('foobar');
        }
        
        // Bad :(
        if (foo !== undefined) {
            console.log('foobar');
        };
        ```
        
    - funcions declarations

        ```js
        // Good :)
        function foo() {
            console.log('foobar');
        }
        
        // Bad :(
        function foo() {
            console.log('foobar');
        };
        ```

## Literals

- We use the array literal notation.
    ```js
    // Good :)
    var foo = [];
    
    // Bad :(
    var foo = new Array();
    ```

- We use the object literal notation.
    ```js
    // Good :)
    var foo = {};
    
    // Bad :(
    var foo = new Object();
    ```

## Operators
### [WIP]

## Variables
### [WIP]

## Functions
### [WIP]

## Hoisting
### [WIP]

## Loops

### for

- We declare variables outside of the for statement.
- We dont't use the increment operator.
- We don't calculate the length on each iteration.
- We don't put semicolon at the end of the for statement.

    ```js
    // Good :)
    var x,
        i = 0,
        len = foo.length;
        
    for (x in foo) {
        console.log('foobar');
    }

    for (i; i < len; i += 1) {
        console.log('foobar');
    }

    // Bad :(
    for(var x in foo){
        console.log('foobar');
    };

    for(i = 0; i < foo.length; i++){
        console.log('foobar');
    };
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
