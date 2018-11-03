# Strings and Variables!


### Variables

Variables are used to store a value to a variable name.

In Javascript, we have special words such as *var, const, and let!*

In JS, we use the single equals sign "=" to *assign* a value to a variable.

This is called **variable assignment**!!

```
var name = "Austin"

let favorite_animal = "mouse"

const DOB = "July 9, 1994"
```

What happens when we:

```
console.log(name)
```

<br>

Variable names should be something that makes sense to its corresponding value.

For instance, we might have a variable that stores the a grocery shopping list.

```
grocery_list = ["eggs", "milk", "rice", "kimchi", "bread"]
```

The value of the variable grocery_list is an array. We will go over what an array is
later!

Variables must start with a letter, $, or _
Note that $ and _ are special characters in Javascript used to indicate to other programmers
who may be reading your code, that the variable is some special type. Other special characters
such as & are invalid in variable naming!

Variables also cannot have any spaces!

In fact, what happens if we try to do...
```
var first name = "Sam"

var 5m = 4

var let = "something?"
```

Returns errors! With Sam, Javascript thinks that the variable name is simply the word "first",
and that we are trying to reassign a variable "name" that already exists to another value "Sam"...

In general, if we have a variable name with multiple words, we use..
<ul>
<li>"Camel Case": myFirstName</li>
<li>"Snake Case": my_first_name</li>
</ul>

Variables cannot start with a number either! In the second code var 5m =4, Javascript has no idea
whether or not you are trying to assign 5 as a variable name or simply referring to the number 5 itself.

Lastly, in the final line of code above, because let is a specially reserved keyword already built
into Javascript, you cannot use it as a variable name. There are many special keywords in Javascript that you
as a coder will figure out as you code more and more.

<br>
Naturally, variables can be *reassigned* to a new value.

```
var favoriteColor = "red";

console.log(favoriteColor);

favoriteColor = "blue";

console.log(favoriteColor);
```

---
### Strings!

What are Strings?? Strings are one of Javascript's 5 primitive data types (Strings, Numbers, Booleans, Null, Undefined)

We have already been working with strings above!

Strings are a special data type in Javascript, denoted by the single or double quotation marks

```
let myString = "Hi Austin!"
```

That "Hi Austin!" is called a string.

Strings are usually used for characters, words, sentences, pargraphs, etc.
<br>
However, they don't have to be words. 'asfnknaskf' is a string, simply because it is
wrapped by single quotation marks.

Note that strings are *sequentially significant*, or that, a string really is a group of characters
(such as the English Alphabet) that are ordered in a special way.

For instance:
```
let fruit = "mango"
```

The order in which the characters "m, a, n, g, o" matters a lot!
If we had fruit = "gamno", the variable still has all the same alphabetical letters,
but means something entirely different to us.

In fact, strings are always **indexed**. Meaning that each character has a specific position
within the string.

What happens if we:
```
let alpabets = 'abcdefghijklmnopqrstuvwxyz'
console.log(alphabets[0])
console.log(alphabets[25])
console.log(alphabets[1000])
```
Just up above, we performed *string-indexing*, by grabbing a specific character
from our alphabets string.

*STRINGS ARE ZERO-INDEXED (MUCH LIKE MANY OTHER THINGS IN PROGRAMMING)*
This means that the first character always starts at position 0!!
That is why when we grabbed the 0th index of our variable alphabets, we got returned
the letter "a"

We can also *slice* a string to return a specific segment of a string.

For instance...
```
let fullName = "John Lee"
```

To simple grab my first name we can do...
```
let firstName = fullName.slice(0, 4)
console.log(firstName)
```

This is called **string slicing**. We grabbed a section of firstName by slicing the
string with the correct indexes.

Note that the syntax for slice is "my string".slice(startingIndex, endingIndex),
with the ending index NOT being included in the slice.

<br>

The final string method we will go over in this markdown is called *string concatenation*,
which is just a really fancy way of saying let's combine strings together.

We can do something like this...
```
var favoriteAction = "I like to ... " + "party"

console.log(favoriteAction)
```

There are TONS OF OTHER STRING METHODS out there! For now, we have gone over some of the
most basic ones...

<br>
<br>

## Section Wrap-up Exercises

1. In your console, create two variables to store your first name and your last name.
Then, create a third variable called fullName that has the value of your first AND last name
by using the two variables you've already created and String concatenation.

Then print out fullName to check your answer.

i.e.
```
fullName = "John Lee"
```

2. In your console, create two variables to store your current location (city and country).
Then print out a concatenated version of your entire location in the proper address format.

i.e.
```
"Dallas, Texas"
```

3. **Indexing**
```
var myBrokenString = "TherXe are randomY characterZs here!"
```
Your task is to console log the X, Y, and Z characters using 3 print statements and string indexing.

BONUS: Make a new variable called myFixedString and assign it the value of myBrokenString,
but without the random X, Y, and Z characters.

(Hint: You need to use a combination of string slicing and concatenation!)

```
console.log(myFixedString)
//should return "There are random characters here!"
```

4. **WHERE's WALDO?**

Your Task is to console log the string "Waldo" from each of the 3 given string variables
below using string slicing... Good luck!

```
let waldoIsHere = "Waldo is my name!"
let waldoWasHere = "On a sad evening, Waldo was captured and killed.."
let waldoWillBeHere = "Maybe in another lifetime, I will be able to meet Waldo."
```
