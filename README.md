# JavaScript

Someone told me that [I don't know JS](https://github.com/getify/You-Dont-Know-JS), but ...

![](https://media.giphy.com/media/tnasbNAUBlDC8/giphy.gif)

In all seriousness, these are the personal notes I took while learning JavaScript. I'll continue to occasionally add to them, and PRs are accepted if you want to add to them, too!

- [JavaScript](#javascript)
  * [Primitives](#primitives)
    + [Strings](#strings)
      - [Concatenation](#concatenation)
    + [Numbers](#numbers)
      - [Arithmetic operators](#arithmetic-operators)
  * [Objects basics](#objects-basics)
    + [Arrays](#arrays)
    + [Accessing object internals](#accessing-object-internals)
  * [Falsiness](#falsiness)
  * [Expressions](#expressions)
  * [Statements](#statements)
  * [Equality](#equality)
  * [Mutability](#mutability)
    + [Primitives](#primitives-1)
  * [Objects](#objects)
  * [Conversion](#conversion)
  * [Global object](#global-object)
  * [Variable hoisting](#variable-hoisting)
    + [ES6 and variable scoping](#es6-and-variable-scoping)
  * [Functions](#functions)
    + [Function parameters](#function-parameters)
    + [Scope](#scope)
    + [function scope and params](#function-scope-and-params)
    + [Examples of global/function scoping principles](#examples-of-globalfunction-scoping-principles)
    + [First class objects](#first-class-objects)
    + [Function expressions vs. declarations](#function-expressions-vs-declarations)
    + [Function Hoisting](#function-hoisting)
    + [Iteration](#iteration)
    + [IIFE](#iife)
    + [Callbacks](#callbacks)
      - [Reduce - A form reduction example](#reduce---a-form-reduction-example)
    + [Pure functions](#pure-functions)
    + [Meta-programming functions](#meta-programming-functions)
  * [Objects](#objects-1)
    + [`this`](#this)
    + [Cloning / copying objects](#cloning--copying-objects)
      - [Shallow copies](#shallow-copies)
      - [Deep nesting](#deep-nesting)
    + [Factory functions](#factory-functions)
    + [Constructors](#constructors)
    + [Object literals and constructors](#object-literals-and-constructors)
    + [Prototype](#prototype)
      - [Methods to test prototype relationships](#methods-to-test-prototype-relationships)
      - [Object.create(obj)](#objectcreateobj)
    + [Prototypes & "Inheritance"](#prototypes--inheritance)
      - [Prototype chain](#prototype-chain)
    + [Prototypal inheritance](#prototypal-inheritance)
      - [Benefits of prototype inheritance](#benefits-of-prototype-inheritance)
    + [Methods can be overridden locally](#methods-can-be-overridden-locally)
      - [`Object.getOwnPropertyNames` and `object.hasOwnProperty`](#objectgetownpropertynames-and-objecthasownproperty)
      - [Shadowing properties](#shadowing-properties)
    + [Prototype accessor/shortcut](#prototype-accessorshortcut)
    + [Constructors + prototype chain](#constructors--prototype-chain)
      - [Directly setting prototypes](#directly-setting-prototypes)
      - [Constructor prototypes](#constructor-prototypes)
    + [Constructors and prototype internals](#constructors-and-prototype-internals)
    + [Frozen non-writeable methods & properties](#frozen-non-writeable-methods--properties)
    + [OLOO vs Pseudoclassical](#oloo-vs-pseudoclassical)
      - [The Pseudo-classical Pattern](#the-pseudo-classical-pattern)
      - [OLOO Pattern](#oloo-pattern)
  * [Functions Pt. II (contexts)](#functions-pt-ii-contexts)
    + [Execution contexts](#execution-contexts)
    + [Global Object](#global-object)
      - [ES6 globals](#es6-globals)
    + [Implicit function execution context](#implicit-function-execution-context)
    + [Explicit function execution: `call`, `apply`, and `bind`](#explicit-function-execution-call-apply-and-bind)
    + [Bound functions](#bound-functions)
  * [Loosing context](#loosing-context)
    + [Method Losing Context when Taken Out of Object](#method-losing-context-when-taken-out-of-object)
      - [Solution 1: Passing context](#solution-1-passing-context)
      - [Solution 2: Binding the function](#solution-2-binding-the-function)
      - [Solution 3: Add function as object method](#solution-3-add-function-as-object-method)
    + [Internal function losing method context](#internal-function-losing-method-context)
      - [Solution 1: Preserve context with a local variable](#solution-1-preserve-context-with-a-local-variable)
      - [Solution 2: Pass context](#solution-2-pass-context)
      - [Solution 3: Bind the context with a function expression](#solution-3-bind-the-context-with-a-function-expression)
    + [Similar problem: Outer Function Referenced By Object Method Lacks Context](#similar-problem-outer-function-referenced-by-object-method-lacks-context)
    + [Function as Argument Losing Surrounding Context](#function-as-argument-losing-surrounding-context)
      - [Solution 1: self = this fix](#solution-1-self--this-fix)
      - [Solution 2: Bind the argument function with the surrounding context](#solution-2-bind-the-argument-function-with-the-surrounding-context)
      - [this.arg vs. context manipulation - forEach, some, every, map](#thisarg-vs-context-manipulation---foreach-some-every-map)
    + [Nested object losing context](#nested-object-losing-context)
    + [Indirect invocation](#indirect-invocation)
  * [Function closures](#function-closures)
    + [Nesting](#nesting)
    + [Objects, functions, and closure](#objects-functions-and-closure)
    + [Lexical Scoping](#lexical-scoping)
    + [Shadowing](#shadowing)
    + [Persistent reference](#persistent-reference)
    + [Factory patten](#factory-patten)
    + [Closure types](#closure-types)
      - [Creating an IIFE closure](#creating-an-iife-closure)
    + [Closures, callbacks & additional arguments](#closures-callbacks--additional-arguments)
    + [Closures & OOP](#closures--oop)
    + [Partial application](#partial-application)
  * [Garbage collection](#garbage-collection)
  * [DOM](#dom)
    + [DOM Structure](#dom-structure)
    + [Traversing DOM](#traversing-dom)
      - [Nodes](#nodes)
    + [Elements](#elements)
      - [Searching by CSS selector](#searching-by-css-selector)
    + [Interacting with the DOM](#interacting-with-the-dom)
      - [Element Attribute](#element-attribute)
    + [Attribute properties](#attribute-properties)
    + [href](#href)
    + [classList](#classlist)
    + [style](#style)
    + [Modifying element text](#modifying-element-text)
    + [Creating nodes](#creating-nodes)
    + [Adding nodes to DOM](#adding-nodes-to-dom)
    + [Removing nodes](#removing-nodes)
    + [Events](#events)
      - [Adding event listeners](#adding-event-listeners)
      - [Removing EventListeners](#removing-eventlisteners)
    + [Page life-cycle events](#page-life-cycle-events)
    + [User events](#user-events)
      - [Mouse events](#mouse-events)
      - [Keyboard events](#keyboard-events)
    + [Event object](#event-object)
    + [Capturing and bubbling](#capturing-and-bubbling)
    + [Delegation](#delegation)
    + [Event loop](#event-loop)
      - [Event loop / closure bug](#event-loop--closure-bug)
      - [IIFE solution](#iife-solution)
      - [ES6 solution](#es6-solution)
  * [XML HTTP Requests](#xml-http-requests)
  * [Window](#window)
    + [`Window.history`](#windowhistory)
    + [`Window.location`](#windowlocation)
  * [Tricks](#tricks)
    + [Make a copy of something (like an object)](#make-a-copy-of-something-like-an-object)
    + [Make N length string**](#make-n-length-string)
    + [Make an N length array of letters](#make-an-n-length-array-of-letters)
    + [Make an empty iterable array](#make-an-empty-iterable-array)
    + [Make an N-1 length array of integers](#make-an-n-1-length-array-of-integers)
    + [`toString()` to determine an object's type**](#tostring-to-determine-an-objects-type)
    + [Logging](#logging)
  * [Debugging](#debugging)
  * [Preventing errors](#preventing-errors)
  * [jQuery](#jquery)
    + [Basics](#basics)
      - [Loading the dom](#loading-the-dom)
      - [Chaining](#chaining)
    + [Creating elements](#creating-elements)
    + [jQuery vs. vanilla JS](#jquery-vs-vanilla-js)
    + [Traversal](#traversal)
      - [jQuery specific selectors](#jquery-specific-selectors)
      - [`filter()`](#filter)
    + [Other search methods](#other-search-methods)
      - [CSS attribute matchers](#css-attribute-matchers)
    + [`closest()` vs. `parents()`](#closest-vs-parents)
    + [`index()`](#index)
    + [`each()` method](#each-method)
    + [`eq()`](#eq)
    + [Form management](#form-management)
      - [Grabbing input from an input field](#grabbing-input-from-an-input-field)
      - [Resetting a form](#resetting-a-form)
      - [Getting data from a form](#getting-data-from-a-form)
      - [`prop()` - setting a checked radio](#prop---setting-a-checked-radio)
    + [Other traversal methods](#other-traversal-methods)
    + [DOM display values](#dom-display-values)
      - [`position()` vs. `offset()`](#position-vs-offset)
      - [`height()` vs. `innerHeight()`](#height-vs-innerheight)
    + [DOM manipulation](#dom-manipulation)
      - [`css()` method](#css-method)
      - [Scroll position - `scrollTop()`](#scroll-position---scrolltop)
      - [`prepend()` vs. `prependTo()`](#prepend-vs-prependto)
    + [jQuery patterns](#jquery-patterns)
      - [Modal toggling](#modal-toggling)
      - [Tabular navigation](#tabular-navigation)
    + [Animations](#animations)
      - [fade animations](#fade-animations)
      - [slide animations](#slide-animations)
      - [`animate`](#animate)
    + [Stoping animations](#stoping-animations)
    + [Events](#events-1)
      - [Page load vs. events](#page-load-vs-events)
      - [Event types](#event-types)
      - [Callbacks](#callbacks-1)
      - [Delegated events](#delegated-events)
        * [Automatically listen for new elements](#automatically-listen-for-new-elements)
        * [Efficient event handling](#efficient-event-handling)
        * [Cleaning up conditional logic](#cleaning-up-conditional-logic)
      - [Namespaced events](#namespaced-events)
      - [Clearing events](#clearing-events)
      - [Stopping event propogation](#stopping-event-propogation)
      - [Specifying a default event on page load with `on()`](#specifying-a-default-event-on-page-load-with-on)
    + [Functions](#functions-1)
      - [`proxy`](#proxy)
    + [Ajax](#ajax)
      - [Organizing ajax calls in objects](#organizing-ajax-calls-in-objects)
    + [Binding ajax method calls as event handlers - extending objects](#binding-ajax-method-calls-as-event-handlers---extending-objects)
    + [Good jquery code](#good-jquery-code)
      - [Variable naming](#variable-naming)
      - [Meaningful function names](#meaningful-function-names)
      - [Reduce function calls](#reduce-function-calls)
      - [Code brevity](#code-brevity)
      - [Efficiency](#efficiency)
    + [Troubleshoting](#troubleshoting)
    + [HTML Data Attributes](#html-data-attributes)
      - [Get or set the value of an HTML data attribute](#get-or-set-the-value-of-an-html-data-attribute)
      - [Set and retrieve custom data on an element after the page has been rendered](#set-and-retrieve-custom-data-on-an-element-after-the-page-has-been-rendered)
      - [Hyphenated data properties](#hyphenated-data-properties)
  * [Handlebars](#handlebars)
    + [Precompiled scripts](#precompiled-scripts)
  * [Localstorage](#localstorage)
  * [ES6](#es6)
    + [`let` and `const`](#let-and-const)
      - [`let`](#let)
      - [`const`](#const)
    + [Shorthand property declaration](#shorthand-property-declaration)
    + [Splat operator](#splat-operator)
      - [Combining / Gathering](#combining--gathering)
      - [Objects](#objects-2)
      - [Values](#values)
    + [Destructuring](#destructuring)
      - [Object properties](#object-properties)
      - [Using destructuring to make method invocations clearer](#using-destructuring-to-make-method-invocations-clearer)
      - [Optional args object](#optional-args-object)
    + [Rest](#rest)
    + [Spread](#spread)
    + [Arrow functions](#arrow-functions)
      - [Abbreviated function syntax](#abbreviated-function-syntax)
      - [Automatic context binding](#automatic-context-binding)
    + [Classes](#classes)
    + [Module import / export](#module-import--export)
    + [Generator function](#generator-function)
    + [Running babel from the command line](#running-babel-from-the-command-line)
  * [Linting](#linting)
    + [Airbnb rules (ES5)](#airbnb-rules-es5)
  * [Node](#node)
    + [Setup](#setup)

## Primitives

* number
* string
* boolean
* null
* undefined

Primitives are immutable

```js
a = 'hello';
a.toUpperCase();    // "HELLO"
a;                  // 'hello'
```

### Strings

You can compare strings, which is interesting

```js
'a' < 'b';        // true
'Ant' > 'Falcon'; // false
```

Character | Output
----| --------
\n | New line
\t	| Tab
\r	| Carriage return
\v	| Vertical tab
\b	| Backspace

#### Concatenation

Example of strange concatenation behavior.

JavaScript strings automatically concatenate Integers and Strings together without throwing an exception.

```js
> 2 + "two"
< "2two"
```

**Number => String**

This also leads to the simplest way to convert a number

```js
> 12 + ""
< "12"
```

Although it may be more explicit to do this

`Number(12)`

Other mathemetical operands will not work in this way

```js
"123" * 3       //369
"8" - "1"       // 7
```

**String => Number**

```js
`Number('12')`
> 12
```

Or you can use a shorthand

```
+'12'
> 12
```

**Formatting long strings**

Concatenation is also useful for formatting multiline strings in JavaScript

```js
var lipsum = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do " +
             "eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut "
```

This method uses escaping newline characters

```js
var lipsum = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do \
eiusmod tempor incididunt ut labore et dolore magna aliqua."
```

**ES6 - Concatenation**

In ES6 you can use interpolation to combine variables and strings.

```js
let name = "world"
console.log(`Hello ${name}`)
```

### Numbers

Use whole numbers (1 cent rather than .01 dollars) - division with floats is less precise.

`0.1 + 0.2;   // returns 0.30000000000000004, not 0.3!`

* `Infinity`: when you need a number that's greater than all other numbers
* `-Infinity`: when you need a number that's less than all other numbers
* `NaN`: typically a math function failed

#### Arithmetic operators

**Modulo**

Often the `%` represents a modulo operator, but in JS it's actually [remainder] operator(https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators#Remainder_()). To demonstrate the differences between the two, let's look at how `10 % -3` would be treated in each case:

```js
var a = 10;
var b = -3;
var remainder = a - (Math.trunc(a/b) * b);  // 10 - -4 * -3 => 2
var modulo = a - (Math.floor(a/b) * b);     // 10 - -3 * -3 => -2
```

The difference here is that a remainder is using `trunc` and a modulo would use `floor`.

```js
> Math.trunc(-3.333)
-3
> Math.floor(-3.333);
-4
```

## Objects basics

### Arrays

**Removing a value**

```js
var arr = [0,1,2];
arr.splice(0,1)   // 0
arr               // [1,2]
```

**Getting an object's keys**

`keys = Object.keys(obj)`

### Accessing object internals

**Use bracket notation with variables and integers**

The key in the `[]` must be a string value. If a variable is placed in the brackets, it will use the value of the variable (converted to a string if necessary) as the key to look up.

```js
var obj = { a: 1, "b": 2, 1: 3, $1: 4 }
obj.a    // 1
obj[a]   // Reference Error
obj["a"] // 1

obj.b    // 1
obj[b]   // Reference Error
obj["b"] // 1

obj[1]   // 3
```

In the examples above, `Referrence Error` happens because `a` and `b` are not instantiated variables.

An integer can serve as an object key, but you cannot use it with the object dot notation. From the [MDN docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Property_accessors#Dot_notation)

> To use dot notation, the property must be a valid JavaScript identifier, i.e. a sequence of alphanumerical characters, also including the underscore (`_`) and dollar sign (`$`), that cannot start with a number. For example, `object.$1` is valid, while `object.1` is not.

```js
// continued
obj.1     // Error
obj.$1   // 4
```

**Access object property with a string**

```js
firstKey = "name";
var lead = { name : "Me", email: "me@domain.com" };
lead[firstKey]  // "Me"  (lead.firstKey would not work - it would like for firstKey as a key)
lead.name       // "Me"
```

**Iterating through an object's keys**

`for (var property in obj) { ... }`

Or if you need to return an array or make access the current index in a callback

```js
Object.keys(obj).map(function(key, index) {
  obj[key] = ... ;
});
```

## Falsiness

**Falsy values in JavaScript**

1. `0`  
2. `NaN` - Return value from a math operation involving `undefined`
3. `""`  
4. `undefined`
5. `null`
6. `false`

**`NaN` vs. `undefined` vs. `null`**

2) `NaN` - never equals any other value, including itself, so to test for NaN use the function isNaN.
3) `""`  
4) `undefine`d - a variable (or property or array item) hasn’t yet been initialized to a value.
5) `null` - "no object"

Some ways to test this out are below:

```js
!!(NaN)        // false
Boolean(0);    // false
```

## Expressions

Expression is any valid code that resolves to a value.

**Incrementing & Decrementing shorthand**

```js
b = a++;    // equivalent of "b = a; a++;". so now b is 1 and a is 2
c = ++a;    // equivalent of "++a; b = a;". so now c is 3 and a is 3
```

**Short circuting in Boolean operators**

`&&` - Returns `expr1` if it can be converted to `false`; otherwise, returns `expr2`.

In other words, if the first expression is falsey, then it doesn't need to evaluate the second value. If it's not falsey, returns the second value.

`||` - Returns `expr1` if it can be converted to `true`; otherwise, returns `expr2`.

```js
var a = 1;
var b = false;
a || (b = true); // b is still false after this, because (b = true) is never evaluated
# => 1
b && (a = false); // a is still true, because (a = false) is never evaluated
# => 2
```

## Statements

* Not meant to return a value (help with logic `if...else` or instantiation `var a;`)
* Cannot be part of an expression
* Statements are expressions

```js
// These both return errors. A statement cannot be part of an expression.
var c = (var a = 1);
var c = (a = 1);
```

## Equality

**Type coercion**

Implicit type coercion is an interesting feature of JS:

If two operands have different types, the equality operator (==) will try to convert one of the operands into another type before testing for equality.

```js
3 == "3"
true

3 === "3"
false
```

**Object equality**

Two variables containing objects are only equal if they reference the same object.

```js
// Arays are objects, too
var array = [1];
array === [1]; // false
```

Here's how you might compare two objects by using `JSON.stringify()`. In this case, each object is info on a flight route

```js
function isValidRoute(invalidRoutes, route) {
  var invalidRouteFound = invalidRoutes.filter(invalidRoute => {
    var invalidRouteValues = JSON.stringify(Object.values(invalidRoute));
    var routeValues = JSON.stringify(Object.values(route));
    return invalidRouteValues === routeValues;
  });

  return invalidRouteFound.length > 0;
}

isValidRoute(
  {"airline":24,"src":"DFW","dest":"YYA"},
  {"airline":24,"src":"DFW","dest":"YYA"}
)
```

## Mutability

### Primitives

The primitives are: numbers, strings, booleans, `null` and `undefined`. Everything else is an object.

```js
var name = "Dylan"; // string primitive
name.indexOf("D"); // temporarily an Object ???
```

Primitives are immutable, even in conversion (new value is returned)

```js
alpha[0] = 'z';     // "z"
alpha;              // "abcde"
```

This is also the case with primitves passed to functions

```js
function change(a) {
  a = 2;
  console.log(a);
}

var b = 1;
change(b);          // logs 2
console.log(b);     // logs 1
```

Variables don't hold values; they hold references to those values. _A Function can't change the value of a variable that is passed to it as an argument._

An object can have its internal values changed within a function without having the reference change. Read more below.

## Objects

Objects are mutable. Arrays are objects

```js
alpha[0] = 'z';       // "z"
alpha;                // [ 'z', 'b', 'c', 'd', 'e' ]
```

Objects passed to Functions can be modified by those functions

```js
function increment(thing) {
  thing.count += 1;
  console.log(thing.count);
}

var counter = { count: 0 };
increment(counter); // { count: 1 }
count               // { count: 1 }
```

If a Function can't change the value of a variable passed in, how is this possible?

> `increment` does not reassign `thing` (which is the same as `counter`). Instead, `increment` modifies a property of the Object: the `count` property. This alters the state of the object, but it does not create a new Object, so `thing` and `counter` continue to point to the same thing.

## Conversion

String => Number

```js
Number('12')
> 12
```

```js
+("12")
12
```

Object => Boolean

```js
Boolean('true')  // true
Boolean(0)       // false
```
Simpler method

```js
!!('abc') // true
!!(0)     // false
```

## Global object

Global variables are properties of the global `window` object

```js
var foo = 1;
window.foo;       // 1
```

```js
function bar() {
  return 1;
}

window.bar;       // function bar() { return 1; }
```

## Variable hoisting

Read the code and the comments below and try to figure out the answer.

```js
function help() {
  return a;        // This line returns undefined. Shouldn't it return a ReferenceError. Why is that?
  var a = "Help!"; // If you comment this code out, this function returns 123 instead of undefined.  Why?
}

var a = 123;  // undefined
help();
```

When variables are declared in Javascript, they are hoisted to the beginning of their current scope. Therefore, this is equivalent code to the snippet below:

```js
var a;

function help() {
  var a;
  return a;
  a = "Help!";
}

a = 123;
help();
```

The function returns `undefined` because `var a;` was hoisted to above the return expression, shadowing the global `123`. The function can access the global `123` because the global object is the implicit context.

**Blocks**

Local variables are scoped to functions in JavaScript, not blocks. Therefore the same behavior will be present for the following code

```js
function say(b) {
  if (b) {
   var a = 'hello from inside a block';
  }

  console.log(a);
}
var b = 0;

say(b);   // undefined
```

Without understanding this rule one would expect the code to have a `ReferrenceError` for a missing variable `a`.

### ES6 and variable scoping

ES6 variables, are not hoisted and will therefore throw a reference error if accessed too early.

```js
console.log( a );	// undefined
console.log( b );	// ReferenceError!

var a;
let b;
```

## Functions

There are four types of functions in JavaScript

1. `function invocation: alert('Hello World!')`
2. `method invocation: console.log('Hello World!')`
3. `constructor invocation: new RegExp('\\d')`
4. `indirect invocation: alert.call(undefined, 'Hello World!')`

**Terms**

_Function vs. method invocation_

If a receiver must be specified, it is a method. If no receiver needs to be specified, it is a function

_Function Invocation_

* Invocation is executing the code that makes up the body of a function (simply calling the function). For example `parseInt` function invocation is `parseInt('15')`.
* Context of an invocation is the value of `this` within function body.

Example:

`[1,5].join(',')` is not a function invocation, it's a method invocation.

The fact that join is defined as`Array.prototype.join` means that `join` is a method on the Array prototype.

_Function Definition_

??

```js
function () {
 console.log("hi")
}
```

**Return value**

Functions without a `return` statement return `undefined`

### Function parameters

* Calling a Function with too few or too many arguments does not raise an error.
* Within a Function, an argument that wasn't provided in the call will have the value `undefined`.

```js
function takeTwo(a, b) {
  console.log(a);
  console.log(b);
  console.log(a + b);
}

takeTwo(1);

// logs out:
1
undefined
NaN
```

### Scope

Scope of a function is a set of variables, objects, functions accessible within a function body.

```js
var bunnyName = "Flopsy";

function hippityHoppity() {
  console.log(bunnyName);
}

hippityHoppity();  // "Flopsy"
```

Variables defined in the global scope are accessible inside methods without being expressly passed in

**Variable local/global scoping**

A local variable has a seperate scope from a global one.

```js
var bunnyName = "Flopsy";

function hippityHoppity() {
  var bunnyName = "BUNSTER";
}

hippityHoppity();
console.log(bunnyName); // "Flopsy"
```

If you remove the `var`, however, then the method will access the global variable and modify it

```js
var bunnyName = "Flopsy";

function hippityHoppity() {
  bunnyName = "BUNSTER";
}

hippityHoppity();
console.log(bunnyName); // "BUNSTER"
```

This 'global shadowing' behavior will not happen if you pass the variable to the function as a parameter.

```js
var bunnyName = "Flopsy";

function hippityHoppity(bunnyName) {
  bunnyName = "BUNSTER";
}

hippityHoppity();
console.log(bunnyName); // "Flopsy"
```

Also, there needs to be an outer variable reference for the function scoped variable

```js
function hippityHoppity(bunnyName) {
  bunnyName = "BUNSTER";
}

hippityHoppity();
console.log(bunnyName); // Uncaught Reference Error
```

There rules are a bit different if you're passing in an object. JS is pass by value, but when passing in objects (i.e arrays) the value is the reference

```js
var bunnyNames = ["Flopsy", "Mopsy"];

function hippityHoppity(bunnyNames) {
  bunnyName[0] = "BUNSTER";
}

hippityHoppity();
console.log(bunnyNames); // "[BUNSTER, Mopsy]"
```

### function scope and params

**Primitives:** are passed in as **reference-by-value** - the function does not modify the passed in object.

```js
function lessExcitable(text) {
  return text.replace(/!+/g, '.');  // replaces ! with .
}

var message = 'Hello!';
lessExcitable(message);  // "Hello."
message;                 // "Hello!"
```

Assign values to variables instead.

**Objects:** are passed into functions using **pass-by-reference** - (kinda, the value is the reference) modifications to objects inside the function are destrutive

### Examples of global/function scoping principles

Functions can not only call global variables inside methods, they can also destructively modify global variables.

```js
var a = 1;

function Foo() {
  this.a = 2;
  this.bar = function() {
    console.log(this.a);
  };
  this.bar();
}

var foo = new Foo();

a               // 1
foo.bar();      // 2
Foo();          // 2
a               // 2

obj = {};
Foo.call(obj);  // 2
obj.bar();      // 2
```

Nondestructive  

* In `foo.bar()`, `bar` is called on the `foo` object which has access to `a`

Destructive  

* `Foo();` modified the global object so that `window.a = 2`
* `obj.bar();` will only return 2, because `Foo.call(obj)` permanently modified the obj already. If we would leave it out, then the result will be `Uncaught TypeError: obj.bar is not a function`.

### First class objects

Functions are first class objects, meaning they can be passed into other functions like other primitive objects.

`sort` is a flexible example of this:

```js
function compareSize(num1, num2) {
  return num1 - num2;
}

[5,3,8].sort(compareSize)
> [3,5,8]
```

The function could also be passed in as an anonymous function expression as well.

### Function expressions vs. declarations

```js
function outer() { return "hello world" }
var foo = outer;    // assign the function to another variable
foo();
```

Essentially, declarations are doing extra work by creating a variable behind the scenes. The variable obeys general scoping rules.

```js
function quack() {
  console.log("Quack!")
}
```

Expressions create a reference which needs to be handled (you usually assign it to a variable). You can assign functions to variables to invoke later.

```js
var fly = function() {
  console.log("Fly!");
}
```

Named function expressions can only access their name inside the function

```js
var hello = function foo() {
  console.log(typeof foo);  // function
};

hello();

foo();                      // Reference Error
```

One important distinction between function expressions vs. declarations is hoisting.

### Function Hoisting

**Function declarations hoisting**

Function declarations are defined first while function expressions are evaluated during code execution.

That's why line 2 (which is a call to a function declaration) does not throw an error.

```js
console.log(quack());

function quack() {
  return "Quack"
}
```

**Function expression hoisting**

But not function expressions

```js
console.log(fly); // undefined

var fly = function() {
  return "Fly!";
}
```

Function expression hoisting rules are the same as regular variables. The equivalent code looks like this:

```js
var fly;

console.log(fly);

var fly = function() {
  return "Fly!";
}
```

The same hoisting behavior happens with function assignment.

```js
console.log(hello());

var hello = function() {
  return 'hello world';
}

// "Uncaught TypeError: hello is not a function
```

Therefore as a rule you should:

* Declare functions before calling them.
* Declare variables on the top of the their scopes.

**Execution**

Code first looks for function declarations, and sets the function to the return value.

Function expressions are evaluated with the rest of the code.

### Iteration

**Short ciruiting loops**

It's possible to short circut iteration in a `for` loop

```js
function run() {
  for(var i = 1; i < 4; i++) {
    alert(i)
    if (i === 2) {
      return false;
    }
  }  
}

run()
// 1
// 2
```

The execution was short circuited before it could reach `3`.

It's not possible in a vanilla JS `forEach` callback.

```js
[1,2,3].forEach(function(v) {
	console.log(v);
	if (v === 2) {
    return false;
  }
});
// 1
// 2
// 3
```

If it was, the code would never have reached `3`. The reason this is is because a new function is created. This isn't necessaryily the case though for JS library's like jQuery or lodash. Read more [here](https://webapplog.com/breaking-bad-loops-in-javascript-libraries/).

### IIFE

Immediately invocated function expressions

Useful for creating your own private scope. For example, say you need to do a for loop in a messy piece of code where `i` or the name of the function might be defined already.

```js
function() {
  for(var i=0; i<100; i++) {
    console.log(i);
  }
})():
```

They don't have to be only function delcaration styles. Here's a simple example using a function expression and a parameter:

```js
var message = (function(name) {  
   return 'Hello ' + name + '!';
})('World');
console.log(message) // => 'Hello World!'
```

The first pair of parenthesis in `(function(name) {...})` is an expression that evaluates to a function object. The second pair of parenthesis is the name parameter's argument `'World'`.

If a method is assigned in function declaration, when it's invoked it counts as a function declaration.

```js
var otherFunction = obj.myFunction;  
otherFunction();     // function invocation
```

### Callbacks

*Functions that take a Function as an argument.*

This Function will be invoked for each element in the `Array` and allow the developer to define specifics about how the chosen abstraction should be implemented. Because it is "called back" later with each element, this `Function` is called a callback.

Gives you the ability not only to write a function to solve a specific problem, such as "iterate through an array and log out the elements", but to write an abstraction, such as "iterate through an array and do something". This allows you to focus on what to do with each element in the Array, and not concern itself with how to iterate through an `Array`.

Abstraction | Used To | Returns | Array Methods
-------------|--------|---------|---------------|
Iteration | Perform an operation on each element in an Array |	nothing | `forEach`
Filtering / Selection | Limit to a subset of elements |	new Array |	`filter`
Transformation | Compute a value for each element |	new Array | `map`
Ordering | Arrange elements by sorting | new Array| 	`sort`
Reducing / Folding | Iteratively compute a result using each element | single value | `reduce`, `reduceRight`
Interrogation | Determine if an Array's elements pass a test |	single value |	`every`, `some`

#### Reduce - A form reduction example

To demonstrate how `reduce` works, we'll go over a common task - gathering and manipulating form inputs.

In JS development you usually aren't going to rely on the form sending data to the server - instead you're going to grab it when an event handler fires. If you're using jQuery you might use `serializeArray()` to create an object for each  `input` field inside your event callback.

```html
<label> Starting Point
    <input type="number" name="startX" placeholder="x:">
    <input type="number" name="startY" placeholder="y:">
</label>

<label> Ending Point
     <input type="number" name="endX" placeholder="x:">
    <input type="number" name="endY" placeholder="y:">
</label>
```

```js
$(function() {

  // Called from inside form callback
  function getFormObject($form) {
    var $inputs = $form.serializeArray();
    console.log($inputs);
  }
  ...
});
// [Object, Object, Object, ... ]
```

Each object looks something like this `{ startX: 'foo', value: 'bar' }`. This structure nests the data a bit too deeply for convenient access, so you might combine all these into a single object with unique key/value pairs; i.e `{ startX: 'foo', startY: ... }`.

A common, and arguably still fairly readable way would be to iterate through and 'decorate' a new object.

```js
...
var formObject = {};

$inputs.forEach(function(item) {
  formObject[item.name] = item.value;
});

return formObject;
```

But maybe we want to work with [pure functions](), so this gives us a chance to learn about `reduce`. Here's an example of how:

```js
var formObject = $inputs.reduce(function(list, item) {
  formObject[item.name] = item.value;
  return formObject;
});

console.log(formObject);
```

Reduce returns an accumulator, which is be default the object that calls reduce (in this case `$inputs`). However, the output looks like this:

```js
{ endX : "3",  endY : "4", name : "startX", startY : "2", value : "1" }
```

But wait... why is `startX` instead `name`. Instead 1 existing as the value pair to `startX`, it's instead exists as it's own pair with `value` as the key. What's going on here?

As with many JS mysteries, the answer is revealed in the [MDN documentation on reduce](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce).

> `arr.reduce(callback, [initialValue])`

> The first time the callback is called, accumulator and currentValue can be one of two values. If initialValue is provided in the call to reduce, then accumulator will be equal to initialValue and currentValue will be equal to the first value in the array. If _no_ initialValue was provided, then *accumulator will be equal to the first value* in the array and *currentValue will be equal to the second*.

So we fell for the trap of assuming our accumulator was one thing ( an empty object) when it was actually another the first object (the `startX` key-value pair) in our collection. To correct this issue we simply supply an empty object as the initial value.

```js
var formObject = $inputs.reduce(function(list, item) {
  formObject[item.name] = item.value;
  return formObject;
}, {});
```

Which formats our values correctly this time :)

```js
...
console.log(formObject);
// { endX : "3", endY : "4", startX: "1", startY : "2" }
```

### Pure functions

**Pure functions** - a Function that doesn't cause any side effects when it is invoked

Functions can modify values outside of them, either by accessing variables defined in outer scopes or by mutating objects that were passed to the function as an argument.

### Meta-programming functions

An example of how you would iterativelly create a number of methods on a specific object

```js
var _ = function(element) {
  u = { .... }

  (["Boolean", "String", "Number"]).forEach(function(method) {
    _["is" + method] = function(obj) {
      return toString.call(obj) === ["object " + method];
    };
  });

  return u;
}

_.isBoolean(false) // true
```

## Objects

### `this`

* refers to the current execution context of a function
* is used to access properties defined on objects from inside that object

```js
var = {
 make: "Fiat",
 started: false,

 start: function () {
   this.started = true;
 }
};
```

### Cloning / copying objects

#### Shallow copies

Getting code like this to work isn't too hard

```js
object = { 'a': 1 };

new_object['a'] = 2;
new_object  // { 'a': 2 }
object      // { 'a' : 1 }
```

Here are the ways we could create `new_object` to accomplish this:

```js
new_object = Object.create(first);
new_object = Object.assign({}, first);
```

#### Deep nesting

Cloning deeply nested objects is a bit trickier.

```js
object = { 'a': 1 };
array = [object];

new_array[0]['a'] = 2
new_array // [{ 'a': 2 }]
array     // [{ 'a': 1 }]
```

How do we make this code work? It depends on how we create (clone or duplicated) `new_array`. We could try these two ways

```js
var new_array= array.slice(0);                     
new_array[0]['a'] = 2
array // [{ 'a': 2 }]
```

But this doesn't work. Here's a similar method

```js
var new_array = Array.prototype.slice.apply(array)
new_array[0]['a'] = 2
array // [{ 'a': 2 }]
```

These both copy references so they won't work. The same thing will happened with `Object.assign([], array)`. What does work is using JSON.

```js
var new_array = JSON.parse(JSON.stringify(array))
new_array[0]['a'] = 2
array // [{ 'a': 1 }]
```

**ES6**

The splat operator replaces apply, so we could try using that one as well. `let new_array = [...array]`. However, it too copies references.

```js
new_array[0]['a'] = 2
array // [{ 'a': 2 }]
```

### Factory functions

```js
function createPerson(firstName, lastName) {
  return {
    firstName: firstName,
    lastName: lastName || '',
    fullName: function() {
      return (this.firstName + ' ' + this.lastName).trim();
    }
  };
}
var person = createPerson('Jon', 'Doe');
```

* Help build objects using a template
* Built with all methods, which may be duplicative
* No way to know whether it's created from a factory function. Can't tell "type"

### Constructors

* Blueprint for creating objects.
* Do not need a return statement
* Can take functions as properties
* Use `new` and capitalization as conventions

When a function is called with the `new` keyword, the following happens:

1) A new object is created  
2) `this` in the function is pointed to the new object
3) the code in the function is executed  
4) `this` is returned if there's not an explicit return

```js
function Dog(name, weight) {
  this.name = name;
  this.weight = weight;
  this.getSize = function() {
    if (this.weight > 20) {
      return "large";
    } else {
      return "small";
    }
  }
}

var pippin = new Dog('Pippin', 20)
```

**`new` and the implicit context**

We can tell that `this` in the above function was a new object because the `window` object was unmodified after execution.

`window.getSize() // getSize is not a function`

However the outcome is different if we leave off the `new` keyword

```js
Dog("Sami", 30);
window.getSize();  // large
```

### Object literals and constructors

Although constructors are very useful, object literals still have a place. In particular, when your constructor has many parameters and/or you are only making one object.

A constructor that needs changing could look like this:

```js
function Car(make, model, year, color, passengers, convertible, mileage) {
  this.make = make;
  this.model = model;
  this.year = year;
  this.color = color;
  this.passengers = passengers;
  this.convertible = convertible;
  this.mileage = mileage;
  this.started = false;
}

var cadi = new Car("GM", "Cadillac", 1955, "tan", 5, false, 12893);
```

Change the literal to this:

```js
var cadiParams = { make: "GM",
                 model: "Caddilac",
                 year: 1955,
                 color: "tan",
                 passengers: 5,
                 convertible: false,
                 mileage: 12892 };
```

Now you can just pass in the literal to the constructor.

`function Car(cadiParams)`

And modify the constructor to make this work.

```js
function Car(params) {
  this.make = params.make;
  this.model = params.model;
  this.year = params.year;
  this.color = params.color;
  this.passengers = params.passengers;
  this.convertible = params.convertible;
  this.mileage = params.mileage;
  this.started = false;
}
```

### Prototype

All objects have a prototype chain, and a `prototype` property. When an object is created, it receives an internal prototype property (although it's possible for it to be blank - `Object.create(null)`) - which references another object.

What does this linkage do? If a property or method is called on an object which doesn't have that property itself, it will look up the prototype chain for the first instance of that property.

For example, an object literal's `prototype` property is the `Object.prototype` object, which provides object methods to all objects.

```js
var foo = {
  a: 1,
  b: 2
};                // created with object literal

foo.toString();   // [object Object]
```

`toString()` was not defined on `foo`, but it was defined on `Object.prototype.foo`. And as mentioned above, the fact that `foo`s prototype is `Object.prototype` gives it access to these methods.

```js
Object.getPrototypeOf(foo) === Object.prototype;  // true
```

#### Methods to test prototype relationships

**Setup**

```js
function Foo() {};
var a = new Foo();
```

* `a` object is the prototype object of the `Foo` object OR
* object `a` is created with object `Foo` as its prototype

Using a constructor changes the returned object's prototype to the constructor functions own prototype

We'll use `Object.isPrototypeOf(obj)` - which returns the prototype of object - to test that hypothesis

```js
Object.getPrototypeOf(a) === Foo.prototype // true
```

Each object created from calling `new Foo()` will end up (somewhat arbitrarily) `[[Prototype]]`-linked to this "Foo dot prototype" object.

```js
...
Foo.prototype.isPrototypeOf( a ); // true
```

This is essentially asking, in the entire `[[Prototype]]` chain of `a`, does `Foo.prototype` ever appear?

#### Object.create(obj)

You can create prototype chains with `Object.create` as well.

Here's the inverse of the prototype relationship testing examples from above, using `Object.create`.

```
var foo = {};

var a = Object.create(foo);
Object.getPrototypeOf(a) === foo;   // true
foo.isPrototypeOf(a);             // true
```

`Object.create(..)` creates a "new" object out of thin air, and links that new object's internal `[[Prototype]]` to the object you specify (`foo` in this case).

### Prototypes & "Inheritance"

Below are some stripped down examples that demonstrate a bit of the mechanics on how JS objects are linked along the prototype chain.

#### Prototype chain

```js
var foo = { a: 1, b: 2 };
var bar = Object.create(foo);
Object.getPrototypeOf(bar) === foo // true
bar.__proto__ === foo;             // true

//  `foo` object is the prototype (object) of the bar object

var baz = Object.create(bar);

Object.getPrototypeOf(foo) === Object.prototype;  // true
Object.getPrototypeOf(baz) === bar;               // true
foo.isPrototypeOf(baz);                     // true - because foo is on qux's prototype chain
```

### Prototypal inheritance

JavaScript objects inherit behavior from other objects. JS object linked on the prototype chain can share behavior. Below are some simple examples:

```js
function Dog() {
  this.species = "Dog";
}

Dog.prototype.speak = function() {
  console.log("Bark!")  
}

var rover = new Dog();
rover.speak();
```

When `speak()` is called on `rover`, it looks for any `speak()` method on the instance. When it can't find one, it looks on the prototype for one. This same things is done for properties on instances (like `rover.species`). Here are other formats to use if you want to create multiple methods on the `Dog` prototype:

1) To avoid repeating `Dog.prototype`, you might choose to assign an object literal to `Dog.prototype`:

```js
...
Dog.prototype = {
  speak: function() {
    console.log("Bark!")  
  },
  walk: function() {
    console.log("Walks")
  }
}
...
```

However, to use this code safely you should first understand why the following code won't work:

```js
function Dog() {
  this.species = "Dog";
}

var rover = new Dog();

Dog.prototype = {
  speak: function() {
    console.log("Bark!");
  }
}

rover.speak(): // Reference Error
```

The `Dog` prototype object was reassigned, and the `speak` method on `rover` still looks to the original prototype object for this method definition. Finding none, a `ReferenceError` is thrown.

There will be no error if:

* a) `rover` is instead instantiated on a line after the method `speak` is added to `Dog.prototype` (and before `rover.speak()` is called), or
* b) If the `speak` method was added to the existing `Dog.prototype`, rather than reassigning it (i.e,`Dog.prototype.speak =  function () {}`). Even if `rover` was created before the `speak` method was defined, `rover` would still look to its original prototype object and find `speak` defined there.

2) You can also pass in a (singleton / object literal) object to `Object.create()`:

```js
var dog = {
  say: function() {
    console.log(this.name + ' says Woof!');
  }
};

var fido = Object.create(dog);
fido.name = 'Fido';
fido.say();             // Fido says Woof!
```

The `say` method is found on `fido` object's prototype object, then called with context of `fido` object itself. This is roughly the basis for the OLOO pattern, which we go into more later.

#### Benefits of prototype inheritance

Objects can be created directly from other objects. Behaviors (methods) and state (properties) can be shared via the prototype chain.

* We can create dogs much more easily with the `dog` prototype - we don't have to duplicate `say` and `run` on every single dog object.
* If we need to add/remove/update behavior to apply to all dogs, we can just modify the prototype object, and all dogs will pick up the changed behavior automatically.

Objects on the bottom of the prototype chain can "delegate" requests to the upsteam objects to be handled.

### Methods can be overridden locally

```js
var dog = {
  say: function() {
    console.log(this.name + ' says Woof!');
  },
};
dog.name = 'Tim';

var fido = Object.create(dog);

fido.name = 'Fido';
fido.say = function() {
  console.log(this.name + ' says Woof Woof!');
}

fido.say();             // Fido says Woof Woof!
dog.say()               // Tim says Woof!
```

#### `Object.getOwnPropertyNames` and `object.hasOwnProperty`

```js
var foo = { a: 1 };
var bar = Object.create(foo);
bar.b = 2;

bar.hasOwnProperty('a');            // true
Object.getOwnPropertyNames(bar);    // ["b"]
```

**Other prototype methods**

`Object.prototype.toString()`: returns a string representation of the object
`Object.prototype.isPrototypeOf(obj)`: tests if the object is in another object's prototype chain
`Object.prototype.hasOwnProperty(prop)`: tests whether the property is defined on the object itself

#### Shadowing properties

Once you change the object's property, it is no longer a constructor (prototype?) derived property.

```js
var foo = {
  a: 2
};

var myObject = Object.create( foo );

foo.a; // 2
myObject.a; // 2

foo.hasOwnProperty( "a" ); // true
myObject.hasOwnProperty( "a" ); // false

myObject.a++; // oops, implicit shadowing!

foo.a; // 2
myObject.a; // 3

myObject.hasOwnProperty( "a" ); // true
```

Constructors have roughly the same delegation behavior - newly created do not "have" the property, but if the property is modified on that instance it changes"

```js
function Foo() {}

Foo.prototype.a = 2;

var foo = new Foo();
var bar = new Foo();

foo.hasOwnProperty( "a" ); // false
bar.hasOwnProperty( "a" ); // false

bar.a++
bar.hasOwnProperty( "a" ); // true
```

However with constructors the use of `this` copies the properties directly on the new linked objects, making newly created project "have" the property.

```js
function anotherObject() {
  this.a = 2;
}

var foo = new anotherObject();
var bar = new Foo();

foo.hasOwnProperty( "a" ); // true  ... but should be false    
bar.hasOwnProperty( "a" ); // false
```

### Prototype accessor/shortcut

`Array.prototype` \ `[]`

* `Array.prototype.slice.call(arguments)` vs. `[].slice.call(arguments)`

`Object.prototype` \ `{}`

Does not work in all cases

`Object.getPrototypeOf([]) === []              \\ false`
`Object.getPrototypeOf([]) === Array.prototype \\ true`

### Constructors + prototype chain

* Every function has a special `prototype` property.

A function's prototype property is only useful when the function is used as a constructor, in which case all objects that it constructs will have this special object set as their prototype. This is the reason why the constructor property of the constructed object points back to the constructor function.

```js
pippin.constructor;                              // function Dog(...)
pippin.constructor === Dog                       // true

Dog.prototype   // Object {} - the constructor function's prototype object
new Dog() === Dog.prototype                      // true

Dog.prototype.constructor                        // function Dog(...)
Dog.prototype.constructor === Dog                // true

Object.getPrototypeOf(pippin) === Dog.prototype  // true
pippin instanceof Dog;                           // true
```

Evidence that function prototype property without `new` keyword is not useful

```js
Object.getPrototypeOf(Dog)                    // function () {}
Dog.prototype                                 // Object {}
Object.getPrototypeOf(Dog) === Dog.prototype; // false

Object.getPrototypeOf(pippin)                                // Object {}
Object.getPrototypeOf(pippin) === Object.getPrototypeOf(Dog) // false
Object.getPrototypeOf(pippin) === Dog.prototype              // true
```

If we wanted to share the behavior of `Dog` with `Poodle`, you could manually set the constructor (prototype?).

```js
function Dog () {}

function Poodle () {}
Poodle.prototype = Object.create(Dog.prototype); // Worse, but also new Dog();
Poodle.prototype.type = "Poodle";

var poodle = new Poodle();
console.log(poodle instanceof Dog);     // true
console.log(poodle instanceof Poodle);  // true

poodle.constructor;                                 // f Dog() {}
poodle.constructor === Dog;                         // false - should be true?
Object.getPrototypeOf(poodle) === Poodle.prototype; // true
Dog.prototype.isPrototypeOf(poodle);                // true
```

The `Poodle` prototype is an instance of `Dog`, so `poodle` is linked to `Dog` on the prototype inheritance chain.

**Constructor vs. prototype**

Note that `poodle`s constructor is `Dog` but the prototype is `Poodle.prototype`. If you reset a constructor's prototype the constructor property won't always reliable.

**Modify the constructor prototype, not the constructed object**

We do `Poodle.prototype = Object.create(Dog.prototype)`, not `poodle.prototype = Object.create(Dog.prototype)`. An instance of the object is not writeable in this way. In ES6 you can use `Object.setPrototypeOf`.

#### Directly setting prototypes

**Don't share prototype references**

`Poodle.prototype` = `Dog.prototype` => not good

If you you start adding functions onto `Poodle.protoype` you'll be modifying `Dog.prototype`.

**Be careful of `Obj.prototype` = `new AnotherObj()`**

`Poodle.prototype` = `new Dog()` creates a separate, linked object but may execute unplanned code or delegate certain properties that you don't want attached.

**Using `Object.create`**

`Poodle.prototype = Object.create(Dog.protype` is a good way to go

Using `Object.create` "make a new 'Poodle dot prototype' object that's linked to 'Foo dot prototype'."

**Use `Object.setPrototypeOf` in ES6**

```js
// modifies existing `Bar.prototype`
Object.setPrototypeOf( Bar.prototype, Foo.prototype );
```

#### Constructor prototypes

`Object.getPrototypeOf(Dog)`    // `function () {}`

Every function is a Function object created from the Function Constructor and as such also has a prototype (`Function.prototype`).
Note that the prototype of a Function Object (i.e `Dog`) can not be modified, unlike objects constructed (i.e `dog`) from it.

**Proto**

* `__proto__` is an `[[Prototype]]` accessor
* `__proto__` returns `Object.getPrototypeOf`

**Object literal & prototype**

What do you do if you want to add a , well since `obj.prototype` is undefined you could use the `__proto__` method

### Constructors and prototype internals

```js
function Foo() {
    // ...
}

Foo.prototype.constructor === Foo; // true

var a = new Foo();
a.constructor === Foo; // true
```

The `Foo.prototype `object by default (at declaration time on line 1 of the snippet!) gets a public, non-enumerable property called `.constructor`, and this property is a reference back to the function (`Foo` in this case) that the object is associated with.

Moreover, we see that object `a` created by the "constructor" call `new Foo()` seems to also have a property on it called `.constructor` which similarly points to "the function which created it".

This is just unfortunate confusion. In actuality, the `.constructor` reference is also delegated up to `Foo.prototype`, which happens to, by default, have a `.constructor` that points at `Foo`.

The `.constructor` property on `Foo.prototype` is only there by default on the object created when `Foo` the function is declared. If you create a new object, and replace a function's default `.prototype` object reference, the new object will not by default magically get a `.constructor` on it.

```js
function Foo() { /* .. */ }

Foo.prototype = { /* .. */ }; // create a new prototype object

var a1 = new Foo();
a1.constructor === Foo; // false!
a1.constructor === Object; // true!
```

`a1` has no `.constructor` property, so it delegates up the `[[Prototype]]` chain to `Foo.prototype`. But that object doesn't have a `.constructor` either (like the default `Foo.prototype` object would have had!), so it keeps delegating, this time up to `Object.prototype`, the top of the delegation chain.

### Frozen non-writeable methods & properties

**Object.defineProperties()**

This function returns an object with an un-writeable `log` property

```js
function newPerson(name) {
  return Object.defineProperties({ name: name }, {
    log: {
      value: function() {
        console.log(this.name);
      },
      writable: false
    }
  });
}
var me = newPerson('Shane Riley');
me.log();     // Shane Riley
me.log = function() { console.log("Amanda Rose"); };
me.log();     // Shane Riley
```

**Object.freeze()**

* Object property values cannot be reassigned
* Internal property object values *can be* reassigned
* Unreversible operation on an object.

### OLOO vs Pseudoclassical

#### The Pseudo-classical Pattern

The Pseudo-classical pattern is a combination of the constructor pattern and the prototype pattern. With this pattern, we:

* use a constructor to set object states, and
* put shared methods on the constructor function's prototype:

```js
var Point = function(x, y) {            // capitalized constructor name as a convention
  this.x = x || 0;                      // initialize states with arguments
  this.y = y || 0;                      // 0 as default value
};

Point.prototype = {
  onXAxis: function() {  // shared behaviors added to constructor's prototype property
    return this.x === 0;
  },
  onYAxis: function() {  // can reassign prototype object (watch instanceof changes) or can add one by one, Point.prototype.onXAxis = function() {...}
    return this.y === 0;
  }
}

var pointA = new Point(30, 40);     // use new to create objects
var pointB = new Point(20);

console.log(pointA instanceof Point);            // use instanceof to check type
console.log(pointB instanceof Point);

console.log(pointA.distanceToOrigin());          // 50
console.log(pointB.onYAxis());                   // true
```

#### OLOO Pattern

Here JavaScript sheds its pretense to be a "class oriented" language, where it uses constructor functions as fake classes. Instead, it embraces its prototype based object model. With the OLOO pattern, we

* define the shared behaviors on a prototype object, then
* use `Object.create()` to create objects that inherit directly from that object, without going through the roundabout way that involves "constructors and their prototype properties" at all.

```js
var Point = {                       // capitalized name for the prototype as a convention
  x: 0,                             // default value defined on the prototype
  y: 0,

  onXAxis: function() {            // shared methods defined on the prototype
    return this.y === 0;
  },

  onYAxis: function() {
    return this.x === 0;
  },

  init: function(x, y) {          // optional init method to set states
    this.x = x;
    this.y = y;
    return this;
  },
};

var pointA = Object.create(Point).init(30, 40);
var pointB = Object.create(Point);

Point.isPrototypeOf(pointA);        // use isPrototypeOf to check type
Point.isPrototypeOf(pointB);

pointB.onXAxis();                   // true
```

## Functions Pt. II (contexts)

### Execution contexts

First-class Functions initially have no context when created; they receive a context when the program executes them.

In other words, `this` changes based on how a function is invoked, not how it was defined.

### Global Object

The global object `window` is the implicit function execution context for global functions and expressions

```js
var foo = 1;
function bar() { return 1; }

window.foo;       // 1
window.bar;       // function bar() { return 1; }
```

Global functions are defined on it such as `isNaN()`

`window.isNan() // function isNaN() { ... }`

**Deleting**

Properties defined on window **cannot be deleted** (sorta). You can delete global variables that you don't define, but NOT those that you did.

```js
var foo = 1;
bar = 2;

delete window.foo;    // false
delete window.bar;    // true

window.foo;           // 1
window.bar;           // undefined
```

#### ES6 globals

`let` and `const` variables aren't accessible by writing `window.variable` name.

### Implicit function execution context

```js
var object = {
  foo: function() {
    return "this here is: " + this;
  }
};

object.foo();         // "this here is: [object Object]"

bar = object.foo;
bar();               // "this here is: [object Window]"
```

This is an example that shows that the binding of a function and context object happens when the function is **executed**, not when the function is defined.

### Explicit function execution: `call`, `apply`, and `bind`

JavaScript provides tools to manipulate function context.

**`call`**

Simple example

```js
var obj = {
  a: 1,
  foo: function() {
    console.log(this.a);
  }
}

obj.foo();          // 1
var bar = obj.foo;
bar();             // undefined

var context = {
  a: 2  
}

bar.call(context); // 2
```

Using `call` to give a function context with mutliple parameters

```js
var iPad   = { name: 'iPad', price: 40000 },
var kindle = { name: 'kindle', price: 30000 };

function printLine(line_number, punctuation) {
  console.log(line_number + ': ' + this.name + ', ' + this.price / 100 + ' dollars' + punctuation);
}

printLine.call(iPad, 1, ';');        // "1: iPad, 400 dollars;"
printLine.call(kindle, 2, '.');      // "2: kindle, 300 dollars."
```

**`apply`**

The same example, except using `apply`

```js
printLine.apply(kindle, [2, '.']);
```

**Call**: Count the Commas (you have to count the number of arguments to match the called function)  
**Apply**: Arguments as Array

`apply` can reduce the length of function parameters by organizing them into an array

```js
function add (a, b, c, d, e, f, g, h, i) {
    return a + b + c + d + e + f + g + h + i;
}
var nums = [1,2,3,4,5,6,7,8,9];

console.log(add.apply(this, nums));             // 45
console.log(add.call(this, 1,2,3,4,5,6,7,8,9)); // 45
```

Here's a more realistic example with `Math.max`, which expects arguments of number like `Math.max(10,20)`

```js
var numbers = [1,2,3]
Math.max(numbers) # NaN
Math.max.apply(null, numbers)
=> 3
Math.max.apply(this, numbers)
=> 3
```

ES6 version would simply be:

```
Math.max(...numbers)
```

**`bind`**

`bind` permenantly binds the execution context so it cannot be reassigned

```js
var a = 'goodbye';

var object = {
  a: 'hello',
  b: 'world',
  foo: function() {
    return this.a + ' ' + this.b;
  }
};

object.foo();                         // 'hello world'

var bar = object.foo;
bar();                                // 'goodbye undefined'

var baz = object.foo.bind(object);
baz();                                // 'hello world'

var object2 = {
  a: 'hi',
  b: 'there'
};

baz.call(object2);
baz():                               // 'hello world'; - baz context is still bound to object
```

The context of `object` has been permanently bound to `baz()` (the method `object.foo`). Therefore `call` has no affect.

`bind` is a good option for fixing the loss of context problem because you can call it multiple times without having to use `call` or `self` each time.

### Bound functions

* A bound function is a function bind with an object.
* `.bind()` makes a permanent context link and will always keep it. A bound function cannot change its linked context when using `.call()` or `.apply()` with a different context. Even calling `bind` again has no effect.

```js
function getThis() {  
  'use strict';
  return this;
}
var one = getThis.bind(1);
one.call(2); // => 1  
one.bind(2)(); // => 1  
new one(); // => Object // Call the bound function as a constructor
```

Only `new one` was able to change the context.

## Loosing context

### Method Losing Context when Taken Out of Object

```js
var john = {
  first_name: "John",
  last_name: "Doe",
  greetings: function() {
    console.log("hello, " + this.first_name + ' ' + this.last_name);
  },
}

var foo = john.greetings;
foo();   // "hello, undefined undefined"
```

`foo.call(john)` will work, but won't work if `foo` is passed somewhere where it doens't have access to `john`

```js
function repeatThreeTimes(func) {
  func();       // can't do func.call(john), out of scope
  func();
  func();
}

function foo() {
  var john = {
    first_name: "John",
    last_name: "Doe",
    greetings: function() {
      console.log("hello, " + this.first_name + ' ' + this.last_name);
    },
  }

  repeatThreeTimes(john.greetings);
};

foo();        
// "hello, undefined undefined"
// "hello, undefined undefined"
// "hello, undefined undefined"

foo.call(john);
// ReferenceError: john is not defined
```

#### Solution 1: Passing context

You can also pass in context to functions as parameters

```js
function repeatThreeTimes(func, context) {
  func.call(context);
  func.call(context);
  func.call(context);
};

...

  repeatThreeTimes(john.greetings, john);
};

foo();
// "hello, John Doe"
// "hello, John Doe"
// "hello, John Doe"
```

#### Solution 2: Binding the function

If you can't change the function context (for example passing it to a library method that you don't own), then `bind` is more useful:

```js
function repeatThreeTimes(func) {  // Do not need to explicitly call context object
  func();
  func();
  func();
}

...

  repeatThreeTimes(john.greetings.bind(john));
};

foo();
```

#### Solution 3: Add function as object method

The function below is missing the correct object context.

```js
var temperatures = [53, 86, 12, 43];

function average() {
  var total = 0;
  for (var i = this.length - 1; i >= 0; i--) {
    total += this[i];
  }

  return total / this.length;
}

console.log(average(temperatures));  // NaN
```

We could provide a context with methods like `call`, `apply`, and `bind`. However, we can also add a method to the array (it's also an object), and simply call it from there

```js
temperatures.average = average
console.log(temperatures.average());  // 48
```

### Internal function losing method context

```js
var obj = {
  a: "hello",
  b: "world",
  foo: function() {
    function bar() {
      console.log(this.a + ' ' + this.b);
    }
    bar();
  },
}

obj.foo();        // undefined undefined
```

Nested functions (within an object) lose context, which is a problem.

Functions execute with their explicit context. The `foo` method is called on `obj`, which explicitly provides context for the `foo` method. However, the call to `bar()` on line 9 has no such explicit context - it's just a function declaration call `bar()`. Since how a function is invoked determines the context, and not where it is defined, the JS (compiler\engine?) sees that there's no explicit context for this call and therefore binds it to the default context - global object. As a result, `this` on line 6 is the global object, not `obj`, thus `a` and `b` are undefined within the `bar` function body.

**Side note: Nested functions outside an object**

The concept of closure in JavaScript makes it so nested function can avoid this problem. Obviously `a` and `b` will still be `undefined`, nested functions retain access to to variables defined in outer scopes so `c` and `d` will be available to any inner functions nested in `foo`.

```js
var obj = {
  a: "hello",
  b: "world",
  foo: function() {
    var c = "bye";
    var d = "world"
    function bar() {
      function baz() {
        console.log(c + " " + d);
      }
      baz();
    }
    bar();
  },
}

obj.foo(); // bye world
```

#### Solution 1: Preserve context with a local variable

A local variable in an outer scope is available to inner/nested functions. Therefore the `self = this` idiom will our context issue.

```js
var obj = {
  a: "hello",
  b: "world",
  foo: function() {
    var self = this;

    function bar() {
      console.log(self.a + ' ' + self.b);
    }
    bar();
  },
}

obj.foo();        // hello world
```

#### Solution 2: Pass context

Providing context

```js
var obj = {
  a: "hello",
  b: "world",
  foo: function() {
    function bar() {
      console.log(this.a + ' ' + this.b);
    }
    bar.call(this);
  },
}

obj.foo();        // hello world
```

#### Solution 3: Bind the context with a function expression

This will bind the `bar` function to its surrounding context when the function itself is defined. Note that we can only use `bind` with a function expression, not a function declaration.

```js
obj = {
  a: 'hello',
  b: 'world',
  foo: function() {
    var bar = function() {
      console.log(this.a + ' ' + this.b);
    }.bind(this);

    bar();
  }
};

obj.foo();
```

### Similar problem: Outer Function Referenced By Object Method Lacks Context

```js
function logThis() {
  console.log(this);
}

var myObject = {
  objectMethod: logThis.bind(this),
  test: 1,
}

myObject.objectMethod(); // Window
```

This is confusing, but I think the trick is to think about when `myObject.objectMethod()` runs, it's effectively just calling `logThis`. Just because `logThis` is called within an object does not mean it gains the context of that object. This is a source of a lot of context / `this` confusion in JS.

One way to change context is to provide it. You can do this by 1) supplying a calling object directly or 2) explicitly provide it on execution

```js
var myObject = {
  objectMethod: this.logThis,        // 1) Caller used
  anotherMethod: logThis.call(this), // 2) Calling context provided
}

myObject.objectMethod(); // myObject
```

Another way to work around the problem is to use the context that's provided inside of function execution

```js
var myObject = {
  objectMethod: function() {
    console.log(this)
  },
}

myObject.objectMethod(); // myObject
```

But can be bound to a new variable while executing a function expression.

```js
var myObject = {
  objectMethod: function() {
    var bar = logThis.bind(this);
    bar()
  },
}

myObject.objectMethod(); // myObject
```

Without an expression, binding does nothing.

```js
logThis.bind(this)
logThis(); // Window
```

### Function as Argument Losing Surrounding Context

```js
function repeatThreeTimes(func) {
  func();
  func();
  func();
};

var john = {
  first_name: "John",
  last_name: "Doe",
  greetings: function() {
    repeatThreeTimes(function() {
      console.log("hello, " + this.first_name + " " + this.last_name);
    });
  }
};

john.greetings();

// "hello, undefined undefined"
// "hello, undefined undefined"
// "hello, undefined undefined"
```

The `this` context is also not going to be preserved, because even though the function expression is defined within the object, it's not executed with the context of the object.

#### Solution 1: self = this fix

```js
...
  greetings: function() {
    self = this;
    repeatThreeTimes(function() {
      console.log("hello, " + self.first_name + " " + self.last_name);
    });
  }
};
...
```

#### Solution 2: Bind the argument function with the surrounding context

The callback function within `repeatThreeTimes` is a function expression, and therefore we can use `bind` to set the context.

```js
...
  greetings: function() {
    repeatThreeTimes(function() {
      console.log("hello, " + this.first_name + " " + this.last_name);
    }.bind(this));
  }
};
```

The same thing happens with certain built in iterator/callback methods

#### this.arg vs. context manipulation - forEach, some, every, map

1) Use `bind`

Without `bind`, the function expression that contains `console.log` is executed in JavaScript's built in `forEach` method losses the `obj` context.

```js
obj = {
  a: 'hello',
  b: 'world',
  foo: function() {
    [1, 2, 3].forEach(function(number) {
      console.log(number + ' ' + this.a + ' ' + this.b);
    }.bind(this));
  },
};

obj.foo();
// 1 hello world
// 2 hello world
// 3 hello world
```

A function expression (the callback) occurs in the `forEach` loop, and therefore allows for the use of `bind`.

2) `thisArg`

The optional param `thisArg` can be used as the value of `this` (reference Object) when executing the callback function. Otherwise, the value `undefined` will be used as its `this` value. Available on:

* `Array.prototype.forEach`
* `Array.prototype.map`
* `Array.prototype.every`
* `Array.prototype.some`

```js
obj = {
  a: 'hello',
  b: 'world',
  foo: function() {
    [1, 2, 3].forEach(function(number) {
      console.log(number + ' ' + this.a + ' ' + this.b);
    }, this);
  },
};

obj.foo();
```

### Nested object losing context

```js
var myObject = {
  count: 1,
  myChildObject: {
    myMethod: function() {
      console.log(this.count);
    }
  }
};

myObject.myChildObject.myMethod(); // undefined
```

`myMethod` above is called on the `myChildObject`, so `myChildObject` is the execution context for `myMethod`. The object property `count` is in the `myObject` context, and therefore undefined when `myMethod` is invoked like it is above.

I believe the only way to pass internal information about a given object is through specifying context (using indirect invocation) when calling or binding the context. We can do this either with `call`

`myObject.myChildObject.myMethod.call(myObject); // 1`

or `bind`

`var countPrint = myObject.myChildObject.myMethod.bind(myObject)
console.log(countPrint());` // 1

### Indirect invocation and constructor function

Passing around context can be used to create class hierarchies in ES5 to call the parent constructor. This is an interesting way to delegate behavior.

```js
function Identify(name) {
  this.name = name.toUpperCase();
}

function Rabbit(name, countLegs) {
  Identify.call(this, name);
  this.countLegs = countLegs;
}
var myRabbit = new Rabbit('White Rabbit', 4);
myRabbit; // { name: "WHITE RABBIT', countLegs: 4 }
```

`Identity.call(this, name)` inside Rabbit makes an indirect call of the parent function to initialize the object.

For more about indirection invocation and an explanation of `this` in general, see here for a good [blog post](https://rainsoft.io/gentle-explanation-of-this-in-javascript/#51thisinindirectinvocation)

## Function closures

* JavaScript functions create closures when they are invoked.
* Closures allow code within a function to access any variable that was accessible at the time the function was declared.
* Values that are no longer accessible from anywhere in the code will be garbage collected and any memory they were using can then be used by other parts of the program.
* Closures can be used to make variables "private" to a function or set of functions and inaccessible from anywhere else.
* Closures allow functions to "carry around" values for later use.
* Every function declaration creates a new scope
* All variables in the same or surrounding scope are available to your code.

Higher-order functions  - functions that take a function as an argument, return a function, or both.

Another snippet about closures:

* Code within a function can access any variables defined within the function.
* Code within a function can also access any variables that can be accessed from the context where it was **defined**.

The first point is more obvious, the second may not be. What does it mean, the variables from the context from where it was defined?

### Nesting

To be more specific, an inner function has access to variables defined in any outer/surrounding scopes (includes function and global scopes). It doesn't matter how deeply nested a function is.

```js
function beginGreeting() {
  var name = 'Julian';

  function rememberName() {
    function greet() {
      console.log(name);
    }

    greet();
  }
  rememberName();
}
beginGreeting();          // 'Julian'
```

This would still work if `name` was defined in the global scope, above `beginGreeting()`.

### Objects, functions, and closure

This same principle works for objects, and functions within objects

```js
var b = 1;

function makeObj() {
  var a = 0;
  return {
    returnA: function() {
      return a;
    },
    returnB: function() {
      return b;
    },
  }
}
```

Variables in upper (or parent) scopes are available to lower (nested) scopes.

Objects within functions have the same scope as the function are they are in.

### Lexical Scoping

JS uses the structure of the source code to determine the variable's scope.

* It can access any variables defined within it.
* It can access any variables that were in scope code can access from the context where the function was defined.

### Shadowing

When searching for a variable, JS searches this hierarchy from the *bottom* to the *top*. It stops and returns the first variable it finds with a matching name. This means that variables in a _lower scope_ can shadow, or hide, a variable with the same name in a _higher scope_.

```js
var name = 'Julian';

function greet() {
  var name = 'Logan';
  console.log(name);
}
greet();             // Logan
```

When `greet()` is invoked it looks in the function scope first for `name`, and does not look further so you can only access the inner scope `name`

A parameter would shadow the outer scope as well

```js
var name = 'Logan';
function greet(name) {
  console.log(name);
}
greet('Sam');   // Sam
```

### Persistent reference

The value of a variable can change after creating a closure that includes the variable. When this happens, the closure sees the new value; the old value is no longer available.

```js
var count = 1;

function logCount() { // create a closure
  console.log(count);
}

logCount();            // logs: 1

count++;               // reassign count
logCount();            // closure sees new value for count; logs: 2
```

### Factory patten

```js
function createAdder() {
  let value = 0;
  const add = (amount) => (value = value + amount);
  const getValue = () => (value);
  return {
    add,
    getValue,
  }}
```

- `value` is a private variable. Only the functions declared inside `createAdder` have access to it.
- `value` is inside of this closure, so the variable “lives on” between function calls.

```js
adder.add(1);
adder.getValue(); // => 1
adder.add(1);
adder.getValue(); // => 2
```

### Closure types

**Pass a function to a function**

```js
function makeTimer(doneMessage, n) {
  setTimeout(function() {
    console.log(doneMessage);
  }, n);
}

makeTimer("Cookies are done!", 1000);
```

Again, function INNER has access to vars in function OUTER if function INNER is nested in OUTER. No matter how deeply nested.

**Return a function's return value**

```js
var secret = "007";

function getSecret() {
  var secret = "008";

  function getValue() { return secret; }
  return getValue();
}
getSecret();                    // "008"
```

Essentially `getSecret()` returns the result of executing the `getValue()` function.

**Returning a function reference:**

```js
var secret = "007";

function getSecret() {
  var secret = "008";

  function getValue() { return secret; }
  return getValue;   // Note lack of parens - getValue was not invoked
}
var getValueFun = getSecret();
getValueFun();                  // "008"
```

Here `getSecret();` returns a reference to the `getValue` function so it can be executed later.

Returning an anonymous function would work fine here as well

```js
var secret = "007";

function getSecret() {
  var secret = "008";

  function getValue() { return secret; }
  return getValue;   // Note lack of parens - getValue was not invoked
}
var getValueFun = getSecret();
getValueFun();                  // "008"
```

What if you wanted to add a `reveal` method, and add a better user interface too?

1) Change to return an object

```js
function getSecret() {
  var secret = "008";

  return {
    reveal: function() {
      return secret;
    }
  }
}
var secret = getSecret();
secret.reveal();                  // "008"
```

2) Add a `set` method

Hmm, this way doesn't seem to work.

```js
secret.set = function(newSecret) {
  // there is no way to access the items from within this method
  // because the closure that contains them is inaccessible

  secret                  // => throws Reference error!
  this.secret            // => undefined
};
```

For the reasons in the comments in the code snippet above, we need to change the `getSecret` definition itself to get this to work.

```js
function getSecret() {
  var secret = "008";

  return {
    reveal: function() {
      return secret;
    },
    set: function(newSecret) {
      secret = newSecret;
    }
  }
}
var secret = getSecret();
secret.reveal();                  // "008"
secret.set('005');
secret.reveal();
```

b) Return an anonymous function which returns a value

```js
var makeCounter = function() { // using a function expression here, but it's the same as above
  var count = 0;

  return function() {
    return count++;
  }
};

var doCount = makeCounter();
doCount(); // 0  Can you tell why this isn't 1? :)
doCount(); // 1
```

#### Creating an IIFE closure

You can use a function expression (FE) to create an IIFE if you do not want to assign the function

```js
var makeCounter = function() {
  var count = 0;

  return function() {
    return count++;
  }
}();

makeCounter() // 0
makeCounter() // 1
```

This also has the added benefit of making it so their scope is local. I.e a global count variable might cause problems in a large code base.

You could even avoid having to invoke the returned function

```js
...
  return function() {
    return count++;
  }()
}();

makeCounter // 0
makeCounter // 0
makeCounter() // TypeError makeCounter is not a function
```

However this returns a value, not a function.

If you're unsure of the safety of naming a function, immediately executing is a safe way.

```js
(function(number) {
  for (var i = 0; i < number; i++) {
    console.log(i);
  }
})(100);
```

### Closures, callbacks & additional arguments

Or, passing arguments to callback functions. Closure functions can take arguments

```js
function makeCounterLogger(start) {
 // Inner function also takes an argument here, but sometimes scoping means it doesn't need to.
  return function(stop) {   
    for (var i=start; i <= stop; i++) {
      console.log(i);
    }
  }
}

makeCounterLogger(5)(8)
```

You could also call the function like so:

```js
var countlog = makeCounterLogger(5);
countlog(8);  // 5 6 7 8
```

This behavior allows callbacks to take arguments, which can be useful when dealing with callback heavy libraries such as jQuery.

http://www.jstips.co/en/javascript/passing-arguments-to-callback-functions/

**Accessing variables in other scopes**

Sometimes another function will have a variable your function wants access. Local scope is hard to share especially between methods, so passing functions that take callbacks can help here.

```js
function otherFunc(mainCallback, local) {
  var otherVar = 2;
  return mainCallback(local)(otherVar)
}

function main() {
  var local = 1;

  var callback = function(local) {
    return function(otherVar) {
      return local + otherVar;
    };
  };

  // able to access to otherVar here
  return otherFunc(callback, local)
}

main()
```

If you didn't want to pass in local, and instead "close" over it

```
function main() {
  var local = 1;

  var callback = function(otherVar) {
    return (function(local) {
      return local + otherVar;
    })(local)
  };

  //  ES6 syntax
  // const callback = (otherVar) => ((local) => {
  //  return local + otherVar;
  // })(local);
  // return otherFunc(callback, local)
}
main()
```

You do an IIFE on the inner closure function. Which allows `main`to retain access to any local variable  passed to it’s inner function. In this case we passed in `local`. So when the `main` is invoked in the new scope (`otherFunc`) you can take in additional params without worry about passing in your previous local ones.

### Closures & OOP

This is some normal JS OOP code

```js
function Person() {
  this.name = "Bob";
  this.age = 47;
}

Person.prototype.info = function() {
  console.log(this.name + ' ' + this.age);
}

var bob = new Person();
bob.info()                 // Bob 47
```

A problem arises if you try to use a method as a callback.

`setTimeout(bob.info, 100); // undefined`

This is because specifying a method of an object as the callback function will cause the function by itself to be the callback, not the object associated with it.

`this` is assigned on function call (it's not something tied to the function itself), so binding the function manually will work

```js
setTimeout(function () {
  bob.greet();
}, 100);
```

Variables from the closure, however are part of the function itself, no matter how it's called. Therefore if we change our code to using 100% closures the behavior will work.

```js
function newPerson() {
  var name = "Tim";
  var age = 28;

  return {
    info: function() { console.log(name + ' ' + age); }
  }
}

var tim = newPerson();
tim.info()                 // Tim 28
setTimeout(tim.info, 100); // Tim 28
```

This works the same if you're referencing a function expression assigned to a variable from within the closure

```js
function worker() {
  var title = 'garbage man';
  var logTitle = function() { console.log(title); };

  return {
    publicLogTitle: function() { logTitle() }
  }
}

var newWorker = worker();
newWorker.publicLogTitle();                    // 'garbage man'

setTimeout(newWorker.publicLogTitle(), 1000);  // 'garbage man'
```

### Partial application

Call certain arguments ahead of time to be called later. Here's a very simple example:

```js
function later(func, arg) {
  return function() {
    func(arg);
  }
}

var logWarning = later(console.log, 'The system is shutting down!');
logWarning();
```

Here's a slightly more complicated example

```js
function greet(greetString, nameString) {
  return greetString[0].toUpperCase() + greetString.slice(1) + ', ' + nameString + '!';
}

function partial(primary, arg1) {
  return function(arg2) {
    return primary(arg1, arg2);
  };
}

var sayHi = partial(greet, "hi")

sayHi("Sarah");                   // "Hi, Sarah!
```

## Garbage collection

JS allocates memory when new variables or properties are declared, and deallocates the memory when those variables **go out of scope** or are deleted.

Go out of scope means no closures still in the system that contain a reference to the memory.

Variables defined at the top level of a JavaScript program remain accessible for the duration of the program's execution. They are also accessible within any functions defined in the program.

This would be garbage collected:

```js
function logName() {
  var name = "Sarah";    // Declare a variable and set its value. The JavaScript runtime
                         // automatically allocates the memory.

  console.log(name);     // Do something with name
}
```

This would NOT be garbage collected:

```js
function makeHello(name) {
  var question = "how are you";
  return function() {
    console.log('Hello, ' +question + name + '?');
  }
}

var helloSteve = makeHello('Steve');
```

When you create a closure, it stores a reference to all variables it can access.As long as the closure exists, those variables remain in existence, which means that the objects or values they reference must also endure.

Until you do something like this `message` and `question` will be accessible, as the function will no longer be availabe in the global scope.

`helloSteve = null;`

## DOM

DOM - an in-memory object representation of an HTML document. It provides a way to interact with a web page using JavaScript

### DOM Structure

The DOM is a hierarchy of nodes. Each node can contain any number of child nodes.

* All DOM objects are Nodes.
* All DOM objects have a specific type that inherits from Node, which means they all have properties or methods along with those they inherit from Nodes.
* The most common DOM object types you will encounter are **elements** and **text** nodes.

**Node types**

* `EventTarget` - provides the event-handling behavior that supports interactive web applications.
* `Node` provides common behavior to all nodes.
* `Text` and `Element` are the chief subtypes of Node.
* `Text` nodes hold text.
* Element nodes represent HTML tags.
* Most HTML tags map to specific element subtypes that inherit from `HTMLElement`.

**Testing node types**

`toString` is a good way to test a node's type

```js
var t = document.querySelector("p").firstChild
t.toString() [object Text]
```

`instanceof` is better when writing code

```js
var p = document.querySelector('p');
p instanceof HTMLParagraphElement;  // true
p instanceof Element;               // true
```

**Useful node properties**

* `nodeName` - Caps name of a html tag (or #comment / #text)
* `nodeType` - Integer value representing a node's type
* `nodeValue` - contains the textual content of the Node
* `textContent` - returns Element's textual content of every Text node that is a child of the Element Node.
* `tagName` - same as `nodeName`, except that it only works with Elements (which can also use `nodeName`)

### Traversing DOM

#### Nodes

Nodes have properties that traverse the DOM tree. All elements have both parent and child nodes, and therefore all methods below.

Parent Node Properties | Value
-----------------------|-------
`firstChild` | `childNodes[0]` or null
`lastChild`	| `childNodes[childNodes.length-1]` or `null`
`childNodes` | _Live collection_ of all child nodes

Child Node Properties | Value
----------------------|------
`nextSibling` | `parentNode.childNodes[n+1]` or `null`
`previousSibling` | `parentNode.childNodes[n-1]` or `null`
`parentNode` | Immediate parent of this node

A given DOM element may return a `null` value, depending on the DOM.

**Walking the dom**

This is similar to how you would write your own `forEach` method.

```js
function walk(node, callback) {
  // do something with node
  callback(node);

  // for each child node
  for (var i = 0; i < node.childNodes.length; i++) {
    // recursively call walk()
    walk(node.childNodes[i], callback);
  }
}

// log the nodeName of every node
walk(document.body, function(node) {
  console.log(node.nodeName);
});
```

### Elements

Elements have properties to traverse the DOM tree:

Parent Element Properties	| Value
--------------------------|------
`firstElementChild` | children[0] or null
`lastElementChild`	| children[children.length-1] or null
`children` | _Live collection_ of all child elements
`childElementCount` | children.length


Child Element Properties | Value
-------------------------|------
`nextElementSibling` | parentNode.children[n+1] or `null`
`previousElementSibling`	| parentNode.children[n-1] or `null`

In IE, use these methods on `document.body` instead of `document`.

#### Searching by CSS selector

* `document.getElementById(id)` finds a single Element with the specified id
* `document.querySelector(selector)` returns the first Element that matches a CSS selector.
* `document.querySelectorAll(selector)` is similar but returns all matching elements.

**HTMLCollection or NodeList**

* Array like objects
* HTMLCollections provide no support for `forEach`
* NodeLists on some browsers do support `forEach`

**Searching for sub-list of elements**

You can call `get` and `query` method on any element, document is usually the most common. Calling these on elements down a specific DOM branch will restrict the results.

### Interacting with the DOM

#### Element Attribute

Method	 | Description | Returns
--------|-------------|--------
`getAttribute(name)`| Retrieve value of attribute `name` | Value of attribute as String
`setAttribute(name, newValue)`| Set value of attribute `name` to `newValue` | `undefined`
`hasAttribute(name)` | Check whether element has attribute name | `true` or `false`

```js
> p.hasAttribute('class');         // true
> p.getAttribute('class');         // "intro"
> p.getAttribute('id');            // "simple"
> p.setAttribute('id', 'complex'); // <p class="intro" id="complex">…</p>
```

### Attribute properties

JavaScript exposes these certain attributes as gettable and settable properties of the DOM Element: `id`, `name`, `title`, and `value`

```js
p.id;       // "complex
p.className // "intro"
```

JavaScript doesn't provide all these properties on every `Element` type: the `name` and `value` attributes, in particular, are invalid on most elements.

### href

Understanding attribute properties is helpful when working with the `href` attribute.

If you have selected an `a` tag element and try to access it's `href` property, most browers will supply the host and port and well.

```js
console.log(e.target.href) // http://localhost:3000/checkout
```

Say you were trying to test if you had a relative link - this wouldn't make things easier.

However using `getAttribute(href)` gets you the href content, which is more helpful.

```js
> console.log(e.target.getAttribute(href))
< /checkout
```

Incidentally, `pathname` seems like will also work here as it also gives you `/checkout`. Be careful though if you were checking for a leading `/` to see if the link was relative. An href like this, `href="#"`, will return a pathname of `/`.

jQuery makes this process a bit easier, allowing you do to something like this `a[href=^'/']`.

### classList

Working with the `class` attribute via `className` is inconvenient when elements have more than one class.

Name | Description
-----|------------
`add(name)` | Add class name to element
`remove(name)` | Remove class name from element
`toggle(name)` | Add class name to element if it doesn't exist, remove if it does exist.
`contains(name)` |	Return `true` or `false` depending on whether element has class name.
`length` | The number of classes to which element belongs.

`document.getElementById('primary_heading').classList.add('heading')`

### style

The `style` attribute on an `Element` references a `CSSStyleDeclaration` Object:

```js
h1.style;      // CSSStyleDeclaration {alignContent: "", alignItems: "",
h1.style.color = 'red';
```

**Setting RGB vs. hex**

```js
container.style.backgroundColor = '#ff1212';
container.style.backgroundColor = "rgb(255,0,0)";
```

**Removing a CSS property**

To remove a CSS property*, set the property to `null` with the `style` property

`h1.style.color = null;`

* - I'm not sure this is possible with jQuery :)

**Dasherized properties**

Use camel case instead `line-height` vs. `lineHeight`

### Modifying element text

Element properties do not include `textNodes`, so use `textContent` to element text.


```html
<p>
  You can <a href="?page=2">step backward</a> or <a href="/page/3">continue</a>.
  </p>
```
```js
var p = document.querySelector('p')
p.textContent = "Hey";
p.textContent;  // "Hey
```

Be careful, because this removes all child nodes

```html
    <p>
     Hey
    </p>
```

Therefore wrapping editable sections in `span` or `div` is safer.

### Creating nodes

Node Creation Method | Returns
---------------------|--------
`document.createElement(tagName)` | A new Element `node`
`document.createTextNode(text)`	| A new Text `node`
`node.cloneNode(deepClone)` | Returns a copy of `node`, or all children if `deepClone` is `true`

### Adding nodes to DOM

Parent Node Method | Description
-------------------|-------------
`parent.appendChild(node)` | Append node to the end of parent.childNodes
`parent.insertBefore(node, targetNode)` | Insert node into `parent.childNodes` before targetNode
`parent.replaceChild(node, targetNode)` | Remove `targetNode` from `parent.childNodes` and insert node at its former position

```js
document.createElement('P')
paragraph.textContent = 'This is a test.';
document.body.appendChild(paragraph);
```

* No Node can appear twice in the DOM.
* You can't call `document.appendChild`; it causes an error. Use `document.body.appendChild` instead.

Element Insertion Method | Description
-------------------------|------------
`element.insertAdjacentElement(position, newElement)` | Inserts `newElement` at position relative to element
`element.insertAdjacentText(position, text)` | Inserts Text node containing text at position relative to element

**position**

``position` must be one of the following String values:

Position	| Description
----------|------------
"beforebegin"	 | Before the element
"afterbegin"	| Before the first child of the element
"beforeend"	| After the last child of the element
"afterend"	| After the element

### Removing nodes

`node.remove()` and `parent.removeChild(node)` remove nodes from the DOM.

**Loading JS**

`window.onload = function() {}`

**Selecting elements**

If you need to select an element by id do

`document.getElementById()`

However you can write your own jQuery-esque selector

```js
function $(id_selector) {
  return document.getElementById(id_selector);
}
```

### Events

**Asynchronous code**

* `setTimeout(callback, delay)` - used to invoke a Function after the specified number of milliseconds.
* `setInterval(callback, delay)` - used to repeatedly invoke a Function, returns an id. `clearInterval(id)` can be used to prevent future invocations of the Function.

**Event** - an object that represents some occurrence and contains a variety of information about what and where it happened. Events can be triggered by the browser as it loads a page, by a user as they interact with the page, and by the browser as it performs work as directed by a program.

#### Adding event listeners

**Event listener** - callbacks that will be invoked whenever a matching event is detected (The code that is run in response to an event firing)

Setting up an event listener

1. _Identify the event_ you are interested in. This can be an event caused by a user action, page lifecycle, and more.
2. _Identify what element the event will occur on_. Depending on the event, the object could be a button, the page, or anything in between.
3. _Define a Function for the event_ . The function should be called when this event occurs. The Function will receive a single argument, which will be an `Event` object.
4. _Register the Function as an event listener_. This is where the first three steps come together into a working system.

`element.addEventListener` or GlobalEventHandlers like `element.onclick` are used to register listeners.

**GlobalEventHandler**

```js
<button onclick="console.log('clicked', event)">
  Click me
</button>
```
Notes:

- You must refer to the event as `event`. Passing in an `e` will not work.
- You can also technically pass in `this` to grab the target element, but `event.target` is probably more standary
- You can also use an IIFE     

```js
<button onclick="(function(e) { console.log(event); })()">
  Click me
</button>
```

**addEventListener**

```js
document.addEventListener('click',
  function(e) { console.log('clicked!', e) };
);
```

#### Removing EventListeners

Event listeners must be removed according to the approach by which they were added to the node.

**addEventListener**

For event listeners registered with addEventListener, the DOM node method removeEventListener must be used:

`eventTarget.removeEventListener(eventType, eventHandler);`

Following this pattern, we would remove the event listener we set above as follows:

`document.removeEventListener('click', handler);`

It's important to note that, because handler must refer to the same Function object used when it was registered, an event listener added with an anonymous function expression cannot be removed with removeEventListener.

**GlobalEventHandler**

The object-property style of GlobalEventHandler makes removing an event listener added with this approach somewhat easier: simply set the desired eventProperty to undefined.

`eventTarget.eventProperty = undefined;`

Following this pattern, we would remove the event listener set above like this:

`document.onclick = undefined;`

### Page life-cycle events

**DOMContentLoaded**

Code that needs access to the DOM should be invoked after the `DOMContentLoaded` event is fired on document. For example, adding an event listener to one or more page elements.

```js
// https://codepen.io/dylankb/pen/PmazLp
document.addEventListener('DOMContentLoaded', function() {
  document.querySelector('.button-container').addEventListener('click', logger);
});
```

_Like DOMContentLoaded, but not_

Another, non event-driven way to execute JS after the `DOMContentLoaded` loaded event fires would be to include it in a script tag just before the closing `</body>` tag.

`load` event - fires after all assets are loaded

### User events

Event Type | Example Events
-----------|---------------
Keyboard | keydown, keyup, keypress
Mouse	| mouseenter, mouseleave, mousedown, mouseup, click
Touch	| touchdown, touchup, touchmove
Window	| scroll, resize
Form	| submit

#### Mouse events

Property | Description
---------|----------
button	| Which button was pressed (null for events unrelated to mouse clicks)
clientX | The horizontal position of the mouse when the event occured, relative to the visible area of the page.
clientY | The vertical position of the mouse when the event occured, relative to the visible area of the page.

#### Keyboard events

Property | Description
---------|------------|
which | The ASCII key code, which is a Number that specifies the key that was pressed.|
key	| The String value of the pressed key. Not supported in Safari.
shiftKey | Boolean value indicating if the shift key was pressed.|
altKey	| Boolean value indicating if the alt (or option) key was pressed.|
ctrlKey | Boolean value indicating if the control key was pressed.|
metaKey | Boolean value indicating if the meta (or command) key was pressed.|

`keypress` event doesn't fire when certain keys are pressed, such as Shift and the other modifier keys

More events [here](https://developer.mozilla.org/en-US/docs/Web/Events)

### Event object

Property	| Description
----------|-----------
`type` |	The type of event.
`currentTarget` | The object that is currently being targeted as the event bubbles up the DOM. This will be the object the event handler was attached to.
`target`	| The object the event originally was fired upon.

### Capturing and bubbling

**Event phases**

There are three phases to events being fired: _capturing_, _target_, and _bubbling_.

By default, event listeners will listen for events that are triggered during the **target** and **bubbling** phases

* Capturing - The browser starts at the outermost element, which will be the `window`, and fires the event on each element it encounters on its way down to the target element.
* Target - fires on the target element
* Bubbling - (Reverse of capturing) event is fired on each parent element , working through containing elements until the window is reached.

**Controlling default behavior**

* `event.preventDefault()` - used to prevent default browser behavior in response to an event
  * Submit event browser reset! - If you don't `preventDefault` when a form is submitted, the whole browser will refresh which acts can make you think something unrelated is wrong with your app :S
* `event.stopPropagation()` - stops the event from being triggered on other containing or contained elements

It is a good practice to call `preventDefault()` or `stopPropagation()` as early as possible in an event handler to show clear intent.

### Delegation

**Event delegation** - a technique used to handle events triggered by multiple elements using a single event handler.

Benefits of event delegation

* Don't have to wait for DOMContentLoaded event - reduces timing complexity
* New elements will have listeners
* Reduces number of event handlers => increases performance

You can do this as opposed to adding an event listener to every button on the page.

```js
document.addEventListener('click', function(event) {
  var target = event.target;
  if (target.tagName === 'BUTTON') {
      var text = target.textContent;
      alert('Button ' + text + ' was clicked.');    
  }
});
```

Cons

* Code that has to handle multiple situations will become more complicated

### Event loop

#### Event loop / closure bug

```js
function delayLog() {
    for (var i = 1; i <= 10; i += 1) {
        setTimeout(function(){
            console.log(i);
        }, i * 1000);
    }
}
delayLog();
11
11
// ... logs 8 more times
```

JavaScript runtime has to finish executing one piece of code before it goes on to execute other code like the function you pass to `setTimeout`. A piece of code or a function that has to be executed asynchronously is stacked up in something called the event loop. So the `for` loop has to finish before your anonymous function gets called even if the timeout is 0 seconds.

After the loop is finished and after the given time out the anonymous functions are executed one by one. However since every anonymous function refers to the variable `i` via closure, and the value of `i` is now `11`, 11 is logged ten times.

There are two main ways to stop that from happening:

#### IIFE solution

One is to make a new scope so that a new variable is declared in each iteration.

```js
for (var i = 1; i <= 10; i += 1) {
  (function(j) {
    setTimeout(function(){
      console.log(j);
    }, 0);
  })(i);
}
```

#### ES6 solution

The other solution is based on the ES6 `let` keyword. If you use `let` instead of `var` in your `for` loop, what effectively happens is that in every iteration the variable `i` is redefined for you.

```js
for (let i = 1; i <= 10; i += 1) {
   setTimeout(function(){
     console.log(i);
    }, 0);
}
```

## XML HTTP Requests

Use the XMLHttpRequest object to send a HTTP request with JavaScript.

```js
var request = new XMLHttpRequest(); // Instantiate new XMLHttpRequest object
request.open('GET', '/path');       // Set HTTP method and URL on request
request.send();                     // Send request
```

Method	| Description
-------|------------|
`open(method, url)` |Open a connection to url using method.|
`send(data)` | Send the request, optionally sending along data.|
`setRequestHeader(header, value)`|Set HTTP header to value.|
`abort()`|Cancel an active request.|
`getResponseHeader(header)`|Return the response's value for header.|

Property| Writable | Default Value |	Description |
--------|----------|---------------|-------------|
`timeout`| Yes | | Maximum time a request can take to complete (in milliseconds)|
`readyState`	| No | |What state the request is in (see below)
`responseText` | No |	`null` | Raw text of the response's body.
`response` | No |	`null`	| Parsed content of response, not meaningful in all situations

## Window

### `Window.history`

### `Window.location`

`location.hash` - URL params after `#`

`location.pathname` - current root url + dir paths

`e.originalState.state` ? - not sure what data structure is

Example:

```js
$('window').on('popstate', function(e) {
  var state = e.originalEvent.state;

  if (location.hash) { switchPage(location.hash) }
)};
```

## Tricks

### Make a copy of something (like an object)

```js
var thing = thing.slice() // ES5
```

### Make N length string**

```js
new Array(3).join('x') // ES5
'x'.repeat(3) // ES6
```

### Make an N length array of letters

First, you could append `.split()` to each of the above two string creation examples.

```js
// ES5 - If you wanted some flexibility
Array.apply(null, new Array(2)).map(function (x) { return 'x' });
// ES5 - more terse example
new Array(2).fill('x');
```

### Make an empty iterable array

For example you can't map over `new Array(2)` since it is an array of 2 elements without pointers. `[undefined, undefined]` is an array of 2 elements with pointers to `undefined`.

```js
Array.apply(null, new Array(2)) // ES5  
new Array(2).fill() // ES5
[...new Array(2)] // ES6
```

### Make an N-1 length array of integers

You could map over the result and collect the index to create a 1..N array of numbers.

```js
new Array(3).join('x').split('').map(function(x, i) { return i }); // ES5
'x'.repeat(3).split('').map((x, i) => i); // ES6
```

### `toString()` to determine an object's type**

```js
> document.toString() // "[object HTMLDocument]"
```

### Logging

`console.table()` - displays an object in a table. (even `table()` works)

`console.dir()` - displays a tree expandable object

`copy()` - copies to your clipboard

`$(element)[0]` - returns the DOM element

`inspect(DOM element)` - opens up the inspector to that element

`values(object) / keys(object)` - keys/values for an object

`$$(selector)` - array of dom elements (works w/out jQuery)

`$_` - last returned value (in Chrome)

`$0` - last selected element (at least in Chrom)

`getEventListeners(obj)` - object of event listeners on element

## Debugging

* Check console for load issues
* Turn on exception pauses in the Sources tab
* Alerts debugging
* Enter `debugger;` into the script and debug from console
* Enter `console.log(someVariable)` and debug from console
* Nested breakpoints: Create a breakpoint/enter a debugger and disable breakpoints (tab icon in devtools) until, for example, the sixth iteration. Then re-enable them. Beats clicking continue X number of times.
* Node debugging - set `debugger` and run `node debug script.js`

## Preventing errors

* Guard clauses

Use when you can't trust input

* Consider edge cases
* Error catching

- Simple guard clause is not possible
- Error could be thrown by built-in JS method

## jQuery

### Basics

#### Loading the dom

```js
$(document).ready(function() {
  // DOM is now loaded
});

$(window).load(function() {
  // DOM is loaded, img tags are loaded
});
```

**Shortcut for loading the dom**

```js
$(function() {
  // DOM is now loaded
});
```

#### Chaining

As long as a jQuery object is returned, you can keep chaining additional jQuery methods.

`$ul.append($("<li />").text('1'));`

```html
<ul><li>1</li></ul>
```

**Not chaining**

`$ul.append(('<li></li>').text('1'));`

An error is thrown `"<li></li>".text is not a function`, so nothing is appended.

```html
<ul></ul>
```

### Creating elements

You can create an HTML element by supplying the html as the first argument, and then an object of html attributes and/or inline CSS properties

```js
var $element = $("<div />", {
  "class": 'shapes ' + data.shapeType,
  data: data,
  css {
    left: +data.startX,
    top: +data.startY
  }
});
```

### jQuery vs. vanilla JS

Action | jQuery | JS
-------| -------|---
Select elements by id | `$('#ID)` | `document.getElementById("ID")`
Add class | `$element.css('class', 'some-class')` | `element.setAttribute("class", "some-class");`
Add class (ii) | `$element.addClass('some-class')` | `element.classList.add("some-class");`
Add other attribute | `$element.attr("alt", "string")` | `element.setAttribute('alt', 'string')`
Remove attribute | `$element.removeAttr("style")` | `element.removeAttribute("style")`
Get class | `$element.attr('class')` | `element.getAttribute("class")`
Get text  | `$element.text()` | `element.innerHTML`/`textContent`/`innerText`
On submit | `$form.on("submit", function(e) {` | `form.onsubmit = function(e) {`
Get value | `$element.val()` | `element.value`

**Accessing jQuery vs. DOM objects**

* Use `eq` to access the jQuery object  
* Use `[]` or `get()` to retrieve the DOM element

```js
var content = $('li');
content[0]
> <li>​…​</li>​
content[0].jquery
> undefined

content.eq(2)
> [li]
content.eq(2).jquery
> "1.11.2"
```

### Traversal

* Generally uses CSS selector rules, but some jQuery specific ones
* Selectors inside `[]` are element attribute selectors (`class`, `data-id`, etc.)  
`("li").filter("[data-id]")`

#### jQuery specific selectors

Multiple selector - `$('.class', '#id', ...)` - Can selector multiple different, non-related elements

jQuery specific pseudo-selector

* `:contains`
* `:odd`
* `:text` - input elements type text
* `:even` - zero based index
* `:input` - includes textarea, button, etc., not just `<input>`
* `:checked`

#### `filter()`

You can select certain items in a collection using the `filter` method and passing in a valid CSS selector or jQuery psuedo-selector

`$('li).filter('.even')`

The return value is a jQuery collection, so it is of course chainable

`$('article li li').filter(":contains('ac ante')").next();`

### Other search methods

**Negation**

`$('td').not('.protected');`

#### CSS attribute matchers

**Find (specific) parent**

`p.parent(".highlight")`

**Fuzzy match**

`$('[class*=block]');`

Selects an element if the selector's string appears anywhere within the element's attribute value

**Starts**

`$('[id^=blind]')`

Grabs all elements with an ID that begins with 'blind'.

**Ends with**

`$('[id$=blind]')`

Grabs all elements with an ID that ends with 'blind'.

### `closest()` vs. `parents()`

`closest` - Begins with the current element, and travels up the DOM tree until it finds a match for the supplied selector

`parents` - Travels up the DOM tree until it finds matches for the supplied selector

```html
<ul class="level-1">
  <li class="item-i">I</li>
  <li class="item-ii">II
    <ul class="level-2">
      <li class="item-a">A</li>
    </ul>
</ul>
```

Examples:

1) `$( "li.item-a" ).closest( "ul" ) // [ul.level-2])`

`closest` travels up DOM tree to find first matching element

2) `$( "li.item-a" ).parents( "ul" ) // [ul.level-2, ul.level-1])`

`closest` travels up DOM tree to find parent _elements_

3) `$( "li.item-a" ).closest( "li" ) // [li.item-a])`

`closest` searches by beginning with the current element, and therefore it returns itself as the result.

4) `$( "li.item-a" ).parents( "li" ) // [li.item-ii]`

`.parents()` does not search the current element, so it returns the next matching element(s) up the DOM tree

### `index()`

`index()` can be used in several ways. Refer to the examples below:

```html
<p>Hey</p>
<p>You</p>
<p>There</p>

<div class="parent">
  <span>Hey</span>
  <p class="child">Child</p>
  <p>class</p>
</div>
```

1) `$element.index('selector')` - **Element's index relative to other elements matched by the selector**

```js
`$('p.child').index('p'); // => 3`
```

Index of `p.child` tag compared to all other `p` tags in the document

2) `$element.index()` - **Index of `$element` relative to other siblings**

```js
var $firstP = $('div.parent').find('p').eq(0); // Get first p tag in .parent - p.child
`$first.index() // => 1
```

Index of `p` tag in relation to all siblings (`span`, etc.)

3) `$collection.index($element)` - **Index of `$element` relative to collection elements**

```js
$('div.parent').find('p').index('p.child') // => 0  OR
$('div.parent p').index('p.child')         // => 0  
```

Index of `p.child` relative to other `p` elements in the collection (relative to other `p` elements inside `parent`)

A modified version of this last one is useful for finding the element's index you clicked on relative to the parent element *and* by element type. Using jQuery it might look something like this:

`$(div.parent p').index($(this))`

### `each()` method

Iterates over a collection, setting `this` to the current DOM element (not a jQuery object)

```html
<ul>
  <li data-id="1">Apple</li>
  <li data-id="2">Apricot</li>
  <li data-id="3">Banana</li>
</ul>
```

**DOM vs jQuery element**

`each()` returns a DOM element and therefore you would have do something like this to get the `data-id` attribute value

```js
$("li").filter("[data-id]")[0].attributes[0].value // "1"
```

or

```js
$("li").filter("[data-id]")[0].dataset.id
```

To make accessing `attr` values a little bit easier using jQuery, pass the element into a jQuery object using `$()`

```js
$("li").filter("[data-id]").each(function(index) {
  console.log( "Index: " + index + " data-id: " + $(this).attr("data-id")); // data properties can also use $(this).data('id');
});

// Index: 0 data-id: 1
// Index: 1 data-id: 2
// Index: 2 data-id: 3
// [li, li, li]
```

### `eq()`

* Return item by passed in index as jQuery object.
* Negative indexes work similar to Ruby (returns item n.length - 1)

### Form management

#### Grabbing input from an input field

All `input` elements return value from the `.val()` method.

```js
$("form#some-form").submit(function(event) {
  var someInput = $("input#some-input").val()

  event.preventDefault();
});
```

Like many jQuery methods, it's also a setter

#### Resetting a form

The DOM form element has a reset method. Accessing it from a jQuery method looks like this

`$form.get(0).reset();` or `$form[0]`

The `get` method is useful if you need to get a specific DOM element in a collection `$('li').get(-1)`

If you were in the element's context, you would already have access to the DOM element and could access it like this

`this.reset();`

This resets the form's input values to their values on page load. So if we had an input with a default value of 1, `<input type="text" value="1">`, `reset()` would provide a `"1"` for that form field.

#### Getting data from a form

`$('form').serializeArray();`

requires `name` attribute on `input` elements

#### `prop()` - setting a checked radio

`$(:radio).eq(0).prop(checked, true)`

You could use `attr`, but checked isn't an attribute of `input` element - it's a property.

### Other traversal methods

`nextAll()` - grab all of the sibling elements that come after the current one
`prevAll()` - grab all of the sibiling elements prior to the current one

### DOM display values

#### `position()` vs. `offset()`

`position()` - relative to nearest parent with `position: relative`

* will not reflect other position-influencing factors (margin)

`offset()` - offset from 0,0 of the window

#### `height()` vs. `innerHeight()`

`height()`

* element content dimensions

`innerHeight()`

* includes padding (not border)

`outerHeight()`

* optionally can include margin
* includes padding _and_ border

`box-sizing`

jQuery dimensions vs. CSS dimenstions may be different because jQuery takes into account box-sizing

### DOM manipulation

#### `css()` method

* Can set multiple CSS properties at once
* Needs dasherized properties as cameCased (`font-size` => `fontSize`)

When using the CSS convenience method be sure to convert your values into `Number` type. Like so:

```js
  function resetElement($e) {
    var data = $e.data();

    $e.css({
      top: +data.startX,
      right: +data.startX,
    });
  }
```

Without this it won't treat the css as a `px`, just a `string`.

#### Scroll position - `scrollTop()`

Retrieves current position of scroll window.

Example below sets element `top` value to current screen position + `30px`

```js
$ele.css({
  top: $(window).scrollTop() + 30
)}
```

#### `prepend()` vs. `prependTo()`

Inserts the specified content as the first child of each element in the jQuery collection

* `contentToPrepend.prependTo(matchingElementsToBePrependedTo)`
* `containerToPreprendTo.prepend(matchingOrSuppliedContentToPrepend)`

Besides syntax order, the main difference is that each method allows for multiple elements or an array to be supplied to the parameter. This means that `prependTo` can prepend content to multiple target arguments\*,

`$("<p>Prepend Test</p>").prependTo([".inner", ".inner-last"]);`

and `prepend` can prepend multiple content arguments*

`$( ".inner" ).prepend( "<p>Prepend Test</p>", "<p>Also</p>" );`

**Multiple argument format**

`prependTo()` requires multiple arguments to be passed in as a single array. `prepend` can take an array or multiple arguments.

\* - A jQuery selector can select multiple elements, I was just emphasizing multiple selectors or arguments could be passed to each. This is also a slightly untrue in the case of ... ?

### jQuery patterns

#### Modal toggling

Using pure jQuery, one way to close a modal you would first filter for visibile modals, then hide or fade those modals out while revealing the newly clicked one.

#### Tabular navigation

Hide all other tabs besides the first

```css
ele + ele { display: none }
```

On click, hide all tabs and display the one you clicked on

```js
  $('parent').on('click', 'a', function(e) {
    e.preventDefault();
    var $e = $(e.target),
        idx = $e.attr('href');

    $('ele').hide().filter(idx).show();
```

You might also want to toggle the active class

```js
    ...
    $('ele').removeClass('active');
    $e.addClass('active');
```

### Animations

Animations are chainable methods

#### fade animations

* Can be called without arguments (except `fadeTo`)
* Default 400 (millisecond) duration
* Two speed keywords: "slow" (600ms) and "fast" (200ms)
* Optionally take a callback that executes on animation completion

```js
$p.fadeOut();
$p.fadeIn(250, function() {
  $(this).addClass('visible');  // animating item (context) not a jQuery object, so using $()
});
$p.fadeToggle();
$p.fadeTo(400, .5);
```

#### slide animations

```js
$p.slideDown();
$p.slideUp(250);
$p.slideToggle(400, function() {
  console.log('Sliding complete!');
});
```

* Can take `linear` as an argument to change animation style
* Can take properties instead of arguments

```js
$p.slideToggle({
  duration: 400,
  easing: 'linear',
  complete: function() {
    console.log('Sliding complete!');
  },
});
```

#### `animate`

* First argument - Object that represents the CSS properties to be animated and what values to end on for each.
* Second argument - duration, then the optional easing method, then the callback.
* Third arg - callback on completion

```js
$p.animate({
  left: 500,
  top: 250
}, 400, function() {
  $(this).text('All done!');
});
```

Two objects way

* First arg - Same CSS object
* Second arg - Duration, easing, and callback

```js
$p.animate({
  left: 500,
  top: 250
}, {
  duration: 1000,
  complete: function() {
    $(this).text('All done!');
  }
});
```

**Delay animation**

`.delay()` - Useful for delaying between different animations - `$p.slideUp(250).delay(500).slideDown(250);`

### Stoping animations

Useful for controlling animations queue.

* `stop()` - Stop current animations and starts next one. Pass `true` to stop all in current/future queue. Pass second `true` to skip to last frame.

I.e, you have a menu with `fadeIn` and `fadeOut` animations and a users skips over many of them frequently

`$p.stop().fadeToggle(200);`

* `.finish()` - Equivalent to running `stop(true, true)` for each animation.

**Stoping all animations**

Set `$.fx.off` to `true`. You can do this on other sites.

### Events

**jQuery DOM interactions**

Some examples below:

* `blur` - clicking out of a form field

#### Page load vs. events

An example of why we need pay attention to under which event a piece of code fires.

This does not highlight green elements as they appear:

```js
$(document).ready(function() {
  $("button#hello").click(function() {
    $("ul#user").prepend("<li>Hello!</li>");
  });
  $('li').css('background-color', 'green');
});
```

`$(document).ready` looks at the page when it's initially loaded, not on each click. When the page loads there are no `li` (we're adding them via jQuery on each click).

Adding this to a click action will work

```js
$(document).ready(function() {
  $("button#hello").click(function() {
    $("ul#user").prepend("<li>Hello!</li>");
    $('li').css('background-color', 'green');
  });
});
```

#### Event types

`.submit()` - Can only be attached to a form

#### Callbacks

* The event callback context (`this`) is the DOM element
* The event is an optional parameter
* `event.currentTarget === this`

```js
function highlight(e) {
  $(this).toggleClass("highlight");
  console.log(e.target === this); // true
}
```
```js
`$('.simple a').on("click", highlight)`;
```

If you want to use the `this` keyword in the event handlers, it’s good to bind it explicitly.
Sometimes `e.currentTarget === e.target`

#### Delegated events

The handler is not called when the event occurs directly on the bound element (the element calling the `.on()` method, but only for descendants (inner elements) that match the selector (the selector passed into the `on()` method call.

jQuery bubbles the event from the event target up to the element where the handler is attached (i.e., innermost to outermost element) and runs the handler for any elements along that path matching the selector.

##### Automatically listen for new elements

Dynamically creating new elements with jQuery can cause a problem when the newly created events need to have associated event handlers.

```html
<p><a class="simple" href="#">A simple click event</a></p>
```
```js
function highlight() { ... }

`$('.simple a').on("click", highlight)`;

`$('.simple').filter("a").clone().appendTo($('#clone"));
}
```

The second line of JS would create a new DOM element, but it would not have a click event bound to it, and therefore we would not be able to trigger the highlight function.

Delegated events have the advantage that they can process events from descendant elements that are added to the document at a later time. Below is an example of how to solve this issue:

```html
<div id="example">
  <p><a href="#">A delegated click event</a></p>
</div>
```

```js
`$('.example').on("click", "a", highlight)`;

`$('.example').filter("a").clone().appendTo($('#clone"));
}
```

The example above uses event delegation to all `a` tags nested in `.example`, and would work.

**this**

- Directly bound events - `this` is the element where the event was attached
- Delegated events - `this` is the element which matches the selector

```js
$('section > header').on('click', ".actions a", function(e) { ... }
```

In this case, `this` inside the `on` callback would be the `a` tag.

**e.currentTarget vs. e.target**

Typically, `e.currentTarget` his property will be equal to the `this` of the function.

**Benefits**

1) Opportunity to reduce code duplification

`like` and `favorite` do very similar things, with only the url being different

```js
  like: function(e) {
    e.preventDefault();
    $.ajax({
      url: "/photos/like",
      type: "POST",
      context: this,
      data: "photo_id=" + photosJSON[currentIndex].id,
      success: function(json) {
        photosJSON[currentIndex].likes = json.total;
        this.renderPhotoInformation(currentIndex);
      }
    });
  },
  favorite: function(e) {
    e.preventDefault();
    $.ajax({
      url: "/photos/favorite",
      type: "POST",
      ...
```

```js
get: function(e) {
      e.preventDefault();
      var $e = $(e.target);

      $.ajax({
        url: $e.attr("href"),
        type: "POST",
        data: "photo_id=" + $e.attr("data-id"),
      }).done(function(json) {
        var socialTypePlural = this.url.substring(this.url.lastIndexOf('/') + 1) + "s"; // returns either favorites or likes
        photosJSON[currentIndex][socialTypePlural] = json.total;
        $('section > header').html(templates.photo_information(photosJSON[currentIndex]));
      });
    }
```


##### Efficient event handling

Creating an event hanlder for many elements is a bit expensive.

```html
<ul>
  <li>
    <p>Bananas</p>
    <a href="#">Remove</a>
  </li>
  <!-- 29 more list items, each with a remove anchor -->
</ul>
```
```js
// This callback is bound to each anchor, making 30 event handlers in memory
$('a').on('click', function(e) {
  e.preventDefault();
  $(this).closest('li').remove();
});
```

Using delegated events can help

```js
$('ul').on('click', 'a', function(e) {
  e.preventDefault();
  $(e.target).closest('li').remove();
});
```

This uses one event listener that checks for anchor clicks

##### Cleaning up conditional logic

Open external links in a new window

```js
$("#list" ).on( "click", "a[href^='http']", function( event ) {
    $( this ).attr( "target", "_blank" );
});
```

**Note**

The context of a delegated event callback (`this`) will be the parent element. In the above example that would be `#list`. The event will be the actual element acted upon, so you can get the specific element through something like `e.target`.

#### Namespaced events

You may have multiple click events bound to an element, but you only want one of them fired. Calling this `$(this).off` would remove all events.

```js
  $("#namespaced").on("click", function(e) {
    alert("Removing all events");
    $(this).off("click");
  });

  $("#namespaced").on("click", highlight);
```

However you can use namespacing to only remove certain events. Below, the `alert` event will now only fire once and the `highlight` functionality will remain

```js
$("#namespaced").on("click.alert", function(e) {
  alert("Now removing only the alert event");
  $(this).off("click.alert");
});
```

If you wanted to remove mutliple different events with the same namespace, you could leave off the event type

```js
$("#namespaced").on("click.alert" ...
  ...    
  $(this).off(".alert");
```

If you did not want to use namespacing at all you could also could specify the handler using the event from the callback

```js
  $("#namespaced").on("click", function(e) {
    alert("Now removing only the alert event");
    $(this).off(e);
  });
```

#### Clearing events

It's often a good idea to remove previously bound events when creating new ones

`$(document).off("keypress").on("keypress", function(e) {`

#### Stopping event propogation

It's common to want to stop the click event action from happening

```js
$('a').on('click', function(e) {
  e.preventDefault();
```

The event will continue to travel up the DOM tree, and might travel on a path that looks similar to this

```html
<a>
<li>
<ul #list>
<div #container>
<body>
<html>
document root
```

To stop the event from propogating further you can call `e.stopPropogation()`

If you wanted to prevent default and stop propogation, you could return false from the function. Here's an example of doing so in a one-liner.

```js
$('a').on('click', false)
```

#### Specifying a default event on page load with `on()`

This method executes a click event on page load.

```html
<ul>
  <li><a class="drawing-method">Circle</a></li>
  <li><a class="drawing-method">Square</a></li>
</ul>
```
```js
$('a.drawing-method').on('click', function(e) {
  e.preventDefault();

  $(this).closest("ul").find('.active').removeClass('.active');
  $(this).addClass('active')
}).eq(0).click();
```

`on()` returns a jQuery object, which is a collection of `a` tags in this case. The default event fires by selecting the first tag with `eq` and manually triggering a `click` event.

### Functions

#### `proxy`

Takes a function and returns a new one that will always have a particular context.

### Ajax

Required

- url
- `success` method OR `done` chained function

Other:

- type (default is GET)
- data (appended as query param)

#### Organizing ajax calls in objects

To get a better high level understanding of the code it's often helpful to organize code into objects.

Say you have a `comments` object with a method `getCommentsFor` that returns the comments for a specified object. If we want to take advantage of other methods defined on the `comments` object inside the success callback we'll have to manually set the context.

```js
var comments = {
    getCommentsFor: function(id) {
      $.ajax({
        url: "/comments",
        data: "photo_id=" + id,
        context: this,
        success: function(commentJSON) {
          this.display(commentJSON);
          this.bindEvent();   // Ensure that binding occurs after successful rendering of content
        }
      });
    },
    display: function () { ... },
```

By default the context will be a response object, and we need to set the context to the `comments` object. Therefore we use the `context` setting, set to `this`. Now when `comments.getCommentsFor` is called the context will `comments` within the callback.

### Binding ajax method calls as event handlers - extending objects

If an object method containing an Ajax call is bound to an event, there is some added complication

- the method's context must be explicitly bound to `this`
- the ajax call must use `this` as the `context` setting

```js
var socialInfo = {
    bindEvents: function() {
      $('section > header').on('click', ".actions a", socialInfo.get.bind(this));
    },
    renderPhotoInformation: function(index) { ... },
    get: function(e) {
      e.preventDefault();

      $.ajax({
        url: $e.attr("href"),
        type: "POST",
        data: "photo_id=" + $e.attr("data-id"),
        // comments methods and properties copied to the event,
        // which will be the callback context
        context: $.extend(e, this),

      }).done(function(json) {
        var $e = $(this.target);
        var url = $e.attr("href");
        // returns either favorites or likes
        var socialTypePlural = url.substring(url.lastIndexOf('/') + 1) + "s";
        photosJSON[currentIndex][socialTypePlural] = json.total;
        this.renderPhotoInformation(currentIndex);
      });
    }
  };
```

If you need to access the DOM element in the success callback as well, then you need to extend either the `comments` object to include DOM event data or vice versa.

### Good jquery code

#### Variable naming

Prepend variables with `$` to denote it's a jQuery object.

#### Meaningful function names

**Add names to document ready functions**

Helpful if you are using multiple large functions.

`$(function calculateStudentInterests()  ... });`

#### Reduce function calls

If efficiency is important for you, then this can be a good thing to do. Also, more function calls means slower code execution and a more tangled debugging process.

**last()**

```js
var $lis = $("li");
$lis.last().addClass("last");
```

`last` is a convenience call to `eq(-1)`

* Using `eq` may be less function calls
* `eq` may not be as semantically clear as `last()`

#### Code brevity

* Toggle classes, not CSS, in your jQuery JS
* Make use of `toggleClass` (rather than add/remove class)

#### Efficiency

* Store selectors as variables - don't search again.
* Make use of `find` - If you do something once you don't need a variable, but `find` is faster than a new `$()` DOM search.

### Troubleshoting

**Loading issues**

* Check if jQuery is working in the browser console

`$('body')`

This should return something

* Always link any scripts files that use jQuery after you link the jQuery library itself.

```html
<script src="js/jquery-1.12.4.js"></script>
<script src="js/scripts.js"></script>
```

### HTML Data Attributes

#### Get or set the value of an HTML data attribute

**jQuery**

Use the `.attr()` method. As a setter method, `attr()` will change the HTML markup.

**JS**

`attributes` - `e.target.attributes['data-id'].value`

`dataset` - `e.target.dataset.id`

#### Set and retrieve custom data on an element after the page has been rendered

**`data()` vs. `attr()`**

`.data()` - As a setter method, `data()` will store the value on the node that can be retrieved with the `data()` method as a getter, but it will not update the HTML markup.

`attr()` - As a setter method, it will modify the page's HTML.

```html
<article data-block="gold">
  <h1>Gold Sponsors</h1>
</article>

<article data-block="silver">
  <h1>Silver Sponsors</h1>
</article>

<article data-block="bronze">
  <h1>Bronze Sponsors</h1>
</article>
```

Note how `attr()` require a bit more verbose syntax.

```js
<a href="#" data-block="gold">Gold Sponsors</a>
var $a = $('a[data-block=gold]');

console.log($a.attr('data-block')); // gold
console.log($a.data('block')); // gold

$a.data('block', 'silver');

console.log($a.attr('data-block')); // gold
console.log($a.data('block')); // silver
```

#### Hyphenated data properties

Data properties with hyphens are formatted as camel-cased, and therefore should be accessed this way using vanilla JS.

```html
<div id="div" data-date-of-birth="28-02-1981"></div>
```
```js
var date = document.getElementById('div');
console.log(date.dataset.dateOfBirth);
```

However using jQuery this is not necessary.

```js
console.log($(date).data('date-of-birth'));
console.log($(date).attr('data-date-of-birth'));
```

## Handlebars

**Basic use case**

1) Compile HTML from script tag into Handlebars function (stored as a variable)  
2) Render template with context JSON

```html
<!-- /test.html -->
<body>
  <script id="itemsTemplate" type="text/x-handlebars">
    {{#each items}}
  	  <li>{{.}}</li>
    {{/each}}
  </script>
  <main>
    <ul id="list">
    </ul>
  </main>
</body>
```

```js
// /test.js
// Compile Handlebars function
var itemsTemplate = Handlebars.compile($('#itemsTemplate').html());
// Render template with context
var products = ['Apple', 'Banana'];
$('#list').html(itemsTemplate({ items: products }))
```

**Partial**

2) Register partial  
3) Render template with JSON context  

```html
<!-- /test.html -->
<body>
  <ul id="list"></ul>
  <script id="itemsTemplate" type="text/x-handlebars">
  {{#each items}}
  	{{> basicTemplate}}
  {{/each}}
  </script>
  <script id="basicTemplate" type="text/x-handlebars">
    <li>{{.}}</li>
  </script>
...
```

```js
// /test.js
...
Handlebars.registerPartial('basicTemplate, $('#basicTemplate').html());
$('#list').html(itemsTemplate({ items: products }));
```

[Handlebars codepen example](https://codepen.io/dylankb/pen/dvLaPM?editors=1011)

**Checking for a partial**

Type `Handlebars.partials` into the console to see registered partials

You could render an object `item` using a partial named `item` like so:

```js
Handlebars.partials.item(item.toJSON()));
```

**Handlebars keywords**

`>` - tells Handlebars to look for a partial with the name `basicTemplate`  
`@key` - current key of iteration  
`@index` - current index of iteration  
`{{.}}` - equivalent to `{{this}}` (current object in iteration)  

A template could also just be a string of Handlebars code that's then compiled to a function instead of a script tag.

```js
var Handlebars = require('handlebars');
var template = '{{#each foo}}\n{{@key}}:{{.}}!\n{{/each}}';

var render = Handlebars.compile(template);
var data = {
  "foo": {
    "first": "Hello",
    "second": "World"
  }
};
console.log(render(data));
// first:Hello!
// second:World!
```

### Precompiled scripts

Compilation is the most expensive part of Handlebars, so we can do it ahead of time.

- `npm install handlebars -g`
- Follow the rest of these instructions for how to precompile your templates [here](https://github.com/sitepoint-editors/handlebars-precompilation-demo)

Handy command:

`handlebars templates/ -f fileNameOfCompiledTemplates.js`

## Localstorage

Localstorage

* No expiration - on desktop may remain indefinitely (mobile safari may delete)
* Up to 5MB
* Data as key-value pairs

Cookies

* Has expiration date
* Holds 4KB
* Data stored as a string

`window.sessionStorage` - only lasts the current session (tab / window closed)
`window.localStorage` - stays around after the browser window or tab closes

**`setItem()`**

`localStorage.setItem(keyString, valueString)`

**`getItem()`**

`localStorage.setItem(keyString, valueString)`

**Dealing with Objects/Strings**

Non-string values will have `toString()` called on them. So how do you save objects? The solution is to use `JSON.parse` and `JSON.stringify`

When setting a value, pass the JS object into `JSON.stringify()`. When getting a value use `JSON.parse` which takes a string of JSON and converts it back to a JavaScript object.

```js
var person = {
  name: 'Amanda Rose',
  bgColor: '#ff0000'
};

function setPerson(personToSave) {
  localStorage.setItem('person', JSON.stringify(personToSave));
}

function getPerson() {
  return JSON.parse(localStorage.getItem('person'));
}
```

**Save on page close**

`unload` event fires when the browser or tab closes.

$(window).on("unload", function() {
    localStorage.setItem("note", $("textarea").val());
});

## ES6

### `let` and `const`

#### `let`

`let` instantiates block scoped variables

```
let a = 2;
{
  let a = 3;
  console.log( a );	// 3
}

console.log( a );	// 2
```

Here's a slightly more common example

```js
let a = 2;

if (true) {
  let b = 5;
  for (let i = a; i <= b; i++) {
    console.log(i); // 2, 3, 4, ...
  }
  // console.log(i) // ReferenceError
}
// console.log(b) // ReferenceError
```

The `for` loop instantiating `i` with `let` reassigns on each iteration. `var` has no such restriction to block scoping.

```js
let a = 2;

if (true) {
  var b = 5;
  for (var i = a;i <= b; i++) {
    console.log(i); // 2, 3, 4, ...
  }
  console.log(i, 'hey') // 6 'hey'
}
console.log(b) // 5
window.i       // 6
```

**`for` and `let`**

Here's a bit of unintuitive ES5 code:

```js
var funcs = [];

for (var i = 0; i < 5; i++) {
	funcs.push( function(){
		console.log( i );
	} );
}

funcs[3](); // 5
```

The problem is there is only one `i` in the outer scope that was closed over.

If you use `for (let i = 0; i < 5; i++) {`, let declares an `i` not just for the for loop itself, but it redeclares a new `i` for each iteration of the loop. That means that closures created inside the loop iteration close over those per-iteration variables the way you wouldd expect.[^1]

The `for` shorthand can obscure some of this, but here is an equivalent to a `let` in a `for` header.

```js
var funcs = [];

for (var i = 0; i < 5; i++) {
	let j = i;
	funcs.push( function(){
		console.log( j );
	} );
}

funcs[3]();		// 3
```

We are defining a `let` within a block scope, and `let` is a block scoped variable so it correctly closes over, making the correct `i` accessible to the function.

#### `const`

That variable reference cannot be reassigned, but object internals can be.

```js
const a = [1,2,3]
a.push(4) # [1,2,3,4]
const a = 42 # ReferrenceError
```

### Shorthand property declaration

```js
// ES5
var a = 5;
var objA = { a: a };
```

```js
// ES6
let a = 5;
let objA = { a };
```

### Splat/spread operator

#### Combining / Gathering

#### Objects

1) spread operator

**Copy objects**

```js
// ES6
let objB = { b : 5 };
let objA = { a: 1 };

let c = { ...objA, ...objB }
console.log(c) // { a: 1, b: 5 }
```

The spread operator iterates over the properties in `objA` and `objB` and assigns them to the new object.

**Copy + Overwrite**

This is a useful tool in writing pure functions

```
const oldThread = state.threads[threadIndex];
const newThread = {
  ...oldThread,
  messages: oldThread.messages.concat(newMessage),    
};
```

- `...oldThread` copies all of the properties from `oldThread` to `newThread`:
- `messages: oldThread.messages.concat(newMessage)` sets the messages property of newThread to the new messages array that containsnewMessage:

Note that by having the property messages appear after oldThread, we’re effectively “overwriting” the messages property from oldThread.

2) `Object.assign()`

```js
...
let c = Object.assign( {}, objA, objB);
```

**Copy + Overwrite**

We can do the same thing in the ES6 example with `Object.assign`.

```js
Object.assign({}, oldThread, {  messages: oldThread.messages.concat(newMessage),});
```

#### Values

```js
function foo(...args) {
	console.log( args );
}

foo( 1, 2, 3, 4, 5);  // [1,2,3,4,5]
```

In ES5 `apply`

```js
foo.apply( null, [1,2,3] );
```

### Destructuring

#### Object properties

Both arrays and object can assign values to named variables:

```js
const car = { model: 'Ford' };
const { model } = car; // const model = car.model;
model; // 'Ford'
```

```
let tenses = ["I", "you", "me"]
let [ firstPerson, secondPerson ] = tenses;
firstPerson // "I"
```

#### Using destructuring to make method invocations clearer

If can't see how a function is defined, then code like this is down right confusing.

```js
Albums.set(albums, true, false)
```

We can probably intuit what the `albums` param is, but we have no idea what this darn false is.

ES6 brings some new features to the table that makes this situation a bit better.

**Default params**

You can do some type checking in ES5 to get the same affect, but it's not very clean looking. In ES6 it's very simple, just use the `=` sign in the method signature.

```js
export default {
  set(albums, incrementId=true, explodeBomb=false) {...};
}
```

Default params / optional arguments are pretty cool, but they don't really help with making vague params like `true` make sense when you see them invoked.

**Destructured params**

To be a bit clearer with what arguments you were passing in ES5, you could pass in an object.

```js
var personInfo = { weight : 170, height: 72, max: 25 };
calcBmi(personInfo);
```

The problem was your method signature would then be less clear, or at least a bit reptitive.

```js
function calcBmi(args) {
  var weight = args.weight;
  var height = args.height;
  var max = args.max;
  var callback = args.callback;

  // the actual function ...
}
```

Now you can do something like this:

```js
function calcBmi({ weight: w, height, callback, max }) {
  console.log(max); // 25
  console.log(w); // 170
}
```

Note that the number and order of the arguments are now flexible.

#### Optional args object

Options object can help provide flexible parameters to your function.

```js
Albums.set(albums, { incrementId: true, explodeBomb: false });  
```

However, as is you need to pass in this options object every time. ES6 gives us some additional flexibility here.

```js
set(albums, { initializeFooToOne: true, explodeBomb: false } = {}) {...};
```

Now we can leave off the options object if we want.

```js
Albums.set(albums, { explodeBomb: true });
Albums.set(albums, { {initializeFooToOne: true });
Albums.set(albums);
```

In the last three examples of `set` invocations, the variable `initializeFooToOne` is always `true`.

Background on this technique and dealing with destructred params in ES6 [here](http://2ality.com/2015/01/es6-destructuring.html#simulating-named-parameters-in-javascript)

### Rest

Rest gathers individual elements together into an array

```js
const aTail = (head, ...tail) => tail;
aTail(1, 2, 3); // [2, 3]
```

### Spread

**Collecting components**

Spread does the opposite of rest: it spreads the elements from an array to individual elements.

```js
let num = [1]
let largerNums = [2,3]
[num, ...largerNums] // [1,2,3]
```

```js
const shiftToLast = (head, ...tail) => [...tail, head];
shiftToLast(1, 2, 3); // [2, 3, 1]
```

Which works as long as the second argument is iterable

```js
num = 1;
[num, ...largerNums] // [1,2,3]

let largerNum = 3;
let nums = [1,2]
[nums, ...largerNum] // largerNum is not iterable
```

**Cloning**

This technique is also useful for cloning:

```js
moreNums = [...largerNums]
// [2,3]
```

### Arrow functions

#### Abbreviated function syntax

Example of equivalent functions

```js
do.something(function(a, b) { return a + b; } // ES5
do.something((a,b) => { return a + b; }) // ES6 - no function
do.something((a,b) => (a + b))           // ES6 - implicit return
do.something((a,b) => a + b)             // ES6 - minimum parens
```

Equivalent example

```js
[5,6].map(function(num, index) { return num + index }); // ES5
[5,6].map((num, index) => { return num + index });      // ES6 - no function
[5,6].map((num, index) => (num + index));               // ES6 - implicit return
[5,6].map((num, index) => num + index);                 // ES6 - minimum parens
```

Single argument functions can be made even terser.

```js
[0,2,4].map((a) => { return ++a });  // ES6
[0,2,4].map(a => { return ++a });    // ES6 w/out extra parens
[0,2,4].map((a) => (++a);            // ES6 w/out return statment
[0,2,4].map(a => ++a)                // ES6 single arg shorthand
```

Here's a nested loop example as well.

```js
let arrays = [[1,2],[3,4]];
// ES5
arrays.forEach(function(nums) {
  nums.forEach(function(num) {
    console.log(num);
  }
}

// ES6
arrays.forEach(nums => nums.forEach(num => console.log(num)) )
```

#### Automatic context binding

This code will now work without manual binding, which is convenient.

```js
var person = {
  age: 29,
  intro: () => { console.log("I'm" + this.age) }
};

var intro = person.intro()
intro() // 'I'm 29'
```

**When it is not helpful**

Watch out when using this with something like jQuery - you may lose jQuery `this` or the current element in an event handler.

### Classes

Is this ES2017/ES7?

```js
class Me {
  constructor(name) {
    this.name = name;
  };

  sayHello() {
    console.log('Hi ' + this.name);
    return 1;
  }
}

const _Me = new Me('Dylan');

console.log(_Me.sayHello()); // 'Hi Dylan'
```

More examples

```js
class Parent {
 constructor() {}
 bar() { console.log('bar'); }
 static foo() { console.log('foo') }
}

var parent = new Parent()
parent.bar();
Parent.foo()

class Child extends Parent {
  baz() { console.log('baz') }
}

var child = new Child();
child.baz()
```

```
class Bar extends Foo {
  constructor(props) {
    super(props)

    // The rest of the implementation
  }
}

Function Bar() {
  Foo.apply(this);

  // the rest
}
```

### Module import / export

Simple example.

```js
// myModule.js
export default {
  module: 'a module',
}

// other file
import myModule from 'myModule';
```

Exporting a function

```js
export function createTodo(text) {
 ...
}

import * as Actions from 'Actions';
```

A bit more complicated.

```js
export const routeByWindowWidth = (props, nextProps, route, maxWidth) => {
    const { router, windowWidth } = props;
    if (nextProps.windowWidth !== windowWidth && nextProps.windowWidth < maxWidth) {
        router.push(route);
    }
};

import { routeByWindowWidth } from './utils/routeByWindowWidth';
```

### Generator function

Generator function which returns a promise which is thenable.

```js
async function() {
  var friends = await $.get("http://somesite.com/friends");
  console.log(friends);
}
```

### Running babel from the command line

Based off an existing repo's `package.json`, but it should work.

First install `babel-cli` npm module, and then you should be able to execute babel through the node modules.

`./node_modules/.bin/babel-node app.js`

## Linting

### Airbnb rules (ES5)

Setting up ESLint with Airbnb rules in Atom for ES5

Reference [this comment](https://github.com/airbnb/javascript/issues/451#issuecomment-275902038) to learn about ES5 linting:

Basically make sure you're:

1. Installing `eslint-config-airbnb-base`
2. Extending `airbnb-base/legacy` in your `.eslintrc`
3. Install package dependencies and the package itself with this fancy bash script:

```bash
export PKG=eslint-config-airbnb-base;
npm info "$PKG" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG"
```

Bash script lifted from [this blog post](http://www.acuriousanimal.com/2016/08/14/configuring-atom-with-eslint.html).

If you don't want to run the command then npm installing `eslint`, `eslint-plugin-import`, and then `eslint-config-airbnb-base` should work.

4. Install linter-eslint for Atom.

Notes:

Instead of using `airbnb-base/legacy` you might be able to use this package, but I haven't tried it:
https://www.npmjs.com/package/eslint-config-airbnb-es5

**Library syntax errors**

Make sure your tests are specified in the env option. Same goes if you're using something like jQuery.
https://github.com/tlvince/eslint-plugin-jasmine/issues/56

**CLI**

Once you've done all of the above, you can also use ESLint as a CLI if you wish. Here's how you'd do that
in the context of your local directory/project.

`./node_modules/.bin/eslint yourfile.js`

https://eslint.org/docs/user-guide/getting-started#local-installation-and-usage

You could also do a global install, but then you'd also have to do a global install of `eslint-config-airbnb`, and following that pattern  could get messy as you switched global ESLint configs over time and across projects.

### Functional ideas

#### Avoiding reassigning params (even with accumulators)

Many ESLint setups [flag](https://eslint.org/docs/rules/no-param-reassignhttps://eslint.org/docs/rules/no-param-reassign) param reassignment and mutation (modifying object internals). This issue even comes up when you [using reduce](https://github.com/eslint/eslint/issues/8581), which IMO isn't a big issue. The problem is that ESLint has no way to recognize the reduce accumulator param as something safe to mutate.

Say you had an `inputs` variable that looked like this:

```js
[
  0 : {name: "progress", value: "0.0"},
  1 : {name: "level", value: "2"}
]
```

and you wanted to turn it into object whether the "name" value's key was "values" value. I.e

```js
[ { "progress": "0.0" }, ... ]
```

This is how you'd normally do this with reduce, but ESLint doesn't like the param re-assignment that's happening (again, as an accumulator it's probably a pretty safe object to mutate).

```js
return inputs.reduce((formObject, item) => {
  formObject[item.name] = item.value; // eslint-disable-line no-param-reassign
  return formObject;
}, {});
```

What you can do instead is return a new accumulator each time.

```js
return inputs.reduce((formObject, item) => (
  { ...formObject, [item.name]: item.value }
), {});
```

Note the need for brackets when setting the key.

https://github.com/airbnb/javascript/issues/1342

## Node

### Setup

- Uninstall any previous node installations [here](https://stackoverflow.com/questions/11177954/how-do-i-completely-uninstall-node-js-and-reinstall-from-beginning-mac-os-x)
- Use one of the nvm [install scripts](https://github.com/creationix/nvm#installation)
- `nvm install --lts`
- `nvm alias default $NODE_VERSION` (preserves default between sessions, see [here](https://stackoverflow.com/questions/24585261/nvm-keeps-forgetting-node-in-new-terminal-session)

[^1]: https://github.com/getify/You-Dont-Know-JS/blob/master/es6%20%26%20beyond/ch2.md#let--for
