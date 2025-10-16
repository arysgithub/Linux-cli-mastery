## Redirection -- Standard Output

Main use of the cat command -- to concatenate or stick together multiple
files, simple command that reads standard input (text written in) and
writes to standard output to terminal.

The control C to exit cat and get control of terminal back

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image1.png){width="4.078128827646545in"
height="1.415485564304462in"}

### How to redirect standard output to a file: 

Use the cat 1\> output.txt - (cannot have space between 1\>, can have no
space between \>output.txt) reason being that standard output is the
name of the stream that the data goes down -- and each stream has a name
and output associated with it. SO standard input has number Zero and
standard output has number 1, and standard error is number 2. So we are
redirecting or changing the direction of where the oupt is going to in
this case the file. So press enter and type your sentence and then enter
again -- it won't take you to terminal so you put control C

NOTE -- the way cat is built you don't need to put the 1 after the cat
you can just write cat \> output.txt and then complete the same
operation and it will run. -- but is important for updating other data
streams

![A close up of a logo AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image2.png){width="4.979861111111111in"
height="0.729268372703412in"} what you will find is that no output comes
to the terminal because it is saved to the file in our home folder

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image3.png){width="4.0553947944007in"
height="1.8619050743657042in"}![A white background with black text
AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image4.png){width="2.3930391513560805in"
height="0.5643952318460193in"}

### Adding more text to the file without truncating:

With truncating

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image5.png){width="4.194997812773403in"
height="1.1934820647419073in"}![A close up of a screen AI-generated
content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image6.png){width="4.281847112860892in"
height="0.9167946194225722in"} You cannot do this because redirection
the Shell will truncate everything before and empty the file and then
wrote.

Without truncating- APPENDING -- use of \>\> double arrows or 1\>\> :

![A computer screen shot of text AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image7.png){width="3.785544619422572in"
height="0.9700907699037621in"} ![A screenshot of a computer AI-generated
content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image8.png){width="2.401431539807524in"
height="0.6630818022747157in"}

## Redirection -- Standard Input and Standard Error

The data stream for standard error is 2 so you would do cat 2\>
error.txt - this would redirect the standard error from the cat command
to error.txt

To append the error to whatever is already in error.txt -- do cat 2\>\>
error.txt - you use the 2 arrows

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image9.png){width="4.229757217847769in"
height="0.6771773840769904in"} - this outputted on the standard error
data stream being terminal

![](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image10.png){width="5.948746719160105in"
height="0.5209055118110236in"}![A white paper with text on it
AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image11.png){width="1.354355861767279in"
height="1.1980839895013122in"}![A screenshot of a phone AI-generated
content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image12.png){width="4.208920603674541in"
height="1.177247375328084in"}

The error message has been sent to this location.

Best use is common LOG errors from web servers -- but the common error
is to use 1 arrow \> you should use 2 arrows \>\> so it always APPENDS
to the text file

![A screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image13.png){width="5.709130577427821in"
height="1.0105577427821522in"}

![A white text on a white background AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image14.png){width="3.6740452755905513in"
height="2.0421489501312338in"}

### Redirect standard output and standard error at the same time

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image15.png){width="6.268055555555556in"
height="0.8090277777777778in"}![A close-up of a text AI-generated
content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image16.png){width="5.771639326334208in"
height="1.1147386264216972in"}

### Standard Input from a file instead of keyboard

Create a file called input.txt

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image17.png){width="6.268055555555556in"
height="1.1833333333333333in"}

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image18.png){width="6.268055555555556in"
height="1.2222222222222223in"}

Use of the file as the input - use cat 0\< input.txt OR cat \< input.txt

![](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image19.png){width="6.268055555555556in"
height="0.5993055555555555in"}

### Combining all 3 standard input, output and error

![](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image20.png){width="6.268055555555556in"
height="0.36180555555555555in"}

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image21.png){width="6.268055555555556in"
height="1.145138888888889in"}

NOTE -- THIS ALSO ERRASED EVERYHTING WITHIN THE OUPUT AND ERROR TXT
BECAUSE OF THE USE OF 1 ARROW so remember 2 \>\> to keep all details
there

### Communicating between 2 terminals 

Open second terminal and type tty -- tells the location of the terminal

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image22.png){width="3.5960192475940507in"
height="1.6254002624671915in"}

Command to have your standard output on the second terminal which
address is the result of tty

![Screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_d4171ed26e5549aba9f7902547d97c6b/media/image23.png){width="6.268055555555556in"
height="3.0104166666666665in"}

Shows how you can use redirection to pass data across your whole
computer and across computer systems

### Summary 

-   Standard Input, Output and Error are Data Streams

-   Using redirecton, you can control where those streams FLOW

-   Standard input = 0, standard output = 1, standard error = 2

-   \> will overwrite a file before writing it

-   \>\> will append a file to what is already there

Important data sources -
<https://mywiki.wooledge.org/BashGuide/InputAndOutput?#Redirection>

<https://www.gnu.org/software/bash/manual/html_node/Redirections.html>

How would you redirect the standard output of the ls  command to a file
called output.txt  = ls \> output.txt

How would you redirect the standard output of the ls  command
to output.txt  but at the same time redirect standard error
to error.txt ? ls \>\> output.txt 2\>\> error.txt
