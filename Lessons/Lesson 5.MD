Lesson 5 - Functions

In programming, a function is a collection of code grouped together that will only be executed (run) when you specifically want it to be.

Let's start with an example program using a turtle, go ahead and place one down if you don't have one already. Ensure it has been refuelled.

Create a new file for the turtle called dance

Write the following code in the file:

```
function turnAround()
  turtle.turnRight()
  turtle.turnRight()
end

while true do
  turtle.forward()
  turnAround()
end
```

The code above uses a while loop which will run forever (we already know true is always true)
In the while loop the code will move the turtle forward one and then run (or call) the function which will run the code inside the turnAround function then it will jump back into the while loop and carry on.

Save the file and run it. Remember you will need to hold Ctrl T to terminate the program.


Copying files
Disk drives

Sending messages between computers with wireless modems

Functions
Make a castle
