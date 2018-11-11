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

<hr>

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

We created var2 within the scope of the if() code block (which encompasses everything
in the curly braces {}). In other words, the variable "lives" within this code block
and can only be accessed within.

```
if (true) {
  let var2 = "Bye"
  console.log(var2)
}
```

So we can access var2 from WITHIN the if() code block.

This means that var2 exists within the *local* scope and can be accessed only
locally from within the code block it was created.

Note that from within the if() code block, we were able to access var1. This is because
in a scope, you can access variables defined in that scope, or in any parent scope.
(This means that even if you are in a local scope, you would always be able to access
global scope!)

However, you can also have smaller children local scopes within another local scope...

```
if(true) {
  let var2 = 'var two'

  if(true) {
    let var3 = 'var three'
    console.log(var2)
    console.log(var3)
  }
  console.log(var2)
  console.log(var3)
}
```

In the code above, var3 is created within a nested if() block, and can only be accessed
from within that scope. That's why when we try to access var3 from the outer if() block,
we get an error that tells us var3 is not defined. However, notice that we are able to access
var2 from within the inner if() block, because a child scope has access to the parent scope!

WHEW!!! Confusing huh!!!?

<hr>

To review variable scoping, let's go over this code block and create a scope tree.

```
let varOne = 'varOne'

if(true) {
  let varTwo = 'varTwo'

  if(true) {
    let varFour = 'varFour'
  }
}

if(true) {
  let varThree = 'varThree'
}
```

In the code block above, I've made four variables, each instantiated in a different scope...

It can be outlined such as:
```
// GLOBAL SCOPE (A)
  //LOCAL SCOPE (B)
    //LOCAL SCOPE (C)
  //LOCAL SCOPE (D)
```

1. Match each variable to the proper scope.

2. Can we access varThree from Local Scope C? Local Scope A?

3. Can we access varTwo from Local Scope C? Why or why not?

4. Can we access varFour from Local Scope B? Why or why not?

5. From which scopes can we NOT access varOne?
