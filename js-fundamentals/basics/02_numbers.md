# Numbers..!

Numbers are another basic Javascript data type.

They are exactly what they sound like.. They are numbers like 1, -50, or 50.05.

```
let myInteger = 5;
let myDecimal = 5.05;
```

Note that in JS, numbers encompass ALL numbers (integers, decimals, negatives, etc)

In other languages such as Python or Java, numbers are split into two different data types
Integers and Floats (Decimal Numbers).

---

### Basic Arithmetic Operations

We can perform many mathematical operations to our Javascript Numbers data type.

We have addition, subtraction, multiplication, division, and exponents...

Quickly in your console try some basic operations and see what you get!

```
//addition
5 + 5

//subtraction
25.5 - 10

//multiplcation
4*4

//division
25/5

//exponent
5**2
```

In addition, we have other Javascript operators such as the commonly used
"modulus" operator ( % ) to check the remainder of two numbers.

For instance:
```
5%2
```

This operation above returns 1 because 5 divided by two leaves a REMAINDER of 1.

We can do some cool things with the modulus operator, such as checking to see if a number is
even or odd.
```
//40 is an even number.
40%2
//This returns 0, because 2 goes into 40 evenly.

//53 is an odd number?
53%2
```

---
One quick note about the order of operations in Javascript...

Javascript math operations follow the PEMDAS rule and evaluate left to right.

In our console, what do you think we will get when we run:
```
40 + 5 * 2
```

What do you think we will get when we run:
```
(40 + 5) * 2
```
Remember, Please excuse my Dear Aunt Sally!

<br>
<br>

#### Quick Exercises!

1. **Dog Years**

We know that *unfortunately* dogs' lifespans are not as long as humans.

In fact, a basic way of converting a human's age to a dog's age is to add one
and then divide by seven.

Your task is to create a variable called age and set it equal to your current age.
Then, create another variable called dogYears that converts your age to dog years.

Finally, console log dogYears to see how old you would be if you were a doggy!

<br>

2. **Student Scores**

Create a variable that calculates the percent grade of a student's performance on an exam,
given the student's score and the max possible score.

You will create three variables (student's score, max score, and percent)

Finally, print the percent to the console. (Note that percentages should be whole numbers!)

<br>

3. **Create Fahrenheit/Celsius and Fahrenheit/Kelvin Converters**

Create a Fahrenheit to Kelvin (Celsius) Converter

Given a Fahrenheit value, convert it to Celsius.
Also, given a Fahrenheit value, convert it to Kelvin.

Finally, if we set Fahrenheit to a number, when we console log the celsius and kelvin converters,
we should get the correct converted numbers outputted.

i.e.
```
fahrenheit = 32
console.log(celsius) //-> 0
console.log(kelvin) //-> 273.15
```
