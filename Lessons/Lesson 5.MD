Lesson 5 - Functions

In programming, a function is a collection of code grouped together that will only be executed (run) when you specifically want it to be.

Let's start with an example program using a turtle, go ahead and place one down if you don't have one already. Ensure it has been refuelled.

Create a new file for the turtle called **```dance```**

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

Now let's write another program that is a little more robust, for instance, the turtle will be able to deal with situations such as obstacles and if it runs out of fuel. This program will utilise what we have learned so far using while and for loops as well as conditionals and functions.

Create a new file called **```forward```** and write the following code in the file:

```
function refuel()
  turtle.select(1)
  turtle.refuel(1)
end

function digForward()
  while turtle.detect() do
    turtle.dig()
  end
end

function moveForward()
  if turtle.getFuelLevel() < 10 then
    refuel()
  end
  
  while turtle.forward() == false do
    digForward()
    turtle.attack()
  end
end

while true do
  moveForward()
end
```

Save the file. Before you run it, let's take a look at what is going on here.

The code above uses a while loop which will run forever (we already know true is always true)
In the while loop the code will move the turtle forward one and then run (or call) the function which will run the code inside the turnAround function then it will jump back into the while loop and carry on.

Save the file and run it. Remember you will need to hold Ctrl T to terminate the program.


Copying files
Disk drives

Sending messages between computers with wireless modems

Functions
Make a castle
