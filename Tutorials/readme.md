# javascript-all-in-one  


## var Hoisting (JavaScript仅提升变量/函数声明，而不提升变量的初始化值。)

```codes
(function() {
  var foo = 1;
  console.log(foo + " " + bar + " " + baz);
  var bar = 2;
  var baz = 3;
})();
// 1, 2, 3

/*it equal to*/

var foo, bar, baz;
(function() {
  foo = 1;
  console.log(foo + " " + bar + " " + baz);
  // now bar, baz not be assigned any value, so it is === undefined !
  bar = 2;
  baz = 3;
})();
// 1 undefined undefined 
``` 

## Function Hoisting

```codes
foo();
function foo() {
  console.log("Hello!");
}
// Hello

foo();
var foo = function() {
  console.log("Hello!");
};
// foo is not a function

/*it equal to*/

var foo;
foo(); // foo was referenced before it be assigned value!
foo = function() {
  console.log("Hello!");
};
// foo is not a function
``` 


