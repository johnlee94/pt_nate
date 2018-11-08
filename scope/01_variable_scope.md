# SCOPE!!!! ~~

Remember when we learned about variables? (YES!)

Scope is an idea in Javascript that dictate where variables "live" after they are
created.

```
let var1 = "Hello"

if (true) {
  console.log(var1)
}
```

In the code above, what do we expect to be consoled out?

The answer might have been pretty obvious based on what we've learned about Javascript
variables so far.

However, when variables are created, they cannot necessarily be accessed from anywhere
in the Javascript file!

Previously when we've created variables, they've always existed in the *global* scope.
Variables that are created in the global scope can be accessed anywhere.

Let's modify our code a little bit to introduce *local* scope.

```
let var1 = "Hello"

if (true) {
  console.log(var1)
  let var2 = "Bye"
}

console.log(var2)
```

OH NO! an error! What happened?

We created var2 within the scope of the if() {} code block. In other words, the variable
"lives" within this code block and can only be accessed within.

```
if (true) {
  let var2 = "Bye"
  console.log(var2)
}
```
