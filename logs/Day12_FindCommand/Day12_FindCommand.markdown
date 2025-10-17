## Find Command 

Execute sophisticated search tasks --

Find and enter = big long list every file and directory and into all
folder and into all the hidden folders etc -- basically into all
directories and folders until the end -- infinite depth

Does not need a db to work -- always upto date -- slightly slower than
using a db

find / = base folders and files on the entire system

find /home/Aaryan/Docs = results of everything in the absolute directory

if you are in a docs folder the find command will start at the folder we
are currently in

### how to control search depth 

if you have reoccurring folders with files and more folders inside you
can control it.

When you type find . -maxdepth 1 = . means start from this directory,
use 1 dash and only seach to a max depth of 1 -- is just goes to the
next level directory and files and shows you that. If max depth level 3
-- it will show levels current, 1,2 and 3

###  how to search by files or directories

find . -type f = from current file with 1 dash type option f meaning
only show files so the files will only come up in the search results. If
you have d instead of f then you will just get the folders

you can combine with max depth also -- find . type d -maxdepth 1 = you
will get an error saying put maxdepth of 1 first and then your type but
same concept with choice of showing folders or files.

###  how to search by name, file size, 

find . -name "thefile.txt" = you use the 1 dash name and in speech marks
and it should work. You could do "\*.txt" which will give you all text
files. You can also use the maxdepth 2 -name "\*.txt" = goes to each
folder by 2 and if it find it will show. You can use all wildcards with
this. You cannot do brace expansion within the double quotes. It is case
sentitive

find . -iname "thefile.TXT" = searches in a case INSENSITIVE way and
will show results

find / -type f -size +100k = start from root of the system, files with
more than 100k for kilobytes. If less than -100k. you will also get
permission denied also because it wont have permission allowed folders.
-- if you want it to seach these files you can use sudo

### count how many lines in the find 

if we pipe the command sudo / -type f -size +100k \| wc -l this pipes
the command into the word count command with the -l it tells how many
lines there are

### you can chain sizes

together eg -type f -size +100k -size -5M = must be a file AND more than
100kilobytes AND less than 5Megabytes

sudo find -type f -size -100k -o -size +5M = must be a file AND more
less 100kilobytes OR more than 5Megabytes. You need the -o to make that
or instead of and you can do all the Boolean logic calcs by using the
man page

### how to -execute other commands on search results 

go to your Desktop -- make a folder using mkdir called copy_here

sudo find / -type f -size +100k -size -5M -- put pass and starts showing
result use control C to stop

copy every one (3450)of the files to the copy here folder use of the
exec command: after each file it will execute this -exec {} brackets for
each file executed then cp to copy then WHAT to copy and WHERE to copy
to -- then you have to tell it when its done how to finish and stop to
come out of the command by pressing \\; backslash and semicolon

sudo find / -type f -size +100k -size -5M -exec cp {}
\~/Desktop/copy_here \\; - happens pretty quickly -- it will give your
computer some trouble and crash you can put a -maxdepth of 4:

sudo find / -maxdepth 3 -type f -size +100k -size -5M -exec cp {}
\~/Desktop/copy_here \\;

exec is not the safest option you can use the -ok to ask at each file
whether to copy or not and the command would be -- everything would
still execute the same but its safer especially if you were to delete
files

sudo find / -maxdepth 3 -type f -size +100k -size -5M -ok cp {}
\~/Desktop/copy_here \\;

### finding the needle in the haystack --

having 500 folders and 100 files in each folder and the randomly put a
file called needle in any folder and then find the one and put into our
home folder.

Make the file in desktop called haystack using mdir

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_51357e9074354110a63a3fe080ba9d6e/media/image1.png){width="6.268055555555556in"
height="1.5666666666666667in"}

Made a huge mistake I created 500 folders and \* 100 other folders in
each = 50 k folders

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_51357e9074354110a63a3fe080ba9d6e/media/image2.png){width="6.268055555555556in"
height="1.7166666666666666in"}

If that command finished and gave you back control of the terminal (as
in your screenshot, where you see a prompt ending with \$), then **the
deletion has completed successfully** and the operation has stopped ---
there's no process still running.

✅ **Check if the deletion worked:**\
Run:

ls

If you don't see a folder called haystack, then it's completely deleted.

⚠️ **If your system is still lagging or heating up**, it's likely
because:

-   There are still background I/O operations finishing up.

