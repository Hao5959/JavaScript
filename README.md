# JavaScript

- [A link for some js interview questions](https://github.com/khan4019/front-end-Interview-Questions#javascript-basics-and-tricky-questions)
- [33 must know questions](https://github.com/stephentian/33-js-concepts)
- [leetcode solutions in js](https://github.com/jyxia/LeetCode-JavaScript)
- [you don't know js](https://github.com/getify/You-Dont-Know-JS)
- [git](http://rogerdudler.github.io/git-guide/index.zh.html)

If you haven’t worked with JavaScript in the last few years, these three points should give you enough knowledge to feel comfortable reading the React documentation:

* We define variables with [`let`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let) and [`const`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/const) statements. For the purposes of the React documentation, you can consider them equivalent to [`var`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/var).
* We use the `class` keyword to define [JavaScript classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes). There are two things worth remembering about them. Firstly, unlike with objects, you *don't* need to put commas between class method definitions. Secondly, unlike many other languages with classes, in JavaScript the value of `this` in a method [depends on how it is called](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes#Boxing_with_prototype_and_static_methods).
* We sometimes use `=>` to define ["arrow functions"](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions). They're like regular functions, but shorter. For example, `x => x * 2` is roughly equivalent to `function(x) { return x * 2; }`. Importantly, arrow functions [don't have their own `this` value](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions#No_separate_this) so they're handy when you want to preserve the `this` value from an outer method definition.

**Don't worry if this is too much to take in at once. The [MDN JavaScript Reference](https://developer.mozilla.org/en-US/docs/Web/JavaScript) is a stellar resource, and you can consult it whenever you get confused by something.**

Also, when you feel unsure about what some newer syntax means, you can use the [Babel REPL with the ES2015 preset](http://babeljs.io/repl/#?babili=false&browsers=&build=&builtIns=false&code_lz=MYewdgzgLgBAllApgWwjAvDA2gRgDQwBMBAzALoDcAUKJLACYgCuARgDaL0bxKoB0yAIYAHABQAPDAD4YkgFREAlBSA&debug=false&forceAllTransforms=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&lineWrap=true&presets=es2015%2Creact%2Cstage-1%2Cstage-2%2Cstage-3&prettier=true&targets=Node-6.12&version=6.26.0&envVersion=) to check what equivalent older syntax it compiles to.

# 33 must know questions for JavaScript
- Call Stack
- Primitive Values
- Value Types and Reference Types
- Implicit, Explicit, Nominal, Structuring and Duck Typing
- == vs === vs typeof
- Function Scope, Block Scope and Lexical Scope
- Expression vs Statement
- IIFE, Modules and Namespaces
# ES 6
## 1. let
   #### 1.1 basic use of let
   #### 1.2 let 不能被提升 
   #### 1.3 temperate death zone 
   ES6 规定，如果区块中存在let和const命令，这些区块对这些命令声明的变量从一开始就形成了封闭的闭合区间。凡是在声明之前使用这些变量就会报错。
  🌰：
````javascript
  if(true) {
  // TDZ begin
  a = 'abc';      // ReferenceError
  console.log(a); // ReferenceError

  let a; // TDZ end
  console.log(a); //undefined

  a = '123';
  console.log(a); //3
````
   #### 1.4 不能被重复声明

## 2. strings
## 3. Arrow Function 
```ES6
  const years = [1990, 1965, 1982, 1937];
  //ES5
  var age5 =years.map(function(el) {
    return 2019 - el;
  });
  console.log(age5);

  //ES6 第一种
  let age6 = years.map(el => 2019 - el);
  console.log(age6);

  //ES6 第二种
  let age6 = years.map((el, index) => `Age element ${index + 1}: ${2019 - el}. `);
  console.log(age6);

  //ES6 第三种
  let age6 = year.map((el, index) => {
    const now = new Date.getFullYear();
    const age = now - el;
    return `Age element ${index + 1}: ${2019 - el}.`
  });
  console.log(age6);
  ```
