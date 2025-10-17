**Intro: Why install Linux on your own VM if you don’t have a Linux OS:**

This way you can play around with whatever you like, without risking, damaging or anything going wrong. 
Think of it as your perfect playground to practice all your skills and learn how to use the Linux terminal. 
Learn how to learn everything about files with Linux CLI
Automate tasks using bash scripts – and run them at specific times. 

NOTE I actually realised I have created bash files before in uni when doing courses and practicals involving LCI and automating tasks.
Learn how to search for new software from repositories and manage it with software managers on the CLI
Source code and compile into working projects

**How to install VirtualBox, Ubuntu and run a Linux Virtual Machine**

A virtual Box allows you to run virtual machines (virtual computers) inside your computer without affecting your current running machine. 
 - click your associated platform package and download – double-click and fill out the installer wizard. Then your Virtual Box is installed
Set up your own Linux virtual machine – using Ubuntu
 - How to select the latest version eg Ubuntu 24.04.3 LTS – is the 2024 version in the 4th month May, but Ubuntu 25.04 – is the 2025 version in the 4th month – click download – takes a while to download because the file is large – save it where you’d like. 
Run virtual Machines – use Virtual Box and Ubuntu
Open Virtual Box – click new – give it a name, it should pick up the type -Linux and the right version type – select the amount of RAM to be allocated to the VM. The RAM will only be allocated while it is running, when the VM is turned of the host will get it back. Give yourself a good amount of RAM, anywhere in the green or so halfway or nearer to the red. 
Going to ask you about a Hard Disk- Because a VM requires a HDD, but for the project we are going to create it a virtual hard disk now with Is just a file like a folder which simulates an HDD, but its not. SO click VDI – Virtual Disk Image. Do you want a dynamically allocated disk or a fixed-size disk? I’d choose dynamic, you can click and store wherever you'd like, give the max limit of file data of like 20GB for the imaginary HDD
Click on settings of the VM you just made – for a bit more power, go to settings- system- and click the processor to the number of cores you have so the Vm runs faster. And on Storage, the Controller Ide where disk says Empty (click) – then click on the Optical disk icon and choose virtual optical disk file – then go to the file where you stored your Ubuntu download and click open. 


Now everything is set up and ready to go. 
**Launching Linux for the first time** – 
Open Virtual Box – Click Start – open our imaginary computer inside our computer, A VIRTUAL MACHINE from that imaginary disk file Ubuntu. Then it will give 2 options: try or install Ubuntu – click install and your language (English) – allow download, and 3rd party install for wifi hardware, MP3 etc. – might say this computer has currently no detected OS – click erase disk and install Ubuntu -write changes yes and click country for time zone, then keyboard layout (English Uk). Will ask name, put your first, computer name VB, username and password. Then you can restart your virtual box and press enter – now you can log in and enter you VM, basically a second app, and everything 
YOU have linux running computer inside your own computer now



**Mastering the Linux Terminal**
**First Commands:** 
Open the terminal in the VM – keyboard shortcut CTRL+ALT+T
echo Text – prints out what you give it as input – ie Text
cal – enter = calendar of the entire current month with the current date highlighted
cal 2020 = entire calendar for 2020 with highlighted current date
cal -y= entire calendar for random year 
date = day, date, time, time zone and year
clear = clean up the Linux terminal 
CTRL+L = clear the entire screen
The above arrow = goes to the previous commands typed
History = all previous commands
From the history, you can see which commands you entered so if you want to run command 2 out of 20, you don’t have to scroll all that way, just type:
!2 = runs the 2nd command you entered out of the 20
!! = run the most recent command you’ve done
history -c; history -w = clears the history, then writes that to make it permanent
exit = Close terminal – X button or CTRL D
I remember these as I did this during semester 2 of the first year of Uni. 

