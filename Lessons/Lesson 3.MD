##Lesson 3 - Logical Expressions

Remember in lesson 1 where we moved a turtle forward using the command **```turtle.forward()```**? If the turtle could successfully move (nothing was in its path) then true would be printed to the screen. If something was in the way and it was unable to move, then false would be printed to the screen.

<a href="n"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%203%20Images/a.png" align="left" height="220" width="350" ></a><br><br><br><br><br><br><br><br><br>

We are now going to write a small program that uses boolean variables to determine values of logical expressions, we are also going to use if statements to determine action based on conditions being met.

We are going to write this program on a turtle so if you don’t have one of those close by, place one in your world now.

As you did in lesson one, make a new file ready for editing and call this one **```move3```**

Now type the following:
```
a = turtle.forward()
b = turtle.forward()
c  =turtle.forward()

if a and b and c then
     print “Moved 3 spaces successfully"
else
     print “Unable to reach destination"
end
```
You will remember from lesson 1 and the introduction to this lesson, the first three lines of the code are going to return a boolean value. These will then be assigned to the variables a, b, and c. If the turtle manages to move forward successfully three spaces then they will all be true.

The if statement beneath will then evaluate the three variables for truth and if they are all true then a successful move message will be printed. Otherwise it will say unable to reach destination. This would indicate that the turtle has been blocked along its path somewhere.

Now test your program by typing **```move3```**

We know we can perform mathematical calculations when programming, for instance typing **```3 + 4```** would result in a printout of **```7```**. What we will now look at is testing for equality.

Type **```3 == 3```** what is printed to the screen?

This statement is returning a boolean value based on the value on the left of the double equals signs compared to the value on the right, similar to saying is 3 equal to 3, which in this case is, so true is printed.

Now type **```t = “test"```**

Typing **```t```** will return the value assigned to t

<a href="n"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%203%20Images/b.png" align="left" height="240" width="380" ></a><br><br><br><br><br><br><br><br><br><br>

If you now do an equality test to see if **```t == ‘test”```** you will see true printed. This is because we assigned the value test to the variable t

You can also type **```“test” == t```** and true will also be printed, do you understand why?

Try typing **```t == “wrong”```** what will be printed and why?

In lesson 2 we ended the lesson by looking at NOT. We can code not in lua by typing the **```~```** sign (tilde) so if you were to write **```2~=3```** this is the same as saying is 2 not equal to 3.

2 isn’t equal to 3 so true should be displayed. Try it.

Now try out **```3 ~= 3```**, what is this saying and what will the result be?

What would be the result of the following expressions:
```
15 > 12

(4 * 7) == 29

13 ~= (9 + 4)

21 + 7 == (50 - (2 * 11))

112 + (3 * 15) ~= ((2 * 50) + (4 * 12 ) + 1)
```
Move on the lesson 4 to learn about while and for loops.
