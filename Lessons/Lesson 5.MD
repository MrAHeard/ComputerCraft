##Lesson 5 - Functions

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
<a href="Dance"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%205%20Images/dance.png" align="left" height="200" width="350" ></a><br><br><br><br><br><br><br><br>

The while loop will run forever (true is always true remember) and move the turtle forward, it will then run (or call) the function turnAround which will run the code inside the turnAround function then it will jump back into the while loop and carry on.

Save the file and run it. Remember you will need to hold Ctrl T to terminate the program.

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
In the while loop the code will call the moveForward function which will try and move forward if it can, if it can't then it will digForward if there is an obstacle, it will also attack if a mob is the obstacle. Within this function, if the fuel Level of the turtle is less than 10, it will call the refuel function which will use one item from slot one as fuel and then carry on. 

Can you work out at what point the turtle will actually stop?

The functions in the program above would be extremely useful in a variety of programs that you may want to write to get a turtle to do something autonomously. 

Now modify the program as follows:

Add a new function at the top of the forward program as shown below:

```
function needsFuel()
  if turtle.getFuelLevel() < 10 then
    return true
  else
    return false
  end
end
```

Also change the code in the if statement in the moveForward function to the following:

```
function moveForward()
  if needsFuel() then
    refuel()
  end
``` 
You must keep the rest of this function the same.

So what have we done? We are now passing a value between functions and in the process we have made the program easier to understand. Now, if the turtle needs fuel it will refuel. It does this by passing a true or false value from the needsFuel function so **```if needsFuel()```** then becomes **```if true then```**

Can you now write your own program that creates a tower exactly 10 blocks high using what you have learned so far?

Now move on to [lesson 6](https://github.com/AllenHeard/ComputerCraft/blob/master/Lessons/Lesson%206.MD)
