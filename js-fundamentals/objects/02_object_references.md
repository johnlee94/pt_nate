# More on Objects

In Javascript, anything that isn't a primitive datatype is an object! That means things like arrays are objects too! Therefore, programmer utilize objects all the time in Javascript.

One very common thing to do is to create functions that manipulate objects in our program.

Suppose we had a simple 'account' object that kept track of a person's expenses and income.
```
let myAccount = {
  name: "John Lee",
  expenses: 0,
  income: 0
}
```

Can we manipulate this object using a function, say to add to my expenses property?
```
function addExpense(account, expense) {
  account.expenses += expense
  console.log(account)
}

addExpense(myAccount, 2.50);
console.log(myAccount)
```

Up above we create a function addExpense that takes in two arguments, the account object and an expense (a number), and then simply adds that given expense argument to the account's expenses property.

It also, console logs out the account after the operation.

Is the original myAccount object modified? We can check by console logging myAccount after the function is ran.

We see that the original object IS modified!!

What actually happens is that when we pass in the 'account' object into our function, we are actually passing a REFERENCE to the object in memory! In other words, we are able to manipulate the original object's properties by passing in a reference to that object in our function. WHEW!!

<br>

Now what if we did something like...

```
function addExpense(account, expense) {
  account = {}
  console.log(account)
}

addExpense(myAccount, 2.50);
console.log(myAccount)
```

Did you notice that the console.log(account) in the function returned the empty object ({}), but when we console logged myAccount, the myAccount object never changed? This is because, we are never allowed to simply overwrite an entire object that is being referenced. We can manipulate its properties, but we cannot simply turn the object into something like a string or number.

<hr>

Note that when you set a variable to equal a reference to an object in memory, when we manipulate this variable, we are also manipulating the original object!

In other words...
```
let animal = {
  species: 'dog',
  name: 'sammy'
}

let sammy = animal;

sammy.species = 'cat'

console.log(sammy)
console.log(animal)
```

Notice that when we console log out both sammy and animal at the end, we get back the SAME changed object. This is because when we do let sammy = animal, we AREN'T creating a new object with the same contents as our animal object. We are actually setting the variable sammy to EQUAL A REFERENCE TO THE ANIMAL object. Thereby changing sammy, we are also changing our animal object.

This may be confusing at first, but keep in mind how objects are stored in memory in Javascript. When an object is created in memory, it has a specific location in memory. Anytime we set a variable to equal this object in memory, we are actually setting the variable to equal a reference to that object. You can think of this reference to be like a pointer or signal- it simply 'points' to where that object is being stored. When we created another variable to equal that same object, it is also 'pointing' towards that object in memory.

You can, however, create an entirely new object in memory that looks like another object and then manipulate that new object if you wished to.

```
let animal = {
  species: 'dog',
  name: 'sammy'
}

let felix = {
  species: 'dog',
  name: 'sammy'
}

felix.species = 'cat'
felix.name = 'felix'

console.log(animal)
console.log(felix)
```
Notice the subtle yet important difference above: in this case, we are setting our felix variable to equal an entirely new object in memory, even though its contents initially are the same as our animal object. When we manipulate our felix object in this case, the original object isn't modified!!
