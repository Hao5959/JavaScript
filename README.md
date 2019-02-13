# JavaScript

- [A link for some js interview questions](https://github.com/khan4019/front-end-Interview-Questions#javascript-basics-and-tricky-questions)
- [33 must know questions](https://github.com/stephentian/33-js-concepts)
- [leetcode solutions in js](https://github.com/jyxia/LeetCode-JavaScript)
- [you don't know js](https://github.com/getify/You-Dont-Know-JS)
- [git](http://rogerdudler.github.io/git-guide/index.zh.html)
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
