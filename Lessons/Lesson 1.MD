##Lesson 1
In computing, the command line is an important feature. It is an extremely powerful tool and if not used carefully you could do serious damage.

In ComputerCraft we are going to look at some common commands using the command line built in to the mining turtles.
To access the turtles command line, right click on a turtle.

<a href="Intro"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/Intro.png" align="left" height="260" width="300" ></a><br>

Here the command line understands certain dedicated commands designed for controlling the turtle, we can also access the lua command line by typing lua.

Firstly, type ls or dir to list the files and directories (folders) stored on the turtle.

To make a new directory, type mkdir followed by the name you would like your folder to have, for instance, type mkdir myfiles

![cd](https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/cd.png?)

If you type ls you should now see two folders listed, one called rom which already existed, and one called myflies which you just made.

Now to go into this directory you type cd (change directory) followed by the directory name so, cd myfiles

![myfiles](https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/dir.png?)

Now if you type dir or ls you can see the directory we made is empty.

To go back, just type cd ..

![cd..](https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/cd...png?)

Alternatively if we wanted to delete a directory we would type rm myflies (rm - remove) we could also do this for files inside a folder

So now you know the basics of the turtle command line, let’s write our first program in lua.

Type lua at the command line

![lua](https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%201%20Images/lua.png?)

You are now in the lua environment where you can run commands or write programs

To create a new file we need to type edit, followed by the name we would like to give to the file, so let’s go ahead and type edit refuel this will create a blank file that we can write a program in for running later on.

During these lessons well will be using the devices API (application programming interface - a collection of code that, rather than being run directly by the user as a program, is meant to be used by other programs) for use in ComputerCraft that can be found on the [wiki](http://www.computercraft.info/wiki/Main_Page), for this particular task we will be using specific turtle commands that can be found on the turtle API section [here](http://www.computercraft.info/wiki/Turtle_(API)).

