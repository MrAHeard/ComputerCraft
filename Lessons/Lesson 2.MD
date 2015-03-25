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

We will now look at Boolean Logic. Boolean values are simply true or false and a programming language can evaluate expressions and return the value as a boolean.

If you type **```true```** this obviously evaluates to true so this will be printed to the screen, similarly if you type **```false```**, false will be displayed beneath.

If you type **```x =10<15```** a boolean value from the evaluation of that expression will now be stored in the variable x Type **```x```** and it will display true because it will tell you whether or not 10 is lower than 15.

<a href="x"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%202%20Images/c.png" align="left" height="220" width="360" ></a><br><br><br><br><br><br><br><br><br>

If you were to type **```g = 5>4```** what do you think it should display? Try it, was you right?

In the examples above x evaluated to true and g evaluated to false. Now we can start looking at some logic.

Firstly we will look at the logical operator **AND**

Type **```p = x and g```** This type of expression will evaluate to true if x is true and if g is true, if either one of these is false it will evaluate to false. What should it be? Try it, was you right?

We can explain this a little clearer by doing the following, if we type **```true and true```** well they are both true so it must evaluate to true. However if we type true and false one of those values is false so the evaluation of the two together can never be true. The same applies if you type **```false and true```** one of them is false so the expression evaluates to false. It is hopefully obvious then that when we use and they both have to be true for the whole thing to become true. What would false and false be?

The next logical operator we will look at is **OR**. Remember with **AND** both sides of the operands either side of the and operator had to be true for the whole thing to evaluate as true. With **OR** only one of them has to be true for the whole expression to be evaluated as true. 

In our examples x was true and g was false, if you now type **```j = x or g```** and then check j it will evaluate to true

We can list the outcome of all possibilities like this for **OR**

<a href="OR"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%202%20Images/or.png" align="left" height="220" width="360" ></a><br><br><br><br><br><br><br><br><br>

False OR False is the only instance where OR can produce false, when both are false.

The above table is called a truth table and these are extremely useful to quickly see the functional values of logical expressions.

Using what you have learned so far, what would be the truth table for AND?

<a href="OR"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%202%20Images/and.png" align="left" height="220" width="360" ></a><br><br><br><br><br><br><br><br><br>

To see this applied in actual code where conditions cause things to happen we could try the following:

We know in our examples that x is true, we also know g is false

So in lua type: **```if g then print “Yes” else print “No” end```**

<a href="if"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%202%20Images/d.png" align="left" height="220" width="360" ></a><br><br><br><br><br><br><br><br><br>

To break this down, basically if g is true (it is after all holding a boolean value so we can do this) then Yes will be printed, otherwise No will be printed. What is going to happen? Try it.

Now type the same command using x instead of g. What happens? Do you understand why?

The last logical operator we are going to look at is **NOT** so if we were to type **```not true```** then false would be displayed, and in contrast to this if we type **```not false```** then true would be displayed, this makes sense when we say it too!

If you type **```a = true```** and check the value of **```a```** it would print true. 

Now type **```a = not a```** and check what is displayed. This kind of notation would flip the value held in **```a```** 

In the next lesson we will look at a practical example of this.

Move on to [Lesson 3](https://github.com/AllenHeard/ComputerCraft/blob/master/Lessons/Lesson%203.MD)
