# More on Variable Scopes

### Variable Shadowing

Given this variable scope tree:
```
//Global
  //Local
    //Local
  //Local

let name = 'Andrew'

if (true) {
  let name = 'Mike'

  if (true) {
    console.log(name)
  }
}

if (true) {
  console.log(name)
}
```

What will be console logged?

I thought we couldn't have two variables with the same name in Javascript!?!?

Well... you can have multiple variables with the same name if they are in different scopes!

The first thing that is consoled out is 'Mike' because the first console.log(name) retrieves
the most root variable name.

This is called variable shadowing in Javascript, because when the interpretor looks for
the variable name when we call it in our console log, it looks for the variable in the most
specific scope first. If it doesn't find it, it keeps going up 1 parent scope level up until
it finds the first variable name. In other words, in this example, even though there is a variable
name in the global scope, JS retrieves the variable name that exists in the local scope because
it is a more specific scope! WHEW!!

The second console.log(name) outputs 'Andrew' because in this case, the only name variable that
exists is in the top-most global scope!


```
//Global
  //Local
    //Local
  //Local

let name = 'Andrew'

if (true) {
  let name = 'Mike'

  if (true) {
    name = 'Jen'
    console.log(name)
  }
}

if (true) {
  console.log(name)
}
```

Which name variable is reassigned when we do name = 'Jen'?

If your guess was that the name variable holding 'Mike' changed to 'Jen', you would
be correct!

Again, when JS reassigns the variable value to 'Jen' here, it retrieves the most
specific variable to the scope of the console.log(name) statement.

<hr>

Furthermore, what happens if ...

```
//Global
  //Local
    //Local
  //Local


if (true) {
  if (true) {
    name = 'Jen'
    console.log(name)
  }
}

if (true) {
  console.log(name)
}
```

When the variable name has not been declared in the file, but we try to assign the value 'Jen'
to it, JS automatically creates a global variable and assigns it to the value 'Jen'.


Notice the subtle but important difference when:
```
//Global
  //Local
    //Local
  //Local


if (true) {
  if (true) {
    let name = 'Jen'
    console.log(name)
  }
}

if (true) {
  console.log(name)
}
```

Here, in the second console.log(name), JS returns an error saying that 'name' is undefined.
In THIS case, we create and assign the variable name to the value 'Jen' WITHIN a local scope.
Therefore, it does not exist in the global scope!!

<br>

Wowwwwwww... Are you confused yet?

Some last thoughts on variable scoping:

1. Even though we can have multiple variables with the same name in different scopes,
I would highly advise against doing this, as it is not necessary and can just lead to confusion
in your code! Up above we could easily assign variables such as name1, name2, ... etc if
we wanted to have multiple "name" variables within our file.

2. Secondly, although JS creates a global variable for us when we simply assign a value
to a variable that hasn't been instantiated yet (like in our name='Jen' example when we never
declared let name = 'something' previously). I would advise to NEVER DO THIS! It would be very
confusing for you and other programmers looking at your code. It is never necessary :)

In this markdown, I showed you some unique cases with variable scoping so that you aren't confused
as to what's happening if they ever come up -- I would recommend you don't actually code like this!
