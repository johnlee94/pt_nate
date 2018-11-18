# Loooooping over Arrays..

Often with JS arrays, we will want to "loop" or "iterate" over the array.

This simply means we want to start at the beginning of our array, and go through each element
and do something with the element, until the end of our array.

In code, it looks like this:
```
let todos = ['clean the house', 'walk the dog', 'do math homework', 'make dinner']

todos.forEach(function(todo) {
  console.log(`I need to ${todo}`)
  })
```

The forEach is another method Javascript programmers commonly use to loop through an array.

So what's happening exactly?

We call the forEach() method on our todos array, and pass it in a function. Within each function that is passed, we pass in our "todo" (which is an element in our todos array) as an argument, and then console log it out.

In other words, for each element in our todos array, we are console logging out 'I need to ' + the todo element that we are looping over in that instance.

To go over it step by step, initially the "todo" that is passed into our function is the 0th index element in our array ("clean the house"), and so we console log "I need to clean the house". Then, we go the next element in our array ("walk the dog"), which is passed as our new "todo" argument, and "I need to walk the dog" is consoled out. Then we go to our next element "do math homework" which is passed in as our new "todo" argument... and so on!

CONFUSED?? It might be hard to wrap our heads around the forEach method at first, but with practice you will be looping over arrays like a pro!!

<hr>

### Section Wrap-Up exercises

1. Create an array of todos with 5 string elements.

2. Use the forEach method to iterate over the array, and for each string element in the array
console log ("I have finished" + the element).

<hr>

You are given this array:
```
let movies = [["Spiderman", 4], ["Frozen", 5], ["Hitman", 2], ["Saving Private Ryan", 3], ["Moana", 4], ["Captain America", 1], ["The Avengers", 2]]
```
movies is an array of individual arrays that each contain the title of a movie at index 0 and the rating of the movie at index 1.

Your task is to loop through the movies array and console log ("I want to watch" + the movie) IF the rating of that movie is 3 or higher!
