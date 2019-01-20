# WHATS THIS? NANI???????

The "this" keyword is one of the biggest concepts when it comes to Javascript objects.

They are essential when creating object constructor functions (which we will go over later!)

For now, know that the "this" keyword references a specific instance of an object.

For instance:
```
var john = {
  firstName: "John",
  lastName: "Lee",
  getFullName: function() {
    return this.firstName + " " + this.lastName
  }
}
```

In the example above, I created a simple method inside my 'john' object that grabs other properties (firstName and lastName) from within the object itself. The "this" keyword refers to the 'john' object in this case!


### Wrap Up Exercises
1. Create 3 movie objects with the following properties: title, year, and rating.

2. Create a function getMovie that takes in an object as a parameter and returns the movie's title and year in a string sentence. (No using this!)
```
getMovie(movie) // => "Frozen is a movie that came out in 2016!""
```

3. Now create a method function getMovieRating in one of the objects that returns that object's rating in a string sentence. (remember to use the "this" keyword!)
```
movie.getMovieRating() // => "This movie has a rating of 5!"
```
