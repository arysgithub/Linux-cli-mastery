# Mastering Open Source Software 

What, how and how to manger software and opensource software

## THE GNU Project -- history 

What is Linux? Linux is actually a piece of the whole O/S -- it is the
Kernell

Richard Stallman:

September 1983 -- announces GNU Project -- developing a O/S similar to
UNIQs but complete free software

JAN 1984 -- quit MIT to work on GNU full time

FREE SOFTWARE (think free speech rather than free lunch) :

1.  freedom to run a program as you with for any purpose

2.  freedom to study how the program works and change it so id does your
    computing as you wish (freedom 1). Access to the source code is a
    precondition for this (ie open source)

3.  the freedom to redistribute copies so you can help your neighbour

4.  the freedom to distribute copies of your modified version to others
    (freedom 3), by doing this, you give the whole community a chance to
    benefit from your changes. Access to the source code is a
    precondition for this

There is a licence that gives a user these abilities the GNU PUBLIC
LICENCE OR GPL

1991 -- gnu almost complete but was a missing part (the KERNELL)

A kernel is responsible for allocating the resources on computer\'s
hardware that is required by the computer\'s software. SO THE INTERFACE
LAYER BETWEEN A COMPUTER\'S HARDWARE AND THE APPLICATIONS IT IS RUNNING.

In 1991 -- Linus Torvald invented a Linux -- and released Linux Kernal
under GPL v2.0

Now the Linux Kernal Completed the GNU project.

The Linux kernel is used on android and chrome OS -- to interface
between the software and hardware.

## uname command

-   tells you loads of information about your computer eg

-   uname -o = the operating system of your computer = GNU/Linux

gnu.org - <https://www.gnu.org/>

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image1.png){width="6.268055555555556in"
height="5.536111111111111in"} = everything to do about the GNU system
and you go to software section and scroll down to ALL GNU packages --
you can see that there is links to every code run on gnu system even the
Linux-libre of all of the source code for the Linux kernel system.

Core utils package had the commands we use on the Linux terminal

LINUS IS ACTUALLY DNU+ LINUX OS

## Modifying and Installing Source Code 

Download, edit, compile and install open source software

Go to gnu.org and go to software and go down to ALL HNU packages and
open up the coreutils package which has all the information of the
commands we used in linux cli -- scroll to downloads -- stable source
released -- tested and final and test is still in progress. Click the
stable -- and the most recent are in the bottom of the page and we want
the one ending in .xz popo up comes -- then save file to downloads. In
terminal you can ls the downloads folder and you will see the download
which is a compresed using the xz algorithm.

![A black background with colorful text AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image2.png){width="4.9069346019247595in"
height="0.9584667541557306in"}

We can unpack using the tar command = tar -xJf filenames -- never gave
it v option so no loads or results but if you type ls you will see ther
is the unzipped folder there.

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image3.png){width="6.268055555555556in"
height="0.8826388888888889in"}

Cd into the core utils and ls we've got a lot of stuff.

![A screen shot of a computer program AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image4.png){width="6.268055555555556in"
height="2.4631944444444445in"} But then go to the src folder and cd into
there you will see files. Lets pipe the data into the less command to
see easily go up or down and view what we want.

Loads of files ending in the .c which is C programming lang

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image5.png){width="6.268055555555556in"
height="1.6590277777777778in"}

Use the grep and pipeline ls into the grep to search for the lines which
contain ls

Ls \| grep ls = return all words of files which contain ls

![A computer screen shot of a program AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image6.png){width="6.268055555555556in"
height="2.717361111111111in"}

The one we interested in is the ls.c

Nano ls.c -- this is the source code for the ls commands -- but we can

### also modify the ls source code and recompile into a running software 

![A computer screen with text and images AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image7.png){width="5.003123359580052in"
height="4.198233814523185in"}

You can modify so whenever ls runs another operation can also happen --
in the ls the main function starts at about line 1695 using nanos
function shortcut control+ / you can go to a specific line and you can
search for words using control +F to find

Weve added this line of code in ![A black background with white text
AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image8.png){width="5.688293963254593in"
height="1.354355861767279in"} the printf one so save and exit

### How how do we turn this code into a runable program and install onto our laptop

Coz they written in c they need to be compiled into machine language --
the compiler used is gcc

So we need to install gcc so do -- sudo apt-get install gcc

![A screen shot of a computer AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image9.png){width="6.268055555555556in"
height="1.2569444444444444in"}

Gcc compiler installed

Then go back ![A computer screen shot of a program AI-generated content
may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image10.png){width="6.268055555555556in"
height="1.66875in"}

Configure the gcc code to our machine by opening the bash configure file

![A screen shot of a computer screen AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image11.png){width="6.268055555555556in"
height="0.8569444444444444in"}

It also create a new file calls the make file -- and we would need to
install the make command to make the make command work.

![A screen shot of a computer program AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image12.png){width="6.268055555555556in"
height="2.183333333333333in"}

Now we can run the make file:

![A screen shot of a computer AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image13.png){width="5.709130577427821in"
height="1.0313943569553805in"}

It will comile all the files it has found that has not been compiled
recently including our ls file -- it comiles into machine code so it can
be executable by our laptop

Install the machine code in the required places for it to work -- then
run sudo make install

![A computer screen shot of a program AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image14.png){width="6.268055555555556in"
height="1.9652777777777777in"}

if you close the terminal then open it and run ls it should wok our
prompt on the ls

![A close up of text AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image15.png){width="6.268055555555556in"
height="0.9305555555555556in"}

And it works

To change it back you just need to re-edit the source code recompile
with make and then it will go back

### Change the code back 

Go back to the src -- then do nano ls.c

![A screenshot of a computer code AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image16.png){width="4.250592738407699in"
height="1.8648436132983377in"} delete it

Save exit the nano

![A computer screen shot of a program AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image17.png){width="6.268055555555556in"
height="1.2222222222222223in"} was in the wrong folder first

Close the termial and reopen again and will work as before

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image18.png){width="6.24045384951881in"
height="1.1980839895013122in"}

## The Software Repositories 

-   library of software to browse and access through a line of a command

-   Ubuntu\'s software repositories

You don't have to give the software bak and you can update eaily when a
new update comes in

<https://help.ubuntu.com/community/Repositories/Ubuntu>

ubuntu has 2 main repositories for free and another 2 that aren't free

<https://packages.ubuntu.com/> ubuntu package search features

### check what package your ubuntu is on your cli: lsb_release -a

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image19.png){width="4.698572834645669in"
height="2.0106977252843397in"}

These are all the sections or categories of the package I have -
<https://packages.ubuntu.com/plucky/>

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_ff297c85bcce4ed7a206a52dcba7b88c/media/image20.png){width="5.142012248468942in"
height="4.679424759405074in"}

The all packages and where they come from
-https://packages.ubuntu.com/plucky/allpackages

It shows you in square brackets which repositories they come from.

No square brackets means it comes from main repositories

So open the first package -- you will see the name, the version and the
package repositories in square brackets . You will see other packages
related to it. You can see what each file contains and the different
sizes

### To check your computer architecture -- use the command uname -m 
