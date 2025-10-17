## Viewing files - 

5 new commands to manipulate file contents

### Cat command refresher 

cat file1.txt -- will output the result to the screen and you can use it
to stick together files like cat file1.txt 2.txt 3.txt 4.txt 5.txt
\>total.txt = stores all the text from 4 files into 1

you can use wildcard make easier -- cat file\[1-5\].txt \> total.txt

useful for audio or mp3 files -- and concatenate together to create one
long file

### tac command 

cat spelled backwards to reverse whatever is put into it. Remember \>\>
2 arrows appends to a file rather than overwrite it

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_2f66a81a305b47e2a0a32ee6492d3083/media/image1.png){width="5.035415573053369in"
height="1.9302613735783027in"} tac doesn't change the letters but makes
the first line last and the last line fist. It basically flips it upside
down --

also you can pipeline the cat into the tac - cat file\[1-5\].txt \| tac
\> reversed.txt

eg paying songs backwards hidden messages -- mp3 file will be reversed
vertically

### rev command

reverse the content on each line eg hello = olleh on the same like
-reverses a file horizontally

same like cat and tac works exactly the same way in typing, you can even
pipeline through it -- you can pipeline through rev and tac to scramble
the data if needed

### pager programs to page through large output to make it easier to read

less is a pager you type the file name and you can scroll up and down to
read a file and if you type Q then it closes

less text1.txt or you can use cat to open the file and then pipe it to
less it doesn\'t matter

also works for like the find feature -- and we pipe it into less and we
can scroll easier line by line using up and down arrow keys

### peak at little piece of a file -- like a filter tool

head and the tail commands

head -- see little piece of the file at the top /head and vice versa for
tail

head command by default shows you first 10 lines of a file -- but you
can change it using it the -n option

you can do head -n 20 absolute path name and it will give you rhe
results

or you can pipeline it

eg cat text2.txt \| head -n 2 -- shows the first 2 lines

find \\ \| head -n 5 = shows the first 5 results

you can pipeline to the wc -l to count the amount of lines to make sure
its done correctly

tail shows the bottom 10 and works the exact way the head does using the
-n etc

you can take the head 20 lines and pipeline to the tail and get the last
3 lines from the head

come into the real use :

-   find \| tail-n 3 \> export.txt etc like a filter tool

## Sorting files and Data 

### Sort letters

To sort a file asc alphabetically -- sort nameoffile.txt = sorted words
A to Z

And you can write to a file and then pipeline it etc

Sort dec- sort the words normally and then pipe to the tac command- sort
nameoffile.txt \| tac

OR

Sort -r words.txt = -r means to reverse

You can pipe to the less command to make it easier to use in scrolling
up and down the file

### Sorting numbers

Sort numbers.txt -- it doesn't do it nicely -- it sorts by the first
digit, not the full number value XXXXXX wrong way

Give the sort -- n number.txt = give the sort the numeric ability

Sort dec -- srt -nr number.txt

### Sort - Only show unique results not repeated 

Give the sort the -u for unique = sort -u numbers0-9.txt

Sort dec = sort -ur unique.txt

### Sort Data in Tables up and down columns

Ls -l /etc = get a lot of data out of this command etc is all system
config files pass into the head and get first 20 lines

### Sort -k = by certain columns eg file size or date :

Ls -l /etc \| head -n 20 \| sort -k 5 = after the k you need to tell it
how to do it -k ColumnNumber. Then if you wanted it numberically it
would bt 5n. if you wanted reversed it would be 5r. numerically reversed
5nr. N=unique = 5u

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_2f66a81a305b47e2a0a32ee6492d3083/media/image2.png){width="3.6698687664041993in"
height="2.255346675415573in"} you can see column 5 after root the file
size is sorted and if you have it in

ls -lh it gives In human readable format -- when sorting numerically but
with human readable data it doesn't sort unless you change the 5n to a
5h and then it will recognise the human and the numbers and I made it
5hr to reverse and make it interesting

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_2f66a81a305b47e2a0a32ee6492d3083/media/image3.png){width="2.9702930883639547in"
height="1.4884372265966754in"}

### Sort by date/ month 

Ls -lh /etc \| head -n 20 \| sort -k 6M = sort by month in the date
column from Jan to Dec

You can have 6Mr also for reversal

Order of the Mr or rM doesn't matter even for above

