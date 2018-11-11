## Let's do some function practice!

1. Create a function called helloName, that takes in a str value as an argument
called Name, and then console logs "Hello, Name."

```
i.e. helloName("John") // => "Hello, John"
```

2. Define a function maxOfTwoNumbers that takes two numbers as arguments and
returns the largest of them. If they are the same, return that number.
Use the if-then-else construct.

```
i.e. maxOfTwoNumbers(5, 6) // => 6
     maxOfTwoNumbers(5, 5) // => 5
```

3. Define a function, as a function expression, maxOfThree that takes three numbers
as arguments and returns the largest of them.

4. Define a function isCharAVowel that takes a character as an argument and returns true if it is a vowel, false otherwise.

```
i.e. isCharAVowel("a") //=> true
     isCharAVowel("b") //=> false
```

5. Define a function fullName that takes two string arguments(firstName and lastName), and returns the full name.
```
i.e. fullName("John", "Lee") //=> "John Lee"
```

6. Define a function called calculator that takes in three arguments: a number, another number, and a string. Depending on the string, argument perform the proper arithmetic operation on the two numbers. Valid string inputs are "add", "multiply", "subtract", "divide", and "power". If a non-valid string is passed, the function should return "I'm only a calculator!"
```
i.e. calculator(5, 5, "add") // => 10
     calculator(500, 500, "dance") // => "I'm only a calculator!"
```

7. Define a function called netIncomeGenerator that takes in one number argument representing gross income (So income before taxes), and returns the net income (income after taxes) as well as how much was paid in taxes in a string sentence. Note that tax percentages are dependent on the gross income as follows:
<ul>
<li>$0 - $24,999 : 10%</li>
<li>$25,000 - $49,999 : 18%</li>
<li>$50,000 - $99,999 : 25%</li>
<li>$100,000 - $199,999 : 30%</li>
<li>$200,000+ : 35%</li>
</ul>

```
i.e. netIncomeGenerator(250,000) // => "You paid 87500 in taxes this year. Your net income is 162500."
```

8. Define a function called pigLatin that takes in a string argument (a word) and converts it to pig latin! Note the rules for pig latin is that if the word starts with a vowel, simply add "ay" to the end of the word. If the word starts with a consonant, move the first letter of the word to the end, and then add "ay".

```
i.e. pigLatin("apple") // => "appleay"
     pigLatin("hello") // => "ellohay"
```

9. Define a function isEven that takes in a number argument, and returns true if it is even and false if it is odd.

```
isEven(2) // => true
isEven(3) // => false
```

10. Define a function isMultiple that takes in two number argumets, and checks to see if the second number is a multiple of the first number. It should return a boolean value.

```
isMultiple(5, 25) // => true
isMultiple(5, 26) // => false
```

11. Define a function caloriesBurned that takes in 3 number arguments (jogging, cycling, and weight training each in minutes) and returns the total calories burned. If an exercise is not done (an argument is not passed, default it to a value of 0)
<ul>
<li>Jogging: 20 per minute</li>
<li>Cycling: 10 per minute</li>
<li>Weight Training: 15 per minute</li>
</ul>

```
caloriesBurned(30, 20, 0) //=> 800
```

**CHALLENGE!!**

12. Define a function totalWages that takes in 3 arguments (wage per hour, total hours worked, and bonus) and returns total wages earned in a week. Note that for overtime hours, one receives 1.5x the normal wage (Overhours are any hours over 40 hours worked in a week). Also note that if a bonus is not received that week, it should default to 0!

```
totalWages(10, 50, 500) // => 1050
// 50 hours worked this week at $10/hr, with an overtime of 10 hours and a bonus of 500.
```
