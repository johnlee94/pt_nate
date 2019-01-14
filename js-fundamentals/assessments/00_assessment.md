### Let's Review! :D

It's been a while since we had our tutoring sessions, and as I can imagine, it's probably been a while since you've done Javascript!

Let's go over the concepts we have learned thus far!

# General

1. What is Javascript primarily used for?

2. What are the 5 primitive data types in Javascript?

3. What is everything else (arrays, etc.) referred to as being?

4. What are the keywords used in Javascript to create variables?

5. Make a variable called myName and set it equal to the string value of your name.

6. Write the general syntax of creating a Javascript function that takes in 2 arguments.
Then call it.

7. What is the difference between null and undefined?

8. In your own words, describe "scope" as it is related to Javascript.


# STRINGS

Given
```
var str = "Hello World!"
```

1. Return the length of this string

2. Return the character "W"

3. Return the string "Hello World, :)", using the variable str.


Make a function that returns the number of characters in a given string.

```
myStringLength("How many?") // => 9
```

Make a function that returns how many times vowel characters appear in a given string.

```
howManyVowels("Hello") // => 2
```

Write a function that converts a given array of words into a sentence. Note the rules of creating a "proper" sentence (Capitalize first word, provide spaces between each word, and finally adding a period at the end)

```
makeSentence(["the", "dog", "walked", "down", "the", "street"]) // => "The dog walked down the street."
```

Write a functon that checks to see if a word is a palindrome. A palindrome is a word that is spelled the same forwards and backwards.
```
isPalindrome("racecar") // => true
isPalindrome("John") // => false
```

Write a function that checks to see if a new password is strong enough for a user. The password needs to be at least 10 characters long, have at least one uppercase character, have at least 1 number, and 1 special character from the following: !,@,#,$,%,^,&,* (These are the special cases for numbers 1-8). If the password passes, return "password registered!", else return "password is too weak."
```
checkPassword("Hello12Iamgr00t") // => "password is too weak." (No special character was included)
checkPassword("HelloIamgr00t!") // => "password registered!"
```

# NUMBERS
Calculate the following using Javascsript Math operators:
1. Add 5 and 7
2. Find the exponential value of 5 to the 3rd power.
3. Find the remainder value of 10 divided by 3.
4. Using the Math library (i.e. Math.power(5, 3)) to find the absolute value of 5 minuse 10.

Make a function that converts human years to "dog years". Note that humans live much longer than dogs. To convert a human's age to a dog's, you add one and divide by 7.

```
dogYears(6) // => 1
```
Make a function that takes in two parameters: an array of numbers, and the string value of either "even" or "odd". It then should return a new array of the given numbers, but only even or odd values.

```
evenOrOdd([1,2,3,4,5], "odd") // => [1, 3, 5]
```

Make a function that calculates how much money I am spending that month. An array of different expenses (numbers) will be passed to this function. A total sum of all the expenses should be returned.

```
allExpenses([500, 1000, 50, 25]) //=> 1575
```

Make a tip calculating function that calculates the total bill after including tip. It should take in two parameters, the bill and the tip percentage value.
```
calculateTip(100, 15) // => 115 (In this case, the bill before tip is $100, a tip percentage value of 15 was given, and so the total bill comes out to $115.)
```

Make a function that takes in two parameters an array of given numbers and a specific number, and returns a new array of numbers that contains only numbers that are greater than the given number.

```
greaterThan([500, 501, 502, 450, 700, 300], 500) // => [501, 502, 700]
```

Make a function that takes in two parameters: an array of numbers and a string value of either "ascending" or "descending", that returns an array of the given numbers, but in sequential order.

```
sortNumbers([4,2,7,6], "ascending") //=> [2,4,6,7]
sortNumbers([4,2,7,6], "descending") //=> [7,6,4,2]
```

Make a function that takes in two parameters, an array of numbers and a specific number, and returns the number in the array that is closest to the given number.

```
nearestNumber([5, 6, 7, 8], 9) // => 8
```

# CONTROL FLOW
1. Write the basic syntax skeleton for an "if", "else if", "else" statement.
2. What type of data structure is commonly used when working with if statements?

Make a function that returns the proper movie ticket price and takes in a string parameter of one of the following choices: "Child", "Senior", "Regular", "Student", "Veteran". The function should return the appropriate price as follows: child - $5, senior - $10, regular - $15, student - $12, and veteran - $10.

```
movieTicketPrice("veteran") // => 10
```

Make a function that takes in two parameters: an array and a number. If the number of elements in the array is less than the given number, return true. Else return false.

```
greaterLengthOfArray([1, "hello", 5, [4, 5], 7], 10) //=> true
```



# ARRAYS
Given this array:
```
arr = ["hello", 5, ["another nested array", 10], 15]
```

1. Grab "another nested array".
2. Add an element value of "hi" to the end of arr.
3. Change the element value of arr at the 1st index to be "bye".
4. Remove the last element from the array.

Write a function that takes in 3 parameters: an array, an element value, and a number; that takes the element value and adds it to the given array parameter as many times as the number value.

```
addTimes([1, 2, 3], "hello", 3) // => [1, 2, 3, "hello", "hello", "hello"]
```

Make a function that takes in an array of any given numbers, and returns a new array of the given numbers, but that contains only unique values.

```
uniqueNumbers([1,1,3,4,5,5,6,7,8]) // => [1,3,4,5,6,7,8]
```

# LOOPS

1. Write the basic syntax skeleton of a "for" statement.
2. Write the basic syntax skeleton for a "while" statement.

Make a function called fizzbuzz that takes in a number argument, and outputs the proper return value at every given number starting at one up to that number. Note that if the number is divisible by 3, then the string "fizz" should be outputted. If the number is divisible by 5, then the string "buzz" should be outputted. However, if the number is divisible by both 3 and 5, "fizzbuzz" should be ouputted. For all other cases, the number should simply be ouputted.

```
fizzbuzz(15) // => 1 2 "fizz" 4 "buzz" 6 7 8 "fizz" 9 "buzz" 11 "fizz" 13 14 "fizzbuzz"
```

Make a function that counts the number of times a word appears in an array of string values.

```
howManyTimes(["hello", "my", "name", "is", "John", "hello", "hello"], "hello") // => 3
```
