## Copying Files and Folders/Directories

### How to use the cp command to copy files to another file 

Cp file_to_copy.txt file_to_Copy_TO.txt

In the desktop = cp file1.txt file2.txt

In the home folder = cp \~/Desktop/file1.txt file2.txt

SO IT WILL COPY THE FILE TO ANOTHER FILE even if the second file is not
meade, it will create it

### How to use the cp command to copy file and paste into directories 

cp file1tocopy file2tocopy ...however files to copy....... foldername/

as a result it will coy files before the folder name into the folder
name

the command cp folder1/\* . = copy all files in folder 1 back to the
current path (.) which is desktop. If you did .. it would go back to the
previous directory which would be the home folder

![](vertopal_48239ac437ca4266baff2cc2b6dd4fe9/media/image1.png){width="5.584113079615048in"
height="0.531324365704287in"}

### How to copy and paste entire folders cp -r

Have a folder you want to copy

Use the cp command with the -r command which is the recursive so and
everything inside it

Cp -r folder1/ destinationfolder/ this is within the same directory but
you can use the absolute to copy to another folder in another place

## Moving + Renaming Files and Folders

Use command to rename = use mv oldname.txt newname.txt

![](vertopal_48239ac437ca4266baff2cc2b6dd4fe9/media/image2.png){width="6.268055555555556in"
height="0.6402777777777777in"}

Same thing works for directories = mv oldfolder/ newfolder (new name
without the/)

This doesn't damage any of the folders inside

### Move 1 folder contents to another folder use the mv command 

mv newfolder/\* . = move everything from within newfolder into . which
is current working directory -- as a result the new folder will be empty

### move files back into a folder using mv

mv file\* newfolder/ - moves everything beginning with file into
newfolder

### move 1 folder to another folder somewhere else

mv newfolder/ \~/Documents/ = this will move it from desktop

### how to move folder to another folder and rename at same time

mv \~/Documents/newfolder/ ./jackpot = so we move newfolder fomr desktop
to the current folder (.) and since theres no name beginning with
jackpot then the newfolder will be renamed to jackpotand don't have a /
after jackpot

![](vertopal_48239ac437ca4266baff2cc2b6dd4fe9/media/image3.png){width="4.627870734908137in"
height="0.35583223972003497in"}

## Editing Files using Nano 

Use nano to edit and create files using cli

Go to the folder you want then type nano diary.txt to open a user gui in
the cli -- the diary is just a file name

If you did not have that file before then it by default is created

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_48239ac437ca4266baff2cc2b6dd4fe9/media/image4.png){width="4.567142388451444in"
height="3.22877624671916in"}

To save your nano file in another location not the Desktop like we in --
use the control O which means write out and thenyou can rename chose
your location.

Nano can be used if you remotely access a server that does not have a
gui installed so the nono will still show its ui

The write up is to save the file

The read file -- will read another file content and place into this file
-- it will say from ./ meaning from this directory then you type in the
file name

Where is = search for words in your file -- doesn't matter with case
sensitivity -- which is a search forward unless you engage search
backward for things before. If you maximise the screen you will find
more functions in the where. It will have the M-C which is alt C = to
include case sensitivity. M- = alt

Replace = search the word to replace and change of word to do it. It
will then ask you for the 1 word or all etc

Cut text = control K

Paste = control U

Justify = text been set to take full space width of the screen getting
rid of enters

To spell = spell checker is not usually setup for nano -- to set one up
save file write it -- go to nano config file in the base directory in
the etc command nano /etc/nanorc -- and we exit it because we cannot
edit the file so we run the command sudo nano /etc/nanorc. Sudo allows
you to run as admin and you enter your password then you have access --
remove the has from the set speller and write out and close to dave an
then go back to our program before we can go to our spell checker and it
will work -- and you can change your details

Location / Cur Pos = current position of your cursor

Go to line = control and \_ = enter the line and column number you want
the cursor to go to

Undo -- alt U

Redo -- alt F

Mark text -- alt A

Copy text = alt 6
