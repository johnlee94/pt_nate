# Null and Undefined?

Null and Undefined are the final 2 primitive JS Data Types!


### Undefined

We already know we can assign values to variables..

```
let name = "Austin"

console.log(name)
```

But what would happen if we..

```
let name;

console.log(name)
```

We get undefined!

Both act as placeholder, or mark an absence of a value. If we don't have a value
to some kind of variable, JS just returns *undefined*.

In the case above, when we console log the value of *name*, JS understands that we had
already instantiated or created our variable name. We just didn't assign it a value yet.
JS often will default to *undefined* when "something is supposed to be there but it doesn't
exist quite yet".

A beginner coder might be confused as to how **undefined** and **null** are different from
"nothing". But in fact, these values do provide valuable insight. They act as
*placeholders*. In other words, they tell us that there is an absence of something.

What happens if we don't create a variable, and instead, try to console log a random
variable that doesn't exist.

```
console.log(something)
```

We get an error! In this case, a variable "something" has never been created. It doesn't exist.
In the name-variable case, the variable DOES exist. It just has a value of undefined!


<hr>

So how can we use undefined in our code? Well, we can directly used undefined to check
variables at certain points of our program.

Let's go back to our variable name example. Suppose we were developing a program that
keeps track of our users, or in other words, we need Javascript to know when specific users
are currently logged into our system.

```
let user;

// user = 'John'

if (user === undefined) {
  console.log('Please log in')
} else {
  console.log(`Hello ${user}`)
}
```

<br>
<hr>

When working with function, if a predefined argument isn't passed, or a function doesn't
have a return value, JS will default, again, to undefined.

For instance:
```
function square(num) {
  console.log(num * num)
}

console.log(square())
```

In this case, when we call our function square(), Javascript expects us to pass in something
to our *num* parameter. Since up above square() is called without an argument, JS will default to passing in
*undefined* as our num parameter. Then, the function runs, and since you cannot perform math operations
on the data type of undefined, we get NaN or "Not a Number."

Again, in Javascript, functions always have a return type value (or that simply functions always return some value after they finish executing). If none is provided, it simply returns undefined.
```
function square(num) {
  console.log(num * num)
}

let result = square(5)
```

When we do provide a return statement, however...
```
function square(num) {
  return num * num
}

let result = square(5)
console.log(result)
```

<hr>

Often times when programming in JS, we will often get undefined in places of our code
which we may not have wanted. For example, if we forget to assign a variable after instantiating it.
Undefined is a great tool to also help us **debug** our code! In other words, when we see
undefined as our output when we expected some other value, we should pause and think what's happening
so we can figure out where in our code certain values are lost.


 ### Null

Null is also a placeholder type value and represents the absence of something. The
key difference is that type null is explicitly set by the programmer.

Let's go back to our user example: What if we wanted to create some kind of logging out
functionality?

Below I have attempted two functions "login" and "logout" that simply assigns a value to our user,
or assigns undefined to our user.
 ```
 let user;

 console.log(user)

 function login(user) {
   user = user;
 }

 function logout(user) {
   user = undefined;
 }
 ```
Initially when we create our user variable and console log it, since we hadn't yet assigned
a value to our user variable, we get undefined. This is something Javascript as a language
defaults to doing like we previously mentioned.

In our logout(user) function, we reassign user to be undefined so that our program knows that,
once again, our user doesn't have a real value. But how can we know that we specifically assigned
user to be undefined through our code, or if the Javascript interpretor did it? We can't!

That's where our null data type comes in handy.

```
let user;

console.log(user)

function login(user) {
  user = user;
}

function logout(user) {
  user = null;
}
```

In our logout function, if we simply assign user to value of null, we can know that we purposely
assigned user the value of null which also indicates that our variable is missing a value.

In other words, we know that whoever wrote this Javascript file explicitly wants our user variable
to be **null** when the logout function is run!
