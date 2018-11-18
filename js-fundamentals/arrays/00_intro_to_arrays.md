# Javascript Arrays!!!~!~

YEAH YEAH!! Arrays are perhaps the most commonly used object in the Javascript language
(more on what objects are later).

They look something like this:
```
grocery_list = ['eggs', 'milk', 'flour', 'rice']
```

Arrays are a built in object prototype in Javascript (more on what that actually means later),
but simply put, they come with the language!

They can hold pretty much any JS primitive datatype or other objects (like another array!)
```
myArray = [12, 'something', true, null, ['another array!', 'wow']]
```

Arrays, much like a JS datatype we have already studied, are sequentially significant and
are indexed.

Which datatype am I referring to? That's right. Strings!

Remember if I had something like this...
```
let string = "Hello"

console.log(string[0]) //=> "H"
```
In strings, each character had an INDEX or position that made up the string (starting from index 0).

Arrays work much in the same way...
```
grocery_list = ['eggs', 'milk', 'flour', 'rice']

console.log(grocery_list[0]) //=> 'eggs'
```

You can think of arrays as being like a list in Javascript. Their purpose often is to hold data in some sequential order, with each element (we call the things that go into an array an element) being retrievable by
its index.

How would I grab 'rice' from my grocery_list array above?

```
grocery_list[3]
```
This would work because 'rice' is at the 3rd index in our array (remember that even though
rice is the 4th element in our array, arrays begin at 0 index).

Now, what happens if I do:
```
console.log(grocery_list.length)
```

It returned 4! The .length is a built-in array property that we can access with any array to return how many elements are in the array.

We can also grab 'rice' from grocery_list by indexing "backwards" using the length property.
```
console.log(grocery_list[grocery_list.length - 1])
```
Since grocery_list.length - 1 is 3, the above code is the same as grocery_list[3].

If we have a superrrrr loooong list, this method is useful for grabbing the last elements in an array.

<hr>

### Section wrap-up exercises.

1. Make an array called hobbies with 5 of your favorite things to do. Then console log your hobbies array.

2. Console log the 2nd element in your array.

3. Check to see that your hobbies array does indeed have 5 elements by console logging the length or your array.

4. Console log the 4th element in your array by using the array length property. 
