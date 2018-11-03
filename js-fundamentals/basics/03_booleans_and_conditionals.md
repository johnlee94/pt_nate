# Booleans

Booleans are another Javascript primitive data type.

They represent a binary data structure, or in other words, they are simply true or false.

In javascript, *true* and *false* are special keywords that are considered of boolean type.

For instance ..
```
let isBored = true
```

What kind of situations can a simple true or false data be useful for?

What about a simple room light? A light can either only be "on" or "off", and so
a boolean might be the perfect way to represent this information.

```
// The room is currently dark

let lightIsOn = false

function lightSwitch() {
  lightIsOn = !lightIsOn
}

//let's turn the light on!
lightSwitch()

//let's turn the light off..
lightSwitch()

// and then on again?
lightSwitch()
```

In the above simple lights example, we create and assign the variable lightIsOn to the
Boolean value of false (Since it says the room is currently dark 0-0)

Then we create a function to toggle the value of lightIsOn between true and false using the ! or NOT operator.
The ! operator is used to simply return the opposite of the current Boolean value.

(I know we haven't gone over what a function is yet and you may not know what a function in JS is YET, just know that a function is a special JS tool use to execute specific lines of code in certain situations)

Try in your console:
```
!true

!false
```

What do you think we would get for..
```
!!true
!!!!false
```

ALL JS values are either *truthy* or *falsey*, or can be evaluated to being true or false.

To check whether a value is truthy of falsey, you can simply run the Boolean() function!

```
Boolean(true)

Boolean(false)

Boolean(0)

Boolean(1)

Boolean(null)

Boolean(undefined)

Boolean('')

Boolean('hello')
```

YEAH, YEAH, YEAH BOOLEANS. WHATEVER. SO WHAT?

In programming, Booleans are most often used with conditionals, or comparison statements.

For example...

```
// The freezing temperature of water is 32 degrees Fahrenheit
let temp = 50
let isFreezing = temp === 32

console.log(isFreezing)
```

What is logged out?

The triple equals (===) is the strict equals comparison operator in JS. It checks to see
if two values are of same data type and of same value, and then returns a Boolean value.

How could we change the isFreezing to return a Boolean value of true?

Other comparison operators:
```
5 == "5"

"string1" !== "string2"
"nate" != "nate"

5<2
5<=2

100 > 1
100 >= 50
```

The double equals (==) loosely checks if two values are equal in JS. It checks to see if
they have the same value, but not their data type. That's why the number value of 5 and the
string value of 5 above return a value of true using this operator.


### Section Wrap-up Exercise

I suddenly win the lotto and want to open up an amusement park in honor of my greatness.
However, I am confused to how I should manage my amusement park's ticket pricing.
Would you help me?

First create a variable *age*, and set it equal to your age (You want to visit my park too right?)

Then create another variable *isChild*, and assign it to a conditional to check to see if the person is 7 years of age or younger.

Then create a third variable *isSenior*, and assign it to a conditional to check to see if the person is 65 years or older.

Finally, console log the isChild and isSenior values to see if the person is a child or senior.
The variables should return a value of type Boolean!

**Sneak Peak Step**

Yay! Now I can check to see if my theme-park-goer is a child or senior. But could we set up a ticket price
now and discount them if the person is a child or senior?

I think the following prices seem reasonable:
<ul>
<li>Regular: $150
<li> Child: $75
<li> Senior: $125
</ul>

Given the variables we created above, how could we do this?
(We need to use if statements, which we haven't learned yet!)

It looks something like this..
```
if(boolean) {
  //code if boolean is true
} else if(boolean) {
  //code if this boolean is true
} else {
  //code
}
```

Let's make a variable called ticketPrice and set it initially to 0.

Then given our boolean data variables, could we set ticketPrice to the appropriate price?

Finally, console log ticketPrice to check if our code's working.
