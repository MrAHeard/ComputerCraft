##Lesson 2

In this lesson you will learn about Variables and Boolean Logic.

A variable in a program is something that can be given a value, this value may remain the same throughout the course of the program or alternatively it may change depending on other factors in the program. For instance a variable containing a High Score in a game would remain the same until such a time the high score is beaten. At this point, the variable would take on the new high score.

In ComputerCraft, place a Computer block down and right click on it. Then enter the lua environment using the command you learnt last lesson.

Firstly we will look at numeric variables, variables that take the form of a number.

If you type **```n = 5```** and press enter (from now on we will assume you know to press enter after inputting a command), this has assigned the value 5 to the variable n

If you now type just the letter **```n```** and press enter, the value 5 will appear as this is what is stored in n

<a href="n"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%202%20Images/a.png" align="left" height="260" width="350" ></a><br><br><br><br><br><br><br><br><br><br>

We could also change the value of n by assigning a new value, type **```n = 10 + 20```**

Now type **```n```** to check the new value assigned to it

These are pretty straightforward assignments for a variable and many more complex formulae can be evaluated (worked out) by programming languages. Try the following example, whilst not complex, it does show how to format a variable assignment using order of operation.

**```n= 3 x (5+8)```**

Probably one of the most common variable assignments is one where a value is incremented (gradually added to), usually in a loop to perform an action a set number of times

Below you will notice the variable is now i instead of n, we can call our variables anything but it is recommended to call them something that makes sense. This is especially useful when debugging code (finding/solving errors)

**```i = i +1```**

We will now look at string variables, they are variables that take the form of an arbitrary string of characters.

For instance type **```h = “hello”```**

If you then type **```h```** it will print hello to the screen as this was the value that was assigned to h

Similarly if you type **```w = “world”```**  and test it, world will be printed to the screen.

Sometimes in programming it is useful to join strings together, this is called concatenation. You can do this in a number of ways depending on the programming language. In lua we use **```..```**
to concatenate strings, for example if you now type **```hw = h..w```** and test it, you will see it prints **```helloworld```** because its simply joined the two values (h and w) together.

If you want a space then you need to join a third string containing a blank space like this **```hw = h..” “..w```** This joins h to a space and then joins w on the end to produce **```hello world```**

<a href="hello world"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%202%20Images/b.png" align="left" height="240" width="360" ></a><br><br><br><br><br><br><br><br><br><br>
