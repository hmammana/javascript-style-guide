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
- Indentation
- [Commas & Semicolons](#commas--semicolons)
- Built-in Object
- Operators
- Variables
- Functions
- Hoisting
- Loops
- Events
- Control Flow / Conditionals
- Modules

## Scaffolding
### [WIP]

## Comments 
### [WIP]

## Indentation
### [WIP]

## Commas & Semicolons

### Commas
- We always put the comma at the end of the line.
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
    ```
- We don't use "Comma-First" style.
    ```js
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
    // Bad :(
    (function () {
        var foo = 'foobar'
        return foo
    }())

    // Good :)
    (function () {
        var foo = 'foobar';
        return foo;
    }());
    ```

## Built-in Object
### [WIP]

## Operators
### [WIP]

## Variables
### [WIP]

## Functions
### [WIP]

## Hoisting
### [WIP]

## Loops
### [WIP]

## Events
### [WIP]

## Control Flow / Conditionals
### [WIP]

## Modules
### [WIP]


## License

Licensed under the MIT license.

Copyright (c) 2013 MercadoLibre, http://www.mercadolibre.com/
