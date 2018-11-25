# Tic Tac Toe Guidelines

1. Write a function that can print out a board. Set up your board as an array, where each index 1-9 corresponds with a number on a number pad, so you get a 3 by 3 board representation.

TEST that your function works, with a test version of a board. As follows:
```
testBoard = ['#','X','O','X','O','X','O','X','O','X']
displayBoard(testBoard)
```

2. Write a function that can take in a player input and assign their marker as 'X' or 'O'. Think about using *while* loops to continually ask until you get a correct answer.

TEST the function so it returns the desired output...

3. Write a function that takes in the board list object, a marker ('X' or 'O'), and a desired position (number 1-9) and assigns it to the board.

i.e.
```
placeMarker(testBoard, '$', 8)
//=> should set board at position 8 to be $
```

4. Write a function that takes in a board and checks to see if the person has won.

TEST to see it's working.
i.e.
```
winCheck(testBoard)
// => true or false
```

5. Write a function that uses the random module to randomly decide which player goes first.
HINT: Use the Javascript Math object, with the random() and round() methods to return randomly an integer value of 0 or 1!

6. Write a function that returns a boolean indicating whether a space on the board is freely available.

7. Write a function that checks if the board is full and returns a boolean value. True if full, False otherwise.

8. Write a function that asks for a player's next position (as a number 1-9) and then uses the function from step 6 to check if its a free position. If it is, then return the position for later use.

9. PUTTING IT ALL TOGETHER: Here comes the hard part! Use while loops and the functions you've made to run the game!

**BONUS**: Allow the game to be replayed.