### Search Data -- grep command 

Grep .end file name = gives you the metadata of the file woth the
creation data the date last edited the total space

![](vertopal_2f66a81a305b47e2a0a32ee6492d3083/media/image4.png){width="6.268055555555556in"
height="0.4076388888888889in"}

### What grep does

grep stands for **Global Regular Expression Print**.\
It searches **text** for **patterns** --- words, phrases, or expressions
--- and prints the matching lines.

Think of it as your **"Ctrl + F" for the Linux terminal**.

### ⚙️ Basic Syntax

grep \[options\] \"pattern\" \[file\]

**🧩 Common Examples**

### 🔍 1. Search inside a file

grep \"error\" logfile.txt

Finds every line in logfile.txt that contains the word "error".

### 📂 2. Search recursively in a directory

grep -r \"main\" /home/user/projects

Searches all files under /home/user/projects for "main".

### 🔠 3. Ignore case

grep -i \"warning\" system.log

Finds "warning", "Warning", or "WARNING".

### 📊 4. Show line numbers

grep -n \"class\" mycode.java

Shows the matching line *and* its line number.

### 🔁 5. Combine with other commands (super powerful)

You can pipe (\|) another command into grep:

ps aux \| grep firefox

Finds all running processes related to "firefox".

**💡 Quick Tip:**

You can highlight matches automatically with:

grep \--color=auto \"pattern\" file.txt

**🧩 Bonus --- Inverse search**

grep -v \"DEBUG\" log.txt

Shows all lines **that do NOT contain** "DEBUG".

In short:\
✅ grep = find text fast\
✅ Works in files, logs, or command outputs\
✅ Combine with pipes for real power

Would you like me to show you **5 practical DevOps uses of grep** (e.g.,
finding config errors, scanning logs, checking processes)?

### **5 real-world DevOps use cases** where grep becomes one of your most-used tools:

#### ⚙️ 1. Find errors in logs instantly

When working on servers, you often need to find issues fast.

grep -i \"error\" /var/log/syslog

🔹 Finds any line containing "error" (case-insensitive) in the system
logs.\
🔹 Add -A 3 or -B 3 to see 3 lines *after* or *before* each match for
context:

grep -i -A 3 \"error\" /var/log/syslog

💡 **Use case:** Quickly diagnose crashes or failed service starts.

#### 🧩 2. Check if a process is running

Instead of scrolling through ps output manually:

ps aux \| grep nginx

🔹 Finds all processes related to "nginx".\
🔹 The first match might be the process itself; the second is your grep
command --- you can filter that out:

ps aux \| grep \[n\]ginx

💡 **Use case:** Confirm if a service like MySQL, Nginx, or Docker is
active.

#### 🧠 3. Search through configuration files

You might need to find where a variable or port is defined:

grep -r \"PORT=8080\" /etc/

🔹 Searches recursively through /etc/ for configuration lines containing
PORT=8080.

💡 **Use case:** Useful for debugging wrong environment variables or
port conflicts.

#### 🔐 4. Check for secrets or keys in code

Before pushing code, make sure you're not leaking sensitive info:

grep -r \"AWS_SECRET_ACCESS_KEY\" .

🔹 Searches your project directory for accidental secrets.

💡 **Use case:** Helps enforce security hygiene before commits or
deployments.

#### 🧰 5. Filter logs during deployment

Combine grep with tail to monitor deployments or container logs live:

tail -f /var/log/app.log \| grep \--color=auto \"ERROR\"

🔹 Streams live logs but highlights only lines containing "ERROR".

💡 **Use case:** Watch your app deploy and instantly see errors without
the noise.

**🚀 Summary:**

  -----------------------------------------------------------------------
  **Command**                              **Purpose**
  ---------------------------------------- ------------------------------
  grep -i \"error\" file.log               Find errors (case-insensitive)

  \`ps aux                                 grep \[n\]ginx\`

  grep -r \"PORT=8080\" /etc/              Find config variables

  grep -r \"AWS_SECRET_ACCESS_KEY\" .      Detect leaked secrets

  tail -f app.log \| grep \"ERROR\"        Monitor live logs for errors
  -----------------------------------------------------------------------

Would you like me to make a **cheat sheet image (CLI quick-reference)**
of the most powerful grep commands for your Linux + DevOps study notes?
