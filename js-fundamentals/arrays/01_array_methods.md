# Common Array Methods~~

In this MD, we will go over some very common methods used with arrays.

How can we add or remove items in an array?

```
let games = ['League of Legends', 'Fortnite', 'PubG']

console.log(games)

games.push('Overwatch')

console.log(games)

console.log(games.pop())

console.log(games)
```

The .push() method adds an element to the end of an array, while the .pop() method
removes the last element in the array. Note that the push() method requires an argument that will be "pushed" or added to the end of the array.

Also note that the pop() method "pops" off or removes the last element, and while it does not take an argument, it returns the element that was removed. That is why when we console.log(games.pop()) above, it returned 'Overwatch', which was the element that was "popped" off.

<hr>

Similarly, if we wanted to add elements to the beginning of our array...
```
let classes = ['Algebra', 'English', 'Dance', 'P.E.', 'History']

// I HATE ALGEBRA SO LET's GET RID OF IT!

console.log(classes.shift())

console.log(classes)

// Let's add a music class to our array!

classes.unshift('Choir')

console.log(classes)
```

Much like the push() and pop() methods, the shift and unshift() behave much the same way.
The shift() method removes the 0th index element in an array, and RETURNS the element that was
reomved (So our console.log(classes.shift()) outputted 'Algebra' which was removed in our classes array).

The unshift() method takes an argument and adds it to the the beginning of an array.

<hr>

We can also directly manipulate elements in our array using square bracket notation.

```
let arr = [1, "hello", [2, "something"], "dogs"]

console.log(arr)

arr[0] = 3

console.log(arr)
```

<hr>

##### The splice() method

There are a TON of array methods out there! (In addition to push, pop, shift, unshift that we have just studied)

One array method that helps us manipulate elements in the middle of our array is the splice method.

It takes in 3 arguments...
splice(starting index, number of items to be removed, item to be added)

```
let animals = ['dog', 'cat', 'fish', 'turtle', 'fox']

animals.splice(2, 1) //=> This will remove 'fish' because it is at index 2, and we want to remove 1 item

let animals2 = ['monkey', 'zebra', 'shark', 'eagle']

animals.splice(1, 2, 'whale') //=> This will remove 'zebra' and 'shark', then add 'whale' at the 1st index.
```

<hr>

### Section Wrap-up exercises

Help me organize my shopping list!!
```
let shopping_list = ['shoes', 'sunglasses', ['eggs', 'milk', 'flour'], 'paper', 'pens']
```

1. Console log my groceries (the array of 'eggs', 'milk', 'flour')

2. Actually mom called and says we DO have eggs at home, so I don't have to buy them.
But, we are out of rice! Replace the 'eggs' element with 'rice' in my shopping_list array.
Console log my new array.

3. I need to buy shirts, and I want to buy them first! Add shirts to the very beginning of my array.
Console log my new array.

4. I no longer need pens. Remove 'pens' from my shopping_list array and then console log my array.

5. Mom called again. We also need Kimchi from the grocery store! Add 'Kimchi' to the end of my
['rice', 'milk', 'flour'] array. Then console log the entire array.

6. Sunglasses are too expensive! Replace 'sunglasses' with 'hat'. Console log my shopping_list array.
