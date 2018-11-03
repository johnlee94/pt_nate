# IF statements

If statements are a powerful Javascript statement that checks a condition before
running code.

Remember our isFreezing variable from earlier we used to store a Boolean value?

```
let temp = 32
let isFreezing = temp <= 32

if(isFreezing) {
  console.log("Omg it's lit outside")
}
```

Do we expect the above console log to run?

How can we change the code above so that console log doesn't run?

This is known as **flow control**, so that we can exactly control how and when certain
parts of our program runs.

<br>

To modify our code above, this would also work:
```
let temp = 32

if (temp <= 32) {
  console.log("Omg it's still lit")
}
```

This is how if statements will be more commonly used and seen in JS.

<hr>

The general skeleton of if statements looks like this:

```
if(boolean) {
  //code if boolean is true
} else if(boolean) {
  //code if this boolean is true
} else {
  //code
}
```

When the JS interpretor sees the keyword *if*, it checks to see *if* the given
condition is true, and then runs the code if it is true. If the if() statement runs,
it will ignore all the *else if* and *else* statements.

However, if the if() statement is NOT run, the JS interpretor will move on to the next
*else if* statements one by one. You can have as many else if statments in a code block
as you need. If any of the else if statements run, the JS interpretor will escape from
the code block.

Finally, if the if() and else if() statements are false and not ran, the else statement will run.
Think of the else statement as a final "catch-all" statement that will run only if all conditional
statements returned false.

CHECK YOUR UNDERSTANDING.
```
var day;

if(day === "Sunday") {
  console.log("Today is Sunday")
} else if (day === "Monday") {
  console.log("Mondays are the worst!")
} else if (day === "Tuesday") {
  console.log("ZZZ")
} else if (day === "Wednesday") {
  console.log("Half way there...")
} else if (day === "Thursday") {
  console.log("Tomorrow's Friday!!!")
} else if (day === "Friday") {
  console.log("Queue Rebecca Black's Friday...")
} else if (day === "Saturday") {
  console.log("I'm out of ideas")
} else {
  console.log("Please give me a valid day of the week.")
}
```
If we set day = "Sunday", JS will hit the first if() statement, and since the conditional
returns true, the console will log "Today is Sunday" and skip the rest of the code block.

If we set day = "Friday", JS will continue running through the code block starting from the
very first if() statement and continue to run through our else if() statements until it reaches an else if statement that has a conditional evaluating to true. (day === "Friday")

Finally, if we set day = "Something that's not a day", JS will run through all the statements, see
that none of the if or else if statements return true. It will then default to the else statment block!

<br>

What's the difference here?
```
let day = "Tuesday"
if(day === "Sunday") {
  //code
}

if(day === "Monday") {
  //code
}

if(day === "Tuesday") {
  console.log("We made it!")
}
```
In the case above, EVERY single if() statement is run. That's because each if code block is
its own domain. Else if and Else statements can ONLY be attached to an if statement!

<br>
<br>

## Logical AND / OR Operators

How can we check multiple conditions at the same time?

Let's say that a good temperature range (in Fahrenheit) to go outside is between
60 and 90 degrees. How could we model that using if statements?

We could...
```
let temp = 65
if(temp >= 60) {
  if (temp <= 90) {
    console.log("Let's go outside!")
  }
}
```

However, we have a better way using the && operator!
```
let temp = 75
if(temp >= 60 && temp <= 90) {
  console.log("Let's go outside.")
}
```

The && (double Ampersand) is the AND operator. It evaluates to true if both
conditional statements on the operator's two sides are also true.
It can be used to check multiple booleans and evaluates to true if ALL conditionals return true.

```
true && true && true // -> true
55 > 10 && "hello" === "hello" && 10 >= 10 // -> true

true && true && false // -> false
5 + 5 > 8 && 100 < 5 *5 // -> false
```

The || (double pipe symbol) is the OR operator. It evaluates to true if either conditional on the
sides of the operator is true. It also is used to check multiple booleans and ultimately evaluates to
true if ONE of the conditionals is true.

In our temperature model, how might we use the OR operator?

Let's say that it's dangerous to go outside if the tempature is below 0 degrees or
if the temperature is above 120 degrees.

```
let temp = 135
if(temp <= 0 || temp >= 120) {
  console.log("STOP! It's dangerous out there!")
}
```

How about here?

```
false || false || true // -> true
5 === 3 || 10 > 2 || 4 < 2 // -> true

false || false || false // -> false
```

CHALLENGE: What is returned in the following cases and why?
```
5 + 5 < 8 || 4 == "4" && 100 > 5

5 + 5 < 8 && 4 == "4" || false
```
<br>
<br>

### Section Wrap-up Exercises

I am opening up a hip restaurant in LA. It needs to be HIP AF! Being vegan these days
is all the rage, right?

Given these two variables,
```
guestOneIsVegan = true;
guestTwoIsVegan = false;
```

Set up an else if code block statement to see what kind of menu items I should serve.

If both guests are vegan, console log "Serve only vegan items!"
If one of the guests are vegan, console log "Serve some vegan items."
If none of the guests are vegan, console log "Serve everything!! :D"
