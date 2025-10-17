## Piping Fundamentals 

Piping - Taking the standard output of 1 command so that it connects and
flows to the standard input of another command ie command 2.

Linux CLI is used to perform 1 task extremely well. This makes piping
incredibly powerful if you can assemble these highly specialised
commands and pass data between them -- this enables the creation of
advanced pipelines.

Eg the date command -- shows us the date, we can use redirection to save
this information to a file called date.txt

![A black background with white text AI-generated content may be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image1.png){width="5.00069772528434in"
height="0.7084317585301837in"}![A screenshot of a phone AI-generated
content may be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image2.png){width="4.156829615048119in"
height="0.9272123797025372in"}

Now we just want the day of the week which in this case is Sat -- you
could use the cut command:

First read the date.txt into standard input for cut command (this will
cut up the file and give you specific columns), so eg Sat would be the
first field/colum and the Oct will be second column/field. -- so we need
to give it the --delimeter long form that will tell you what devides the
columns in the file which is in this case is a space which is a " " and
then we need to tell it the --fields and then a space and then 1. So --
cut \< date.txt --delimiter " " --fields 1 and then enter we get Sat as
an output

![](vertopal_f173428944e74149b74aee3634ac2b66/media/image3.png){width="6.268055555555556in"
height="0.37569444444444444in"}

Works but is cluncky -- the writing to a file which takes memory then
reading the file into the cut command -- after getting the data out we
would have to delete the file etc.

### SO HOW PIPELINING DOES THIS 

-- pipe the date directly into the input of the cut command

USE this symbol to PIPE \| - so you want to pipe the data from the date
command standard output into the cut command standard input so do date
\| cut --delimiter " " --fields 1 and you will get Sat. DONE ALL IN ONE
STEP

![](vertopal_f173428944e74149b74aee3634ac2b66/media/image4.png){width="6.268055555555556in"
height="0.3763888888888889in"}

And we can further output the data ie Sat into a file

![](vertopal_f173428944e74149b74aee3634ac2b66/media/image5.png){width="6.063346456692913in"
height="0.4792333770778653in"}

![A white background with a black line AI-generated content may be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image6.png){width="4.2714293525809275in"
height="0.7501049868766404in"}we can even do it with an error file
Aswell = date \| cut --delimiter " " --fields 1 1\> cutOutput.txt 2\>
error.txt

TBH, it doesn't matter where the redirection is placed; it can be at the
beginning, after the cut, in the middle of the different options, or at
the end.

PIPELINING to a 3^rd^ command -- just add another \|

AND YOU CANNOT try redirecting in the middle or between a pipeline eg --
date \> data.txt \| cut --delimiter " " --fields 1 = the result of this
is the pipelining to cut does not happen, the data.txt file is created
with the date data but nothing is passed onto cut and the pipeline is
not continued. Redirection is processed before pipes in shell so it
breaks the pipeline. OR CAN IT???? -- YES BY USE OF THE TEE COMMAND
WHICH IS MORE ADVANCED

## Pipelining - advanced piping techniques 

### TEE COMMAND 

![A diagram of a computer AI-generated content may be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image7.png){width="2.8328040244969377in"
height="1.8068372703412074in"} - pipe between 2 commands and in the
middle we are using the tee command to pipe 2 commands to cause data to
flow horizontally pass the data on the pipeline and fall vertically to
also store data in file. You will need to do it like this command 1 \|
tee file.txt \| command 2 so use of 2 \|. The Tee command takes a
snapshot of the data flowing through It at that point and saves it in a
file and refirection of standard output can no longer flow down the
pipeline.

![](vertopal_f173428944e74149b74aee3634ac2b66/media/image8.png){width="6.268055555555556in"
height="0.3548611111111111in"}

![A screenshot of a phone AI-generated content may be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image9.png){width="4.427701224846894in"
height="0.9272123797025372in"}

date \| tee date.txt \| cut --delimiter " " --fields 1 \> today.txt --
to save all the data into toady.txt and to date.txt using redirection.

![](vertopal_f173428944e74149b74aee3634ac2b66/media/image10.png){width="6.268055555555556in"
height="0.3090277777777778in"}

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image11.png){width="3.5317432195975504in"
height="0.9272123797025372in"}![A white background with a black line
AI-generated content may be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image12.png){width="2.6205325896762903in"
height="0.5542125984251969in"}

Redirection means you cannot do anymore pipelining after that
redirection. But we can have a second tee command and then the pipeline
can continue

### Xargs command

Xargs Command -- TURN your piped data into command line arguments.

Not all commands accept standard input and some only accept cli
arguments this is when you will need to use xargs arguments which
convert them to command line arguments to make your pipelines
indestructible.

Date command and pipe into echo basically echo "hello" and echo spits
hello. Echo doesn't accept standard input -- it only accepts cli
aguments

#### HOW TO USE CONVERT DAT FROM STANDARD INPUT INTO CLI XARGS command

Xargs converts data from standard input into cli arguments eg: date \|
xargs echo result is the full date.

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image13.png){width="5.073624234470691in"
height="1.4377001312335957in"}

And we can give echo its own text date \| xargs echo "Hello" but it will
process Hello first

![](vertopal_f173428944e74149b74aee3634ac2b66/media/image14.png){width="5.677876202974629in"
height="0.41672462817147854in"}

We need to pipe down because the data that comes out is still on
standard output

![](vertopal_f173428944e74149b74aee3634ac2b66/media/image15.png){width="6.268055555555556in"
height="0.33819444444444446in"}

Example works -- cerate new file in files called deleteme.txt

![A screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image16.png){width="6.268055555555556in"
height="1.0in"}

Rm command is the command to remove/delete stuff -- this only accepts
cli arguments

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image17.png){width="5.19424321959755in"
height="1.5854352580927384in"}

Lets create a file called filestodelete.txt which will contain names of
files to delete like cutOutput.txt, date.txt, today.txt

We can use the cat to read the file, we cant just pipe the info into rm
command -- but we can pipeline into rm with xargs and then it works and
deletes the files:

![A computer screen shot of a computer program AI-generated content may
be
incorrect.](vertopal_f173428944e74149b74aee3634ac2b66/media/image18.png){width="6.268055555555556in"
height="1.8375in"}

### Summary 

-   Piping connects STDOUT (standard output)of one command to the STDIN
    (standard input)of another command. And STDERR -- standard error

-   Redirection of STDOUT breaks pipelines

-   To save data "snapshot" without breaking pipelines using the tee
    command

-   If command doesn't accept STDIN but you want to pipe to it, you can
    use xargs aslong as it accepts cli arguments

-   Commands you use with xargs can still have their own arguments like
    they would have had if they didn't have the xargs -- and they will
    be executed first

If you understand all of this day 3, then you have unlocked the crown
jewel of CLI
