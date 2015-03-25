##Lesson 1
In computing, the command line is an important feature. It is an extremely powerful tool and if not used carefully you could do serious damage.

In ComputerCraft we are going to look at some common commands using the command line built in to the mining turtles.
To access the turtles command line, right click on a turtle.

<a href="Intro"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/Intro.png" align="left" height="260" width="300" ></a><br><br><br><br><br><br><br><br><br><br>

Here the command line understands certain dedicated commands designed for controlling the turtle, we can also access the lua command line by typing **```lua```**.

Firstly, type **```ls```** or **```dir```** to list the files and directories (folders) stored on the turtle.

To make a new directory, type **```mkdir```** followed by the name you would like your folder to have, for instance, type **```mkdir myfiles```**

<a href="cd"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/cd.png" align="left" height="260" width="300" ></a><br><br><br><br><br><br><br><br><br><br>

If you type ls you should now see two folders listed, one called rom which already existed, and one called myflies which you just made.

Now to go into this directory you type cd (change directory) followed by the directory name so, **```cd myfiles```**

<a href="myfiles"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/dir.png" align="left" height="260" width="300" ></a><br><br><br><br><br><br><br><br><br><br>

Now if you type **```ls```** or **```dir```** you can see the directory we made is empty.

To go back, just type **```cd ..```**

<a href="cd.."><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/cd...png" align="left" height="260" width="300" ></a><br><br><br><br><br><br><br><br><br><br>

Alternatively if we wanted to delete a directory we would type **```rm myfiles```** (rm - remove) we could also do this for files inside a folder

So now you know the basics of the turtle command line, let’s write our first program in lua.

Type **```lua```** at the command line

<a href="lua"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/lua.png" align="left" height="260" width="200" ></a><br><br><br><br><br><br><br><br><br><br>

You are now in the lua environment where you can run commands or write programs

To create a new file we need to type edit, followed by the name we would like to give to the file, so let’s go ahead and type **```edit refuel```** this will create a blank file that we can write a program in for running later on.

During these lessons well will be using the devices API (application programming interface - a collection of code that, rather than being run directly by the user as a program, is meant to be used by other programs) for use in ComputerCraft that can be found on the [wiki](http://www.computercraft.info/wiki/Main_Page), for this particular task we will be using specific turtle commands that can be found on the turtle API section [here](http://www.computercraft.info/wiki/Turtle_(API)).

We will be using some commands for checking the fuel level and we will write a program to do this automatically using a loop. First, let’s look at how to check the fuel level and supply the turtle with fuel. Fuel can be any normal fuel source in Minecraft such as wood or coal.

Now type **```turtle.getFuelLevel()```**

**```getFuelLevel()```** is a function and must be types exactly like above with a capital F and L, this is the usual convention for variable names or function names containing more than one word, it makes them easier to read and understand.

<a href="getFuel"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/getfuel.png" align="left" height="260" width="300" ></a><br><br><br><br><br><br><br><br><br><br>

Here we can see the instruction returns 0, this is because a new turtle does not have any fuel. The 4 x 4 grid on the bottom right of the screenshot above is the turtles inventory. Items can be placed here for use, mined items will also populate these slots as the turtle mines. The slots are numbered top left to right, top to bottom so the top row of slots are 1, 2, 3, 4 and so on down to 16.

If we want to use items, we need to run a command to select the correct slot number. In the screenshot below, some coal has been placed into slot 1.

To use this fuel we would need to tell the turtle to select slot number 1, we do this by typing **```turtle.select(1)```** the one indicates the slot we wish to select, we could put any whole number from 1 to 16 in here and it would be selected.

<a href="selectCell"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/select.png" align="left" height="260" width="300" ></a><br><br><br><br><br><br><br><br><br><br>

Now the slot containing coal is selected we can go ahead and refuel the turtle. Type **```turtle.refuel(1)```**

Next, check the fuel level of the turtle again, you should see that the turtle now has a fuel level of 80, so for one lump of coal we can perform 80 single operations. You will notice that the coal item in slot 1 has reduced by one. We could have typed **```turtle.refuel(10)```** to give the turtle ten lumps of coal resulting in a fuel level of 800.

<a href="refuel"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/refuel.png" align="left" height="260" width="300" ></a><br><br><br><br><br><br><br><br><br><br>

We can now use this fuel to mine, place or move. For instance I could type **```turtle.forward()```** and the turtle would move forward one block space. In doing so, the fuel level of the turtle is reduced by one. Notice when we move forward successfully, true is printed to the screen. We will use this later in the boolean logic practical application in lesson 3.

<a href="forward"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/forward.png" align="left" height="260" width="300" ></a><br><br><br><br><br><br><br><br><br><br>
