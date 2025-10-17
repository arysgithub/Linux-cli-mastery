## Locate command -- search for commands anywhere 

epending on what distribution you are running the locate command may not
come pre-installed. Ubuntu 20.04 appears to have this issue, for
example, but Ubuntu 18.04 does not.

If you find you are having issues, try installing the locate 
and mlocate packages from your repositories.

sudo apt install locate

sudo apt install mlocate

That should do the trick!\]

### How use locate

It works by searching a database file on your system -- search for any
path that matches that option and gives a standard output

Locate \*.conf = check for all files ending in .conf = result including
file paths ending in .conf

Locate .log = log files with error messages, servers

### Linux is case sensitive -- to remove the sensitivity, use the locate -I command 

Locate -I \*.CONF = return all ending in conf

Locate -I --limit 3 \*.CONF = limit results to 3

Locate -S = gives up information about the database and its complexities
and directories, bytes and stored database

And you can use \> to redirect put data in folder

Locate -e \*.config = check to see if those files from the DB is
existing so cannot dlete

Locator - - follow/-- checks if links still valid

### Update the database in the cli using updatedb command

Gain superuser privileges using sudo command -- run admin commands

Updatedb to locate commands to give accurate results

Create a new file called find me in desktop using touch command

Try run the locate command it wont find it because it hasn't been
entered into the db

We need to update the db -- using updatedb

We will receive an error because the shell updatedb doesn't have admin
access -- you can use man to recheck

Use the sudo command as -- sudo updatedb

And then you will be required to enter your password to your laptop --
you wont see your password being typed out -- it is a safety feature

-   If correct the db will be updated -- ie the shell db and now you can
    locate the file

If you type locate findme.txt and it will bring out the absolute path

Locate -S = it will locate the db and showcase how many directories and
file and how much bytes are being used . you can also use the \> to save
the text into a file

The size of the files continuously changes

Locate --existing --follow = the existing and follow options exist so
that when you waiting for the admin to do their stuff you can continue
doing some work.

### Limitations of locate command 

-   It uses the locate command in order to function

-   You create a new file called important.txt  but it has been 2 hours
    since your locate  database has been updated.  - Will
    the locate  command be able to find important.txt ? -- no because
    the is impossible for the locate command to find it if the file is
    not entered in the db

> ![A screenshot of a computer AI-generated content may be
> incorrect.](vertopal_7fbb2822a987486884754a81ddf59c90/media/image1.png){width="6.268055555555556in"
> height="1.7854166666666667in"}
