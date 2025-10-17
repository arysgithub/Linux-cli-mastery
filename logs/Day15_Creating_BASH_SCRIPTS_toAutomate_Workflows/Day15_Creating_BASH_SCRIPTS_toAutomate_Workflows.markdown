## Creating bash scripts to automate workflows 

All you need to do is make a text file -- from cli -- use nano
our_script.sh

Now if you do file our_script.sh = we see that as far as the shell is
concerned its just an empty file

IN nano our_script.sh

-   you need to tell it that this is a special file use an interpreter
    as a bash script code

-   if a bash script and typed echo It would understand that it's the
    echo command

use the shebang #! Then /bin/bash (path to our bash command). If you do
the where bash you get /bin/bash

#!/bin/bash - run this as a bash line on the first line and no spaces
anywhere. Now when you save that

![](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image1.png){width="6.268055555555556in"
height="0.7569444444444444in"}

when you do the file our_script.sh It will tell you it a boune again
bash shell script file

![A screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image2.png){width="6.268055555555556in"
height="2.4319444444444445in"}

### Python in cli script

also an interpreted coding lang like the bash script. So if you do which
python3 you get the absolute path /usr/bin/python3.

![A close up of a black and white background AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image3.png){width="3.8504483814523183in"
height="0.6406047681539807in"}

So if you change the first line our_script.sh in the nano to
#!/usr/bin/python3 , save and exit then run file our_script.sh = it will
return saying it is a python script

![](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image4.png){width="6.268055555555556in"
height="0.5534722222222223in"}

### Bash script continued

nano our_script.sh

#!/bin/bash

\--so now any commands you put into here will now we understood to be
cli commands and you can call the file from the cli and it will execute
the commands inside the bash

![](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image1.png){width="4.931498250218723in"
height="0.5955380577427821in"}

### Bash script creation

-- create a file called magic on our desktop and make 100 file and save
the metadata in another file.log

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image5.png){width="6.268055555555556in"
height="4.902083333333334in"} I did have a mistake in typing Desktop,
that's why there was an error

### Run the bash command - bash filename.sh

### Bash scripts to do backups (archive and compress)

Nano backup.sh

#!/bin/bash

![A screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image6.png){width="6.268055555555556in"
height="2.232638888888889in"}

It works perfectly but as we can see there is cases where the error
isbeing outputted to thescreen -- so we are going to take the errors and
send them to a folder where they auomatically are deleted the
2\>/dev/null and if you don't want the print out of everything being
copies you remove the v from cvzf that's all.

![](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image7.png){width="6.268055555555556in"
height="0.7326388888888888in"}

### How to make bash more efficiently 

Rather setup your bash from your home directory

Make a folder all in lowercase called bin using mkdir

Move your bash script from desktop to your bin folder

Go into your bin folder

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image8.png){width="3.711934601924759in"
height="1.759734251968504in"}

Now we need to make this so it can be run from our cli

Go change permissions of your backup.sh program to allow execute the
file as programs

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image9.png){width="1.892863079615048in"
height="1.6019925634295713in"} that's the easy way but the other way
from cli is to:

Use the chmod command to change mode/permissions of file +x means give
it executable permissions then the file name -- chmod +x backup.sh:

![A screenshot of a computer code AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image10.png){width="4.032834645669292in"
height="0.7990977690288714in"} once this happens the backup.sh turns to
a green colour to say it is executable as a script

![A computer screen shot of a computer AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image11.png){width="6.268055555555556in"
height="1.1416666666666666in"} ive added the \~Desktop/backup so it
always saves there

### Now run the bash file name as a command 

![](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image12.png){width="5.698711723534558in"
height="0.2500349956255468in"} - rename backup.sh to just backup done

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image13.png){width="6.268055555555556in"
height="1.4638888888888888in"} - when the shell says it cannot find
something it means its not on the cli search path -- edit shell search
path

Use nano .bashrc then scroll all the way to the bottom and type the
following

PATH="\$PATH:\$HOME/bin" -- variable called path = what the path
currently is then colon then home folder then bin -- so the bin folder
will be added to the path, save close cli then open again

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image14.png){width="3.637110673665792in"
height="3.1986909448818897in"}

When you open it back up again and echo the Path you will see that the
path will also search our bin folders back up script so it will be
understood by the cli

![A computer screen with white text AI-generated content may be
incorrect.](vertopal_9b793a78daa94826b57ddd1dcbdb9efc/media/image15.png){width="4.7543635170603675in"
height="2.030586176727909in"} it does it all

Now In your bin folder if you create another script eg hello and give it
executable properties and it will do your task basically creating your
own commands from the bin folder

### Difference between alias and script 

-- coz you could do this using an alias to complete the command etc. --
it would work the same because we have 1 line script. Alias is for
basically 1 command. Script is for more lines of code with if while and
loops etc. and script you can schedule using cron not aliases.

Scripts are more powerful than aliases
