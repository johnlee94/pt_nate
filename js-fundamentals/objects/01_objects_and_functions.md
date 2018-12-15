# Utilizing Objects in FUNctions! O_O


Suppose we have 2 book objects as below:

```
let book1 = {
  title: '1984',
  author: 'George Orwell',
  pageCount: 326
}

let book2 = {
  title: 'A Peoples History',
  author: 'Howard Zinn',
  pageCount: 723
}
```
Could we make a function that can return a summary of our book properties?

```
function getSummary(book) {
  console.log(`${book.title} by ${book.author}`)
}


getSummary(book1)
getSummary(book2)
```

Awesome!

<hr>

In the past, when we created functions, they always had a return type of a single value such as a string or number. What if in a function we wanted to return multiple values?... Could we instead return an object that would hold these multiple values? YES!!

Suppose we wanted to return a summary AND the pagecount of our book object in a function.
```
function getSummaries(book) {
  return {
    summary: `${book.title} by ${book.author}`,
    pageCountSummary: `${book.title} is ${book.pageCount} pages long`
  }
}
```

So since our function is now returning an object, we can simply use a variable to hold that object and access different parts of it as necessary:
```
let book1summaries = getSummaries(book1)
let book2summaries = getSummaries(book2)

console.log(book1summaries.summary)
console.log(book2summaries.pageCountSummary)
```


### Section Wrap-up Exercises

Remember when we created a Fahrenheit to Kelvin converter function, and then a Fahrenheit to Celsius converter function?

Your task here is to do something very similar, but this time, instead of creating two separate functions, you are going to be creating a single function that returns an object containing three properties: the original Fahrenheit, the converted Celsius value, and the converted Kelvin value.

For Instance, if I plug in 32 degrees into the function, I should get an object as follows:
```
fahrenheitConverter(32)

// => { fahrenheit: 32, kelvin: 273.15, celsius: 0 }
```
