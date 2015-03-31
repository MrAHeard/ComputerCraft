##Lesson 4

During this lesson we are going to look at loops. When programming, a loop is a piece of code that you can choose to run while a certain condition remains or you can run a loop for as many times as you wish before breaking out and doing something else. Firstly, let's look at a while loop.

A while loop takes the form of **```while boolean do code end```** so an example would be **```while true do turtle.turnRight() end```** If you type this code into the lua environment of the turtle it would run forever as true is always true. To terminate the program, right click the turlte and click ctrl t.

You can also put more than one instruction in the command so as well as turning left you could get the turtle turnig right. **```while true do turtle.turnRight() turtle.turnRight() end```**

In previous lessons you learned how to refuel a turtle and select a slot to use for this as well as placing blocks. During this lesson we will refuel a turtle and use a loop to build a structure. Find a suitable place in your world to make a bridge and place a turtle down.

First, ensure you have some fuel of some kind in slot 1 of your turtle. Then add the maximum amount of cobblestone to slot 2. Right click on the turtle. We will now write a program that does two things:

- Checks if there are items in slot 2

- Checks if the turtle is out of fuel

Create a new file called Bridge (**```edit Bridge```**)

```
turtle.select(2)

while turtle.getItemCount ~= 0 and turtle.getFuelLevel() ~= 0 do 
```

The first line of code above selects the turtle's second slot. The while loop checks there are items in slot 2 and it also checks that the turtle has got fuel. While those condiotns are both true, the code inside the loop will repeatedly run, this code is as follows:

```
  turtle.placeDown()
  turtle.forward()
end
```
You must indent (move inwards) the code as above, whatever is indented will be the run in the loop.

<a href="Bridge"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%204%20Images/Bridge.png" align="left" height="200" width="300" ></a><br><br><br><br><br><br><br><br><br>

Save the program and run it.




While and for loops
Bridge

Copying files
Disk drives

Sending messages between computers with wireless modems

Functions
Make a castle
