## Aliases

Aliases- easy-to-remember nicknames names with shortcut of your commands
eg pipeline etc to make CLI easier.

### Create a file called .bash_aliases in your home folder

Click activities in the top left of Ubuntu VM -- and search text and
open up text editor -- save it and name .bash_aliases -- we needed to
name the file with a full stop to make the file a hidden file

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image1.png){width="4.457024278215223in"
height="2.2936931321084866in"} you can see them if you click on hidden
folders that are already there:

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image2.png){width="3.8492661854768153in"
height="2.6564457567804025in"}

### Make an alias in the file you jut created: alias aliasname = '...'

Were going to name out alias getdates and works like so

alias get dates = 'date \| tee /home/aaryan/fulldate.txt \| cut --
delimiter =" " \-- fields =1 \| tee /home/aaryan/shortdate.txt \| xargs
echo hello'

then click save and close

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image3.png){width="6.268055555555556in"
height="1.3173611111111112in"}

When we reboot our terminal, that alias should be reloaded

### Think of the aliases as being your own commands in Shell

Ie get dates will return hello Sat - ![A black background with green
text AI-generated content may be
incorrect.](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image4.png){width="4.031812117235345in"
height="0.7917771216097987in"}and the files will be created

![A close-up of a computer AI-generated content may be
incorrect.](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image5.png){width="1.7419969378827647in"
height="0.7616174540682414in"}![A screenshot of a phone AI-generated
content may be
incorrect.](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image6.png){width="2.722374234470691in"
height="0.6805938320209973in"}![A screenshot of a phone AI-generated
content may be
incorrect.](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image7.png){width="1.6300415573053368in"
height="0.5237073490813648in"}

Instead of tyoing out that really long command we can just call the
alias using the alias name which has our saved command

### We can use aliases in bigger pipelines aswell

If the first command in your alias can accept standard input -- then you
can just pipe to the alias and run the whole pipeline and then pipe out
of the alias and carry on.

Create a new alias in your bash alias file and write your command:

Were going to be using the cal argument but it only accepts command line
arguments ![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image8.png){width="4.4308923884514435in"
height="1.3440923009623797in"}

![](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image9.png){width="6.268055555555556in"
height="0.44583333333333336in"}

Reboot the terminal.

My command was not executing
![](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image10.png){width="6.268055555555556in"
height="0.6465277777777778in"} because I forgot that accurate spelling
is important but once done that

![A white paper with text AI-generated content may be
incorrect.](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image11.png){width="1.0313943569553805in"
height="1.0522298775153105in"} weve managed to save the contents into a
file using our alias

![A calendar with numbers and letters AI-generated content may be
incorrect.](vertopal_6f979a1f7f7340359a9224837e210ffc/media/image12.png){width="6.268055555555556in"
height="2.6777777777777776in"}

We passed to the xargs information 2 arguments 05 and 2021 into the cal
-- calendar command and it runs the pipeline. This will work. And we
embedded a standard output saving to a file.

### Summary 

-   An alias is a custom nickname for a command or pipeline

-   Aliases go in a .bash_aliases file in your home folder

-   A period at the start of a file name makes the file hidden

-   alias aliasname = "commands/ pipeline" - can be single quotes or
    double quotes

-   aliases are accessible only when you restart your terminal

-   MAKE SURE THE FIRST COMMAND CAN BE PIPED to in the PIPELINE
