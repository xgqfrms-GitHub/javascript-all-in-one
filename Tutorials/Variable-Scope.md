# Variable Scope

https://www.sitepoint.com/demystifying-javascript-variable-scope-hoisting/  


```codes
var locales = {
  europe: function() {          // The Europe continent's local scope
    var myFriend = "Monique";

    var france = function() {   // The France country's local scope
      var paris = function() {  // The Paris city's local scope
        console.log(myFriend);
      };

      paris();
    };

    france();
  }
};

locales.europe();
``` 




