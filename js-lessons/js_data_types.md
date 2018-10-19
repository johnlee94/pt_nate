## Basic Javascript! Data types, variables, arrays, oh my!

### SWBAT
* List the five primitive javascript data types
* Create an array and access any item in that array
* Add and remove items from an array

#### A note about semicolons

Semicolons in JavaScript are required in some cases, optional in some cases, and not allowed in some places. If you choose to use semicolons where they are optional, be consistent! Make sure *not* to use semicolons where they are not allowed. [Here](https://www.codecademy.com/blog/78) is an article outlining where semicolons are required, optional, and not allowed.

## Types

A **type** in a programming language specifies a **kind of data**. While this might not be the most technical way to describe it, it's how we're most likely to think about it.

Javascript has five **primitive** types:

* String - characters or textual data... stuff like:  "abc" and "hello there 123"
* Number - just like it sounds... this is a number: 123 or 12.3
* Boolean - these are `true` or `false` values
* Null - has exactly one value which is `null`. This is used to signify an empty value.
* Undefined - usually this is a variable that hasn't been initialized: `var x;` will result in x being undefined at this point.


Those are primitive data types. What does that mean...that they live in caves? No, in the context of Javascript we can think of them as being baseline values.


Javascript also has the notion of:

* Object

Objects are complex types with many properties and methods attached or 'built in' to them. An object can be thought of as a logical containment unit for values and functionality that will manipulate or provide access to those values. Believe it or not, a function is a type of object. An array is also a type of object.


### What's the point of knowing these data types?

Because each data type has a whole bunch of built-in methods you can call on it.

Try this in your console:
```
"hello".length

3.length
```

Now try this:
```
"carrot" - "car"

6 - 3
```

lastly, try this:
```
3 + 5

"tea" + "pot"
```

Interesting... we can use the `+` operator on both the number type AND the string type. But it does something different for each of them.


## Variables
What's the point of having data types if there is nowhere we can temporarily store them?

This is where variables come in.

The special word (keyword) `var` indicates that this sentence is going to define a variable. It is followed by the name of the variable and, if we want to immediately give it a value, by an `=` operator and an expression. We don't have to assign a value right away.

This is not arithmetic, this is *assignment*.

So we can say
```
var x = 1
x = x + 9

console.log(x) => gives us what?
```

How do we name variables? Use common sense and camelCase.

We will come back to how variables are stored later...

### Array of hope!

![ray_of_hope](https://larspsyll.files.wordpress.com/2016/04/a_ray_of_hope_by_kaslito-d5yo5t0.jpg)

**What is an Array**

*    A container for data, similar to a list. You could think about it like a pill box.
*    An array is a data structure.
*    Each item in an array is called an element.
*    Arrays can hold all kinds of different data types: strings, integers, objects, functions, even other arrays!

What types of arrays did we see in the prework?

There are two ways to properly create an array; one that you all have seen before and one that is relatively rare, but I still want you to be able to understand it.

```
// rare syntax
var superheroes = new Array("Batman", "Superman", "Spiderman", "Captain America");

// what we're going to be using
var superheroes = ["Batman", "Superman", "Spiderman", "Captain America"];

```

The most important thing we're going to be using arrays for is to access the elements inside of them.

What would I need to type to access the element "Batman" in my `superheroes` array?   
`superheroes[0]` right?

How could I access "Spiderman"?

Think of it like years in your life. You start at zero and go from there.

### Independent Practice

What does each one do?

*    `Array.push()`
*    `Array.pop()`
*    `Array.shift()`
*    `Array.unshift()`
*    `Array.sort()`
*    `Array.reverse()`

<!--*    `Array.splice()`
*    `Array.slice()`
*    `Array.split()` *try this one with different arguments*
*    `Array.indexOf()`-->

Here are some resources for more information about arrays and methods you can use on them:

* [devdocs.io](http://devdocs.io/javascript-array/)
* [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)
* [W3 Schools](http://www.w3schools.com/jsref/jsref_obj_array.asp)

### Independent Practice Round Two!
Those six array methods that you just practiced are all very important, but they're not the only methods you will be using! Here's another round of very common and useful array methods that are beneficial to learn:

* `String.split()` *why did I include a string method in this list?* 🤔
* `Array.join()`
* `Array.splice()`
* `Array.slice()`
* `Array.indexOf()`

After you feel like you have a good understanding of those five methods, check out one of the resources above and see if you can find any other methods that you think will be useful that you can share with the class!

### Loops
**What is a loop**

So far we've seen two different loops in Javscript in the prework:

* `While`
* `For`

### While Loops

Let's start with a `while` loop and then move onto `for` loops later.

The two parts of a while loop:  

*  A condition that it checks
*  Something that it does

I want you all to walk me through creating a while loop that will `console.log` every number from 1-9


As an exercise I want you all to put this into practice

* Create an array of all the members of The Beatles!
* Loop through The Beatles, and console.log each one introducing himself. *Ex: "I'm Ringo Starr."*


#### For Loops
While loops are similar to For loops, but for loops are often the better choice because they take care of the assignment, the run condition and the incrementation/decrementation all in one step.

Why is it called a for loop?

	"The loop body is executed 'for' the given values of the loop variable"

```
for(assignment; run condition; increment/decrement){
    //LOOP ACTION HERE
}
```

* THE ASSIGNMENT sets a variable before the loop begins
* THE RUN CONDITION defines the condition for the loop to run
* INCREMENTS/DECREMENTS executes after each completed loop  

Let's loop through an array of people and `console.log` both the `index` and the `element`.

I want you all to pair up now and describe what is happening in this loop to each other.

Let's create another one but have it log in reverse.

We will have to subtract 1 from `Array.length` in our assignment.

What will our new end condition be?

What about our increment condition?

```js
  var numbers = [1,2,3,4,5,6,7,8,9,10,11,12,13,14];
```
* Create a loop that loops through this array from end to start but jumps by two each time.

* Create another loop that only prints out multiples of 3.

Why don't we revisit our Beatles while loop that we wrote a few minutes ago and convert it to a `for` loop!

**Avoiding Infinite Loops**

Loops operate based on conditional statements, running as long as the condition it is checking against is true. Take care not to write a condition that will always evaluate to true, otherwise you will create an infinite loop that will crash your browser (and maybe your whole computer!!!).

### White Boarding

*  * OPTIONAL * Shut your computers.  
![home_alone](https://media0.giphy.com/media/d2ZjBlsQa5dWO45a/200.gif)

Let's whiteboard examples of:

* String
* Number
* Boolean
* Array
* variable assignment

## Conclusion

* What are the five primitive JavaScript data types?
* What method can be used to remove the last item in an array?
* What method can be used to remove the first item in an array?
* What method can be used to add an item to the end of an array?
* What method can be used to add an item to the beginning of an array?
