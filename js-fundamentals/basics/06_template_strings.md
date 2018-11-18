# Template Strings

Remember how we create the String datatype in JS?

Yep! We use the single or double quotation marks as follows:

```
let name = "Nate"
```

If I wanted to make a sentence using my name variable...

We learned about string concatenation, or simply combining two strings together.

```
let name = "Nate"
console.log("Hey my name is " + name + "!") // => Hey my name is Nate!
```

While using the + operator to concatenate strings is totally valid, it can be a bit
annoying to use sometimes, especially when you have to be mindful of remembering to put
spaces or punctuation marks in your string.

There is a more commonly used JS method that was introduced in later version of JS called
string templating. It looks something like this:

```
let name = "Nate"
console.log(`Hey my name is ${name}!`)
```
Up above, we use backticks(it is located on the same key as the tilda symbol ~) which indicates
to JS that we are trying to use template string formatting.

We can then insert variables using the $ symbol and putting the variable within {}.

Another example:
```
let animal = "fox"
let human = "Austin"
let place = "forest"

console.log(`The ${animal} and ${human} had their first lovely meeting in the ${place}`)
// => The fox and Austin had their first lovely meeting in the forest.
```

Template stringing is often preferred to be used over concatenation because it is both easier
to make and read!
