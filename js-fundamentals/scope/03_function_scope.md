# Scoping in Functions!

```
//Global Scope (convertFahrenheitToCelsius, tempOne, tempTwo)
  //Local Scope or FUNCTION SCOPE (fahrenheit, celsius)

let convertFahrenheitToCelsius = function(fahrenheit) {
  let celsius = (fahrenheit - 32) * 5/9
  return celsius
}

let tempOne = convertFahrenheitToCelsius(32)
let tempTwo = convertFahrenheitToCelsius(69)

console.log(tempOne)
console.log(tempTwo)
console.log(celsius)
```

In the code above, we have a function that converts Fahrenheit to Celsius.

The following variables (convertFahrenheitToCelsius, tempOne, and tempTwo) exist
in our global scope.

The following variables (fahrenheit which is our function argument, and celsius which
we instantiated WITHIN our function) exist in the local scope of our function.

In other words, we cannot access celsius in our console.log(celsius) because it doesn't
exist in the global scope!

Note that function scope is a type of local scope in Javascript and is slightly different
from block scope (for example, when we create variables in an if() block statement), but
more on that later...

For now, recognize that variables created in a function are in the local scope of the function
and cannot be accessed from outside!
