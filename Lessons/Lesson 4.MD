##Lesson 4

During this lesson we are going to look at loops. When programming, a loop is a piece of code that you can choose to run while a certain condition remains or you can run a loop for as many times as you wish before breaking out and doing something else. Firstly, let's look at a while loop.

A while loop takes the form of **```while boolean do code end```** so an example would be **```while true do turtle.turnRight() end```** If you type this code into the lua environment of the turtle it would run forever as true is always true. To terminate the program, right click the turlte and click ctrl t.

You can also put more than one instruction in the command so as well as turning right you could get the turtle turning left. **```while true do turtle.turnRight() turtle.turnRight() end```**

In previous lessons you learned how to refuel a turtle and select a slot to use for this as well as placing blocks. During this lesson we will refuel a turtle and use a loop to build a structure. Find a suitable place in your world to make a bridge and place a turtle down.

First, ensure you have some fuel of some kind in slot 1 of your turtle and use some of the fuel using the right command. Then add some cobblestone to slot 2. Right click on the turtle. We will now write a program that does two things:

- Checks if there are items in slot 2

- Checks if the turtle is out of fuel

Create a new file called Bridge (**```edit Bridge```**)

```
turtle.select(2)

while turtle.getItemCount ~= 0 and turtle.getFuelLevel() ~= 0 do 
```

The first line of code above selects the turtle's second slot. The while loop checks there are items in slot 2 (item count not equal to 0, ~= 0 ) and it also checks that the turtle has got fuel (fuel level not equal to 0,  ~= 0). While those condiotns are both true, the code inside the loop will repeatedly run, this code is as follows:

```
  turtle.placeDown()
  turtle.forward()
end
```
You must indent (move inwards) the code as above, whatever is indented will be the run in the loop.

<a href="Bridge"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%204%20Images/Bridge.png" align="left" height="180" width="300" ></a><br><br><br><br><br><br><br>

Save the program but before you run it, check your turtle is facing the right way, if not you can run the built in program **```turn right```** or **```turn left```** to get it pointing the right way. Now run your program, your turtle should now repeatedly place a block beneath it and move forward producing a bridge.

<a href="Bridge building"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%204%20Images/Bridge2.png" align="left" height="360" width="600" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br><br>

If the turtle was to run out of items in slot 1 or the turtle was to run out of fuel, the while condition would be broken and the program would stop. That is how while loops work. If the turtle was to run into an obstacle before these conditions became true, the turtle would just stop.

We will now look at for loops.

For loops work a little bit differently as they don't work on boolean conditions. 

Let's start with an example, create a new file called count and type the following:
```
for num = 3, 10 do
  print (num)
end
```
<a href="For loop"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%204%20Images/for.png" align="left" height="180" width="300" ></a><br><br><br><br><br><br><br>

In this loop we still have a do and an end, we also have some code in the middle that will be repeatedly run.

The code **```for num = 3, 10 do```** creates a variable called num and sets it to the value 3. It then runs the **```print (num)```** so it will print 3. 

The code then adds one to num and runs the code inside the loop again, this time printing 4. The code will continue to repeat in this manner until num = 10 as in the first line of code.

Try it!

<a href="Count"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%204%20Images/count.png" align="left" height="180" width="300" ></a><br><br><br><br><br><br><br>

A for loop is a great way to run some code a set amount of times, so long as you know how many times you want to run it.

Let's write another program, create a new file called itemCount you also need to make sure you have some items in some of the slots so we can test our program is working.

```
total = 0 

for slot 1, 16 do
  total = total + turtle.getItemCount(slot)
end

print ("I have " .. total .. " items")
```
<a href="itemCount"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%204%20Images/itemCount.png" align="left" height="180" width="300" ></a><br><br><br><br><br><br><br>

When you run your program it will count the items in slot 1, then slot two, all the way to slot 16. All the time adding them together and updating the value of total along the way.

<a href="itemCountRun"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%204%20Images/itemCountRun.png" align="left" height="300" width="350" ></a><br><br><br><br><br><br><br><br><br><br><br><br>

You can chek this worked by adding up the items in the slots.

In the next lesson we will look at 
Copying files
Disk drives

Sending messages between computers with wireless modems

Functions
Make a castle
