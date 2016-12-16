# javascript-all-in-one  


## var Hoisting

```codes
(function() {
  var foo = 1;
  console(foo + " " + bar + " " + baz);
  var bar = 2;
  var baz = 3;
})();
// 1, 2, 3

/*it equal to*/

var foo, bar, baz;
(function() {
  foo = 1;
  console(foo + " " + bar + " " + baz);
  // now bar, baz not be assigned any value, so it is === undefined !
  bar = 2;
  baz = 3;
})();
// 1 undefined undefined 
``` 




