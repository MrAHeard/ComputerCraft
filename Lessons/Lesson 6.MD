##ComputerCraft Communication

In this lesson we will look at how to send messages between computers in ComputerCraft.

<a href="Comms"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/Comms.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

ComputerCraft also comes with a variety of computer components which are all interactive. In this lesson we will look at how to send messages between devices and how to store programs on [floppy disks] (http://en.wikipedia.org/wiki/Floppy_disk) (these were used many years ago before the introduction of high capacity USB memory sticks, they had a capacity of 1.44MB, by today's standards you wouldn't even get an mp3 file on a floppy disk.

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

To be able to print to the monitor we need to tell the computer that there is a monitor attached and also at what side of the computer it is situated at.

We then need to indicate what we want to be written/printed on the monitor.

```
local monitor = peripheral.wrap("left")
monitor.write("Hello World!")
```

<a href="helloworld"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/helloworld.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

Go ahead and save the file, then run it.

<a href="runhelloworld"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/runhelloworld.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

This file is now stored on the disk in the drive, if you right click on the drive and take the disk out you could use this on another machine. This is useful as if you destroyed the computer to move it somewhere else, any programs stored on it would not be saved.

Now you know how to store programs on a disk, create an identical setup (monitor, terminal, and disk drive) somewhere near the one you created earlier. Ensure there is a disk in the drive.

Before we start writing our programs, we need to ensure there is a method of communication for the terminals. We can add a wireless modem on the back of each computer. To add one, you need to crouch (shift) and right click.

<a href="modem"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/modem.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

Now you have two separate systems setup, we will write our programs. On the first machine we will write a message that will listen for a message, go ahead and create a new file called **```receive```**

```
local modem = peripheral.wrap("back")
modem.open(3)
local event, modemSide, senderChannel, replyChannel, message, senderDistance = os.pullEvent("modem_message")
local monitor = peripheral.wrap("left")
monitor.write("The message was: " ..message)
```

Modem and monitor added as before in our earlier program on lines 1 and 4 however the modem is attached at the back.

**```modem.open(3)```** opens the channel that we are going to send our message on. You can only open 128 channels at any given time and the maximum channel you can open is 65535.

**```local event, modemSide, senderChannel, replyChannel, message, senderDistance = os.pullEvent("modem_message")```** indicates the event of receiving a message complete with sender channel, reply channel and message.

Now on the other system we will write a program that will send a message. Create a file called **```send```**.
```
local modem = peripheral.wrap("back")
modem.transmit (3, 1, "Hello World!")
local monitor = peripheral.wrap("left")
monitor.write("Sending...")
```

We use **```modem.transmit(channel, replyChannel, message)```** in order to send the message. The reply channel is captured by the listening computer and suggests which channel they should reply on.
At the end we write a confirmation message on to the monitor indicating what we are doing.

<a href="send"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/send.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

If you now run the receive program first on one machine, then proceed to run the send program on another, you should see the message that was transmitted, displayed on the other monitor.

<a href="receive"><img src="https://github.com/AllenHeard/ComputerCraft/blob/master/Screenshots/Lesson%206%20Images/receive.png" align="left" height="313" width="500" ></a><br><br><br><br><br><br><br><br><br><br><br><br><br>

Using this simple example of transmitting on a channel and providing a reply channel and a message you can see how communication can take place between devices.

In the [lesson 7] (https://github.com/AllenHeard/ComputerCraft/blob/master/Lessons/Lesson%207.MD) you will use what you have learned so far to complete some programming challenges.
