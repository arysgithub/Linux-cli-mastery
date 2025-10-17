## File Extensions in Linux 

File extensions give you what file your dealing with at a glance. Png is
an image txt is a text file

### File command -- 

eg file finename.txt -It will tell you the filename, what kind of file
it its, the metadata

![A screen shot of a computer program AI-generated content may be
incorrect.](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image1.png){width="6.268055555555556in"
height="1.0798611111111112in"}

If I rename the bmw etc to a pdf and try again lets ee the result

![A screen shot of a computer code AI-generated content may be
incorrect.](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image2.png){width="6.268055555555556in"
height="0.9215277777777777in"}

Linux read te header of the file but still saw it was a JPEG -- if you
try open it you get an error because the pdf file reading system cannot
read the pdf because it is a jpeg. The content is different but the
program got tricked and saw the file name and thought it was a pdf.

If you put a .dsadad file extension, the software doesn't know it so it
will just open it as a jpeg because it knows it's a jpeg but if you had
a .txt it would not work. -- you cannot do this in any other system

## Wildcards 

-   Eg really messy desktops -- want to mover everything around and make
    really specific and generic commands that will be used in cli to
    adjust your output

-   Wildcards are used to build patterns called REGULAR
    EXPRESSIONS(patterns that a piece of text needs to match)

Ls command to show multiple folders

Ls Douments/ Downloads/ Pictures/

![A screen shot of a computer AI-generated content may be
incorrect.](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image3.png){width="3.3425667104111985in"
height="0.8613790463692038in"} but with wildcard you can do list or copy
or remove files with .pdf or that start with r

### STAR \* WILDCARD 

This command will basically match any piece of text or numbers basically
anything= ls \*

![A screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image4.png){width="3.3633530183727034in"
height="2.3870636482939633in"}

Ls D\* - the pattern is the D then the star

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image5.png){width="2.4391174540682417in"
height="1.0425251531058617in"}

Ls \*.txt

![](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image6.png){width="6.268055555555556in"
height="0.45902777777777776in"}

### ? wildcard

This will only match anything but with just 1 placeholder or character

![A close up of a number AI-generated content may be
incorrect.](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image7.png){width="5.93832895888014in"
height="0.739686132983377in"}

If we did ??.txt -- it would match A1.txt 66.txt etc

![A close up of a logo AI-generated content may be
incorrect.](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image8.png){width="4.323520341207349in"
height="0.531324365704287in"}

### \[ \] wildcard

Allow pattern to be more specific and only match letters or numbers for
given spec

Ls file\[1234567890\].txt -- will give us results from a file with any
or fiven number over there for the numbers so if you had fileA.txt it
would not show up

![A black background with white text and symbols AI-generated content
may be
incorrect.](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image9.png){width="5.625785214348206in"
height="0.718850612423447in"}

![A black background with green and blue text AI-generated content may
be
incorrect.](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image10.png){width="5.125715223097113in"
height="0.8334492563429571in"}

Ls file\[0-9\]\[0-9\].tx -- will result with 2 digit numbers

Ls file \[a-z\]\[0-9\]\[A-Z\].txt -- will result with lowercase then
number then uppercase

Ls file \[0-9ABC\] will return all with numbers or A or B or C as first
characters

Which of these regular expressions would match these files: \
important_report1A.pdf , important_report1B.pdf , important_report1C.pdf

![A close up of a text AI-generated content may be
incorrect.](vertopal_3674202a68f04ffbb52933ee7f6466ba/media/image11.png){width="6.268055555555556in"
height="1.1583333333333334in"}

Many more other wildcards -
<https://tldp.org/LDP/GNU-Linux-Tools-Summary/html/x11655.htm>

how to use wildcards - <https://www.linfo.org/wildcard.html>
