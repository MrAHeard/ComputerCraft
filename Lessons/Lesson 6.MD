##ComputerCraft Communication

In this lesson we will look at how to send messages between computers in ComputerCraft.

<a href="Comms"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/Comms.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

ComputerCraft also comes with a variety of computer components which are all interactive. In this lesson we will look at how to send messages between devices and how to store programs on [floppy disks] (http://en.wikipedia.org/wiki/Floppy_disk) (these were used many years ago before the introduction of high capacity USB memory sticks, they had a capacity of 1.44MB, by today's standards you wouldnt even get an mp3 file on a floppy disk.

Set yourself a work area up with (from left to right) a monitor, a computer terminal, and a disk drive like the one below:

<a href="setup"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/setup.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

Monitors can be joined together to form a larger monitor, this can be useful for displaying larger amounts of text on the screen. Expand your monitor to a 3x3 as below:

<a href="monitor"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/monitor.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>


In the same way as you wrote files when working with turtles, a computer terminal works in the same way. The addition of a disk drive alllows us to transfer programs on a disk form one work station to another. 

Let's start with a basic example program that will print something to the screen and we will save it to a disk.

Ensure you are equiped with a disk and right click on the disk drive. Place the disk in the slot as shown:

<a href="disk"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/disk.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

You will notice a green light appear on the disk drive indicating there is a disk present. Now right click on the terminal.

To select the disk drive, type **```cd disk```** and create a new program called print (**```edit print```**)

<a href="editdisk"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/editdisk.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

To be able to print to the monitor we need to tell the computer that there is a monitor attached and also at what side of the comuter it is situated at.

We then need to indicate what we want to be written/printed on the monitor.

```
local monitir = peripheral.wrap("left")
monitor.write("Hello World!")
```

<a href="helloworld"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/helloworld.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

Go ahead and save the file, then run it.

<a href="runhelloworld"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/runhelloworld.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

This file is now stored on the disk in the drive, if you right click on the drive and take the disk out you could use this on another machine. This is useful as if you destroyed the computer to move it somewhere else, any programs stored on it would not be saved.

Now you know how to store programs on a disk, create an identical setup (monitor, terminal, and disk drive) somewhere near the one you created earlier. Ensure there is a disk in the drive.

Before we start writing our programs, we need to ensure there is a method of communication for the terminals. We can add a wireless modem on the back of each computer. To add one, you need to crouch (shift) and right click.

<a href="modem"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/modem.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

Sending messages between computers with wireless modems

Functions
Make a castle
