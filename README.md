# JavaScript
<!DOCTYPE html>
<html>
  <head></head>
  <body>
    <a href='https://github.com/khan4019/front-end-Interview-Questions#javascript-basics-and-tricky-questions'>
    A link for some js questions
    </a>
    <h3>Call Stack</h3>
    <p>
    1. let 
      1.1 basic use of let 
      1.2 let 不能被提升
      1.3 temperate death zone
    ES6 规定，如果区块中存在let和const命令，这些区块对这些命令声明的变量从一开始就形成了封闭的闭合区间。凡是在声明之前使用这些变量就会报错。
    🌰：
    if(true) {
    // TDZ begin
    a = 'abc';      // ReferenceError
    console.log(a); // ReferenceError
    
    let a; // TDZ end
    console.log(a); //undefined
    
    a = '123';
    console.log(a); //3
      1.4 不能被重复声明
  
  2. strings
  3. Arrow Function 

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
    </p>
  </body>
</html>