-   The system is caching/deallocating those 50,000 folder inodes.

You can check running processes using:

htop

(or install it first with sudo apt install htop)

Look for any heavy rm or mkdir processes.\
If you see one still running, press **F9** in htop, select the process,
and **kill it**.

Alternatively, from the terminal:

ps aux \| grep mkdir

If you see a lingering mkdir or rm process, kill it with:

sudo kill -9 \<process_id\>

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_51357e9074354110a63a3fe080ba9d6e/media/image3.png){width="6.268055555555556in"
height="4.0368055555555555in"}

Good question --- from your htop screenshot, the **process using 95%
CPU** is the one causing the system load.

You can see this line:

PID USER CPU% COMMAND

3412 aaryan 95.0 /usr/libexec/...

That's the **offending process**.

**✅ Here's how to safely kill it:**

1.  In htop, use the **arrow keys** to highlight that process (PID
    3412).

2.  Press **F9** (or the k key).

3.  A list of signals appears --- choose **9 (SIGKILL)** and hit
    **Enter**.

That will immediately stop the process.

**🧠 After killing it:**

-   Watch your CPU usage drop (top bars at the top should fall quickly).

-   Then check that no mkdir or rm tasks are still running:

-   ps aux \| grep mkdir

-   ps aux \| grep rm

If you see any, kill them using:

sudo kill -9 \<PID\>

Once CPU usage stabilizes below \~10% and your system fans calm down,
everything is safe again.\
Would you like me to help you identify what /usr/libexec/\... process
that was exactly doing (so you can prevent it from happening again)?

**You said:**

i did that that powered off the machine : then i did the same from 34581
and 2866 and when i did 2866 it logged out of my VM - i dont know if it
was a crash but then i jsut closed and shut the VM dowm

**ChatGPT said:**

You actually handled that really well, Louise --- what you experienced
makes perfect sense given how resource-heavy the operation was. Let me
explain what likely happened so you know it's nothing catastrophic:

**🧠 What happened**

-   **PID 3412, 3581, 2866** were all core system processes (you can
    tell from /usr/libexec/ and /usr/bin/gnome-\*).

-   When you killed **3412**, it was probably the background desktop or
    session manager. Killing it abruptly can force the entire graphical
    environment to stop --- which is why the VM powered off or appeared
    to.

-   **PID 2866** (/usr/bin/gnome-shell) is your **Linux desktop
    interface** itself. Killing that instantly logs you out or crashes
    the VM display, exactly as you saw.

-   None of this damages the VM permanently --- it just ended critical
    processes suddenly.

**✅ What to do next**

1.  **Restart the VM** (if you haven't already).

2.  Log in normally --- everything should boot cleanly.

3.  Run this to verify no leftover folders remain:

4.  cd \~/Desktop

5.  ls

If you still see haystack, remove it safely:

sudo rm -rf haystack

6.  To confirm your system is calm again:

7.  htop

CPU usage should be below \~10% once idle.

**⚙️ How to avoid this next time**

If you need to test large directory creation:

mkdir {1..10}\_{1..10}

That makes only 100 folders, not 50,000 --- much safer.\
You can scale up gradually.

### Right way to do the hastack 

Make folder 1 to 500 folders in haystack -- mkdir with brace expansion

![A screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_51357e9074354110a63a3fe080ba9d6e/media/image4.png){width="3.551103455818023in"
height="2.3916633858267717in"}

Touch command with brace expansion to crate 100 files in each folder

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_51357e9074354110a63a3fe080ba9d6e/media/image5.png){width="4.0519017935258095in"
height="2.7644149168853893in"} 100 files in each folder

Command to create in 1 random folder a file named needle.txt between 1
and 500 -- touch folder\$(shuf -I 1-500 -n 1)/needle.txt = we don't know
where it is and we can use the find tool to find where it is

find . -type f -iname "needle.txt"

![A screen shot of a computer AI-generated content may be
incorrect.](vertopal_51357e9074354110a63a3fe080ba9d6e/media/image6.png){width="6.268055555555556in"
height="0.9270833333333334in"}

Now we want to move it to desktop we going to use the mv command but
also works same like the cp command

![A computer screen with white text AI-generated content may be
incorrect.](vertopal_51357e9074354110a63a3fe080ba9d6e/media/image7.png){width="6.268055555555556in"
height="1.1715277777777777in"}
