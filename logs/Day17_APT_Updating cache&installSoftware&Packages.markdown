## APT package manager

The cli tool deals with all the packages and it is called APT package
manager -- this gets the new software for you.

### Search for packaging using apt 

Apt-cache search docx -- searches the package manager for all the
packages that end in docx for word file and we get a short description
about the packages

To be more specific with your search you could pipeline the result of
that into grep text to get the files that deal with text -- ie Apt-cache
search docx \| grep text

Apt-cache show filename.txt to get a whole more information about the
file and you can pipe into less so you can easilt understand and scroll
through

### If you were to turn off the WIFI with your VM 

Apt-cache search "web server" \| less = we actually get results without
web connection

Apt-cache search apache2 = give us the info without internet connection

Its still working without WIFI so it is in fact stored on our computer
in the CACHE.

CACHE -- a storage place locally for frequently used data for better
performance that's why we use the -cache so it looks inside the cache
for the results

### Where is the cache located 

In ubuntu its at /var/lib/apt/lists

These re all the packages of the packages on the system that you can
have installed

You can see that the requests for the files is
gb.archive.ubuntu.com....... -- this means its just got the data from
the data centre closer to you.

It will also state the type of Ubuntu repositories used from the source

If you use pipeline less -N will number the pipeline

## Updating the Cache and Upgrading the software

The contents in the cache are from the contents on the server --

### Update the cache -Sudo apt-get update 

= to update your file system in your cache to make sure the package
system in chache and the server repositories are the same

### Update ALL software - sudo apt-get upgrade 

Tells you what is out of date and what need to be update and everything
and when you give it permission it will then do that for all software on
the whole system. \# it is way easier than mac or oS or windows where
you have to go to sites, download and run wizards to update etc...

You can use cron to schedule this regularly

MAKE SURE YOU UPDATE THE CACH EBEFORE YOU UPGRADE SOFTWARE SO THAT
EVERYTHING IS UPTO DATE AND IF YOU CAN MAKE SURE THAT IT IS REPOSITIORIE
OF UBUNTU SO IT IS EASILY UPDATABLE.

## Installing new Packages

Apt-cache search nameetc

Then apt-cache show nameetc \| less - to show you more details about
your search results and then you can read through to make sure it is the
package you want to install

Then run the sudo apt-get install namesetc (using apt-get to get data to
get data from the internet) -- installs the new dependensies

Then the package is installed.

Most packages are binary -- pre compiled into machine language for the
OS ready to run

Now you can type the command name nameetc and it will run and the maeetc
will even have its own man page

If you type xman instead of man for the manual pages you will get a pop
up gui of the man page to search. Hold down mouse to show the drop down
options and sections etc. -- and then click to open up the command and
its data
