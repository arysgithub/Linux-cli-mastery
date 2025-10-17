Day 6

## Navigating the file system 

How to use the pwd and ls commands

Where are we in the current Linux system:

-   The shell will already tell you
    ![](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image1.png){width="3.1983628608923884in"
    height="0.3750524934383202in"}

Aaryan is the user of who is logged in

@ symbol then the name of the computer Aaryan-VirtualBox thcomon and
then the squiggle called tilder -- the bash way to show the current path
to the current users home directory. The \$ is to begin

### The pwd -- Print working directory -- starts with a / called an absolute path

-   Tell us the folder our shell is currently working in ![A screenshot
    of a computer AI-generated content may be
    incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image2.png){width="2.0819192913385827in"
    height="0.4031463254593176in"}

> The starts from the root directory / till we get to the home directory
> for the user Aaryan. I.e if you go my computer in files

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image3.png){width="3.5068864829396325in"
height="2.190152012248469in"}- this here is the base root directory

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image4.png){width="2.7816382327209097in"
height="1.458536745406824in"} then into home there\'s a folder Aaryan

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image5.png){width="3.561672134733158in"
height="1.7524245406824146in"}- this is where we are in the shell

### Command to see what\'s in the folder -- ls command

Can use the gui file system OR LIST command ls -- ls cannot do standard
input it does cli args. Ls absolute path, or ls \~ or ls by default will
list the content that your currently in just type ls

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image6.png){width="6.268055555555556in"
height="1.7458333333333333in"}

Blue text = folders or you can use ls -F = classify the Folders with a /
afterwards

White text = files

![A computer screen shot of a computer code AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image7.png){width="6.268055555555556in"
height="0.9041666666666667in"}

You can do ls -F \> list.txt and that will save the standard output in a
file

![A computer screen shot of a program code AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image8.png){width="3.2155063429571302in"
height="1.0849529746281714in"}![A screenshot of a computer AI-generated
content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image9.png){width="2.969352580927384in"
height="2.225323709536308in"}

### Ls -L = puts everything in long form format 

It showcases the file permissions, the date of creations

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image10.png){width="3.8545319335083112in"
height="2.1578718285214347in"}

Everything starting with a d = directory if it is just a -- then it is a
file,then file permission rwr = read write execute for the user. Then
the group the user is in r-x = read and execute. And then for everyone
else just r-x = read and executing. Then you have the hard links to the
file ie 1 or 2 Then you have the user Aaryan and then belonging to the
group Aaryan then shows the file size is 4096kilo Bytes , when it was
last edited and when t was last called and the name of the file/folder

### Ls -lh -- make the file human readable 

![A screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image11.png){width="4.34461832895888in"
height="2.662107392825897in"}

### Cd (change directory)command -- to move/navigate around the file system 

2 ways -- use of absolute path starts with / of where we want to go

![](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image12.png){width="6.268055555555556in"
height="0.47152777777777777in"}

Or option 2 -- RELATIVE PATH -- replace the whole path with the tilder
\~ because tilder will will already be in our HOME path and don't forget
you need the \~/directory

![A black background with green and blue text AI-generated content may
be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image13.png){width="3.9527537182852144in"
height="0.7127909011373579in"}

You could just do it as cd Downloads and that will put you In downloads

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image14.png){width="4.698572834645669in"
height="1.1251574803149607in"} ls no results means no files in downloads

### Cd command to change back to our home directory even if anywhere on file system

1.  Use cd \~

2.  Or use cd /absolute path

3.  Or cd enter and it will take you back to your home directory

### Ls -a will show hidden files aswell

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image15.png){width="6.268055555555556in"
height="1.2506944444444446in"} it will show that these are hidden files
begin with a dot

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image16.png){width="4.594390857392826in"
height="1.1147386264216972in"}

2 very important hidden folders: shortcuts to help you move around your
file system easily

. = current directory - cd . = shell stays where it is

.. = moves back to the previous directory/parent folder -- cd .. = shell
goes back a folder

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image17.png){width="4.448537839020123in"
height="0.718850612423447in"}

![A computer screen with text AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image18.png){width="6.268055555555556in"
height="2.2993055555555557in"}

Here we've gone to our home folder then back to our folder before which
is just a / and in there is the files that are the using the ls are
shown there you will see this is the root folder here for the
administrator -- permission denied

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image19.png){width="3.854704724409449in"
height="0.6980139982502187in"}

![A screen shot of a computer screen AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image20.png){width="5.93832895888014in"
height="1.9481889763779527in"} blue folders and white are files

![A screen shot of a computer screen AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image21.png){width="2.7528379265091862in"
height="1.6879538495188102in"} get back to home folder cd enter

### Tab auto completion -- to speed up navigating file system 

You don't have to go folder by folder when using the cd commnd you just
type cd and the directory you want to go to eg ![A screenshot of a
computer AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image22.png){width="2.040786307961505in"
height="0.7024671916010499in"}

Jump to desktop -- cd \~/Desktop/ and youd go to desktop - and you could
use the full absolute path but

USE TAB COMPLETION -- cd /h then press TAB button and it will auto
complete the word home instead of typing it all out

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_3b7daa096b8b4fd190bc1b57c9c26254/media/image23.png){width="4.952758092738407in"
height="1.0318241469816274in"} - it will give you suggestions of tab if
there were many folders if you press 2 times, so you type a second
letter accordingly and tab and as a result it cuts down our error prone
spelling mistakes

\- this will work for folders and file names

### Opening a terminal from your folder in files

Navigate to your folder in file explorer and right click press open in
terminal and you are there!
