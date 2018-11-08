# FUNctions!!

[![Conjunction Junction](./assets/conjunction_junction.png)](https://www.youtube.com/watch?v=5kTvLVRXcJs "Conjunction Junction Schoolhouse Rock")

Functions are perhaps the most important tool in Javascript for executing code.

Functions are simply snippets of code we build that can be used over and over again.

Functions have 3 major parts to them: input (arguments/parameters), code, and output(return value).

```
var alertUser = function() {
  alert("Aren't you tired of this example yet?")
}

alertUser()
```

In the above code, we create our function, alertUser.

First, we DEFINE our function, or we simply let JS know that we have created a function for use.
Once we have defined our function, we can call it as many times as we need!

Then, we INVOKE or CALL our function (alertUser()), which is what tells JS to actually RUN the function.
```
alertUser()
alertUser()
alertUser()
```
In our alertUser() function above, we simply run a given block of code with no input.

<hr>

Let's create a function that takes input! In javascript, we call function inputs *arguments* or *parameters*.

I want to make a simple function that takes in any number and returns the square of that number.

```
function square(num) {
  console.log(num**2)
}

square(3)
square(10)
square(500)
```

In the above code, I define a function called "square" that takes in exactly one argument (a number) and then
console logs the square root of that number.

Then, I invoke function, passing in different arguments each time. (3, 10 and 500).

What happens if I ...
```
square()
square("number?")
```

Note that NaN stands for "Not a Number". This makes sense when you try to square a string. JS returns NaN!

Note that generally speaking, you should always pass the same number of arguments when invoking a function as
the given defined function asks for.

<hr>

Making a function that has multiple arguments...
```
function multiply(num1, num2) {
  console.log(num1 * num2)
}

multiply(5, 5)
```

With newer features of JS, you can predefine an argument value IF none is provided as follows:
```
function multiply(num1, num2=5) {
  console.log(num1 * num2)
}

multiply(10)
multiply(10, 10)
```
In the example above, if we don't pass in the second argument when invoking our function "multiply", it defaults
to the value of 5, according to our defined function.

<hr>
Finally, as previously mentioned, a function typically has a third component which is an output.
We typically refer to this as a return value.

Did you notice that whenever we invoked a function in our console, after our console log outputs,
the console always returned a value of undefined?

This is because in JS, a function is expected to return some kind of value.

For instance in our multiply example...
```
function multiply(num1, num2) {
  return num1 * num2
}

multiply(2, 4)
```

In JS functions, we typically *return* some kind of value after our function runs instead of console logging it.
*return* is a keyword in Javascript used in functions, that simply states that our function will return some value!

Since functions should always return some value, we can do things like this...
```
let value = square(5)
let value2 = square(6)
```

What would happen if we did something like this?
```
value3 = square(square(10))
value4 = square(multiply(5, 5))
```

Yes! We can chain functions together. Since functions are expected to return some value, we can use their return
values and plug it into some other function.

Ultimately, we can create and invoke as many functions as needed to solve the problem at hand.

### Exercises

**Shopping**

1. Create a function called add that takes two number parameters and returns the sum of their values.

2. Create a function called finalSalesGenerator that takes in a number value(item retail price), and returns the total cost after sales tax, given a sales tax of 7.75%

3. Create a function called logThis that takes a given parameter, and returns a console log value of "I am logging a value of" plus the given argument.

Finally, help me figure out how much money exactly I would need on my shopping expedition (including sales tax), using the functions you've defined above.
I want to purchase...
<ul>
<li> Shoes: $65
<li> Sunglasses: $150
<li> Shirt: $25
</ul>

Make sure to console log the final value!

<hr>

**Tipping**

Your task is to make a function that calculates the total bill including tip.

Create a function called tipCalculator that takes in two arguments: the total and the tip.

The function should return the final bill after tip is calculated.

Note that if no tip is provided, the function should default it to 15%. However,
if no "total" argument is provided, instead of returning the final bill, console log
"A total must be provided".
