Contribute notes based on [this](https://www.youtube.com/watch?v=Juo_0lpBMPY) video now!

## **What happens when your start a computer?**

The first thing that happens on starting a computer is that it executes the software that are there in the BIOS (Basic Input Output System) also referred to as a firmware.

This firmware comes by default in a computer stored in ROM attached to the motherboard. Secondly, it loads the bootloader which is responsible to initialize the OS.
___

## **What is Bootloader?**

It is a program that responsible for intializing the *Operating System.*

___

 ## **What is OS (Operating System)?**
 
 An operating system (OS) is system software that manages computer hardware, software resources, and provides common services for computer programs. 
 
 ___
## **An operating system should have :**
 - Kernel
 - File system
 - User interface (GUI & CLI)
 - Should be able to manipulate data based on command.
 ___
 
## **What is file system?**

Method or Data Structure that the OS use to store and retrieve the data in the memory.

___

## **What is kernel?**
The kernel is a core component of an operating system and serves as the main interface between the computer's physical hardware and the processes running on it. 
It is also known as bridge between *Software* and *Hardware.*
___

## **What are Most Popular OS ?**
- Microsoft Windows
- Mac OS (Only on apple)
- Linux (UNIX based)
- Android 
- iOS (iPhone Operating system)
___

## **Why use Linux?**
 - Open Source 
 - Support almost all *Programming Languages*
 - Developer Friendly
 - Terminal is superior to CMD
 - Bash Scripting 
 - SSH (Secure Shell)
 ___

  ## **History of Linux**
 
  In **1969** First unix OS created by <u>*Ken Thompson*</u> and <u>*Dennis M. Ritchie*</u>
  10 years later <u>*Richard Stallman*</u> started working on GNU project (BSD , MINIX, etc).

  In **1991** <u>*Linus Torvalds* </u>started working on the "Linux Kernel". This kernel was use in every linux distribution.

>Linus Torvalds is a father of *Linux*  


## **Linux Distributions** 
 - Ubuntu
 - Fedora
 - Arch
 - Kali Linux
 - Pop OS and many more

As a beginner you should start out with Ubuntu.

## **Why Ubuntu than any other distribution?**
- It is Beginner Friendly
- It has a decent UI (user interface)
- Ease to use for non-programmer also

>Fun fact : Linux is all about of Keyboard
___

## **What is Terminal?**

A terminal(black window) is a tool where we are going to write our commands.Start terminal using this command : `ctrl+alt+t` or you can press windows button and type terminal.
___
 
 ## **What is SHELL?**
 A *shell* is a command line interpreter because it executes the commands line by line. 
 
 >Just like how Python (a programming language) works.
 ___
 
 ## **What is BASH Programming?**
 
 Every command we are writing on the terminal is a BASH language.
 ___
 
 ## **Shell Format**
 `apoorvgoyal@apoorvtwts:~$`
  this is the format of shell, lets understand what all this means:
  
  - `apoorvgoyal` : username 
  - `@apoortwts` : hostname
  - `~` : represents the home directory of the user('~' symbol is called tilde)
  - `$` : after this you can start writing command
  ___
  
## **Printing "Hello World" in terminal**
 `apoorvgoyal@apoorvtwts:~$ echo "Hello World" `
 ___
  
## **pwd (Print Working Directory)**
 The pwd command writes the full pathname of the current working directory to the standard output.<br>
  `apoorvgoyal@apoorvtwts:~$ pwd`
  ___

 ## **File Structure in Linux**
 The linux file hierarchy structure or the Filesystem Hierarchy Standard (FHS) defines the directory structure and directory contents in Unix like operating systems. It is maintained by the Linux Foundation.
 
 ![image](https://www.linuxtrainingacademy.com/wp-content/uploads/2014/03/linux-folders.jpg)
 ### if u wanna know in depth then [Go follow this Link](https://www.geeksforgeeks.org/linux-file-hierarchy-structure/)

 ___
   
   
## **Path of a Directory**
Suppose u have to go `/home` directory in the above diagram. How will u go in terminal?

You can use this way `~$ cd ~/home`

## Basics Commands in Linux
|                Task                          |          Command                 |
|----------------------------------------------|----------------------------------|
|List files                                    |`ls`                              |
|Changed directory                             |`cd <Directory name> `            |
|Clean the terminal                            |`clear`                           |
|Make directory                                |`mkdir <Directory name>`          |
|Make file                                     |`touch <File name>`               |
|Reads data and opens in the terminal          |`cat <file name>`                 |
|Previously executed commands                  |`history`                         |
|Short discription of the command              |`whatis <command>`                |
|Remove directory                              |`rmdir <directory name>`          |
|Copy file or directory                        |`cp <directory/file name>`        |
|Move file or directory                        |`mv <directory/file name>    `    |
|Opens a text editor                           |`gedit <file name>`               |