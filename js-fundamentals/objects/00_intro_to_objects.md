# Objects whooohooooo!!!~~

Objects are used in JS when creating an entity that has multiple properties to
hold several pieces of data.

For example, think of a book. It has a title, author, pages, genre, etc..., or
several properties that make up the book.

In Javascript, it can be modeled such as this:
```
let myBook = {
  title: "Harry Potter and the Chamber of Secrets",
  author: "J.K. Rowling",
  pageCount: 699,
  genre: "Fantasy Fiction"
}
```

Notice the syntax used for creating an object. Up above, we simply have a variable declaration
which we have seen several times, but paying special close attention to the object notation...

We have the curly braces that create the object, followed by several properties, with each property
associated with a value by the colon (:) and separated by commas. Also note that up above, we have property values that are of String and Number data value type.

In fact, we could have a property value be pretty much ANY datatype -- it can even be an array or another object!

To grab just one property off of my object, we use *dot notation*.

```
console.log(myBook.title)

console.log(myBook.author)
```

We often call our property/value pairs as *key value pairs*. With the property being the "key". Think of how keys work in the real world. Each key is unique and opens up one specific door exactly. Much the same way in an object, when you call an object's property or key, it returns back the one specific value that "key" is associated with.

To change an object's property value, we simply can...
```
console.log(myBook.pageCount)

myBook.pageCount = 1001

console.log(myBook.pageCount)
```

### Section Wrap-up Exercise

1. Create an object person, with 3 properties: name, age, and hobby.

2. Console log a string template mirroring this example: "John is 15 years old and likes to play tennis"

3. Change the person's hobby to something MORE fun!

4. Console log the string template again to see that the hobby property was indeed changed.