**How to Understand Command Structure**
Everything is case sensitive 
Command – little computer programs stored somewhere on your laptop. Eg all above 
Structure for Commands - Command name, options(customised behaviour), input(to operate on).  

The terminal acts as a window to the Shell. The Shell is what interprets commands for when they are submitted through the terminal.. What this means is that your Shell will know what program you want to run from the name, then it will search on the Shells path (the files), and what you want done
Echo $PATH  = The Shell path you are in folder path separated by : and the / is a folder. 
It reads from the very left so will go from the very far left folder first because it searches in order of first preference. 
Which cal  = see which folder a command is in so cal command is in a certain folder /user/bin/cal
Which/which - /user/bin/which

OPTIONS: date -u = date in UTC,
 cal -y, date -a -b -c -d -e = all options from a to e or same output if date -abcdef, 
 date –universal (long names have 2 dashes) 
I can have a more customised behaviour = cal -A 1 12 2017 = calendar for DEC and 1 month after, -B = before 
Cal -A 1 -B 1 12 2017 = calendar for 1 month before and 1 month after Dec 2017

INPUT is known as OPERAND (considering you don’t have options then you have a space after your name and the OPERAND/what to do eg cal 2020, can also give more than 1 input cal 12 2020 = DEC 2020)
Honestly, I've also done this stuff with A-levels and uni 

**Using the Linux Manual**
How to access and read your manual (man) pages that has all the commands and Linux full fundamentals on how to ube the commands. 
8 Sections:
1 User commands – all users can run them 
2 system calls – advances programming functions system calls
3 c library function -libraries for C
4 devices and special files – how different devices on your computer managed
5 file formats and conventions – formats for word, pdf configurations etc
6 games – games available on system
7 miscellaneous – protocols, file systems
8 system admins – setting up automations and all system admins
How to search for commands on the Terminal
 – use the man command, -k is for searching and the input which(a search term) – and are the manual pages that come out and the pages that they are in (1 -user command) (8-system admin) 

How to use the command
 – you read the SYNOPSIS section after being in a man search page eg below

Man 1 which for the locating commands and then q to go back to the terminal 

Eg the synopsis on the which sasys you can have multiple filenames so I can do which cal date echo and it will give me the file locations for each

man 5 securetty gives this here: 
SYNOPSIS NOTES: 
Which [-a]  <SOMETHING> = this means that the file a is something that is mandatory, and it has to be there
Which [ -a | -f] <SOMETHING> … = this means I can have one or the other, so either a or either f 

Learn about a new command from scratch: 
Command ot list out a directory's contents – so search what might be available within the manual 
Man -k “list directory contents”  -in quotation marks so all 3 words are searched at the same time. Usually, if command manual are in the first section when typing them with man no need to repeat 1 

man ls you can scroll done the description to use many options

According to the synopsis we can also just enter ls alone because option and file are both optional and … (many ) so ls enter

Ls -l more organised 

4096 is all the file sizes – to make this readable in the description it says you can use h to make anything human readable especially with l and s so you can see the size below is now 4.0k for words that sound like 2 works then the linux command will have a – between them

**See also the section in man pages – for links**
To open the page press CTRL+ left click
Some commands are defined in SHELL but not MAN
SHELL COMMAND IS help. To find all the commands that need help just type help and enter and you will get all the help commands. So if man doesn’t work use the help

I know about shell and have used and  built shell projects and commit to git using shell  on my windows Cli but it’s the first time I used man and I guest has for the Linux system. 

---

## 📘 Topics Covered
- Basic CLI navigation
- History commands
- Shell and environment variables
- Command structure: options, flags, arguments
- Manual pages
- VirtualBox and Ubuntu setup

## 📅 Timeline
This journey is updated daily with what I’ve learned. Each day will be logged as a separate Markdown file under `/logs`.

## 🔗 Connect
Follow my DevOps-in-Public challenge on [LinkedIn](https://linkedin.com) and check out my GitHub for all projects in the journey.
