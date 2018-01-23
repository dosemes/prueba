---
layout: post
title:  "Refactoring: use ES6"
categories: projects SimpleDebugger refactoring es6
---

## ES6

When I started [SimpleDebugger] 5 years ago the [ES5] was a standard. So I refactored code to ES6 using `class` and moving stuff to separate modules. `index.js` file is only start point code. Its grabbing all needed files and exports the main module which is [SimpleDebugger].

### Class

I don’t really like this thing because it causes confusion about objects in JavaScript. I hope it is well known that JavaScript has prototype based architecture. There are no classes in JS.

I love prototypes. It is so different from class object-oriented architecture. I feel prototypes gives developer more freedom than classes. Prototypes are more flexible.

Sure it is cool to have some shortcut to define `Constructors` (I will write post what I mean `"Constructors"` in near future or you can read about it: [From constructors to classes]) and I really don’t know why the `class` is chosen.

I used it in [SimpleDebugger] and it works fine.

### [Modules]

I moved [SimpleDebugger] Constructor and **removeNode()** to separate files.

[SimpleDebugger] has its own file and it exports only this module.

I moved **removeNode()** to **dom.js**. This function is not the default of this module. I think **dom** module will not have any default. It will be the collection of functions to do stuff on DOM.

## Satisfy TODO notes

## Added bump version npm script

## Things to do

- (add smth...)

## Things I done

- (list things you've done)

[SimpleDebugger]: https://github.com/th3mon/SimpleDebugger
[ES5]: https://en.wikipedia.org/wiki/ECMAScript
[From constructors to classes]: http://exploringjs.com/es6/ch_core-features.html#sec_from-constr-to-class
[modules]: http://exploringjs.com/es6/ch_modules.html
[Modules]: http://exploringjs.com/es6/ch_modules.html