## Scheduling Bash scripts using CRON

-   <https://crontab.guru/> - cron schedule simple editor, different
    cron tab

Open terminal and type -- crontab -e -e is to edit, if its your first
time it will ask you what editor to use click 1 for nano

![A computer screen with white text AI-generated content may be
incorrect.](vertopal_f009ea02842d4fe0a28e97064ab9d7b9/media/image1.png){width="3.10336176727909in"
height="0.9523939195100612in"}

In the cron tab -- theres commented lines using \# but gives intro about
cron

Scroll to the bottom - A cron tab:

-   Each cron tab is broken up ino rows and each row is for 1 scipt or
    command to schedule

-   Each row will have 6 columns \# mins hours dom mon dow command

-   the first 5 will be schedule information the final column is the
    command or scipt to be run, there can be many spaces between the
    columns

> mins -- between 0 and 59 like a clock if you want to run every min you
> put \* for any this is the only wildcard which will work if 50 then h
> is 12 = run at 12:50pm
>
> hours -- based on 24hr clock from 0 to 23 -- if 14 then would run at
> 2pm or \*
>
> dom -- day of the month -if 1 it would only run on 1^st^ of month or
> \*
>
> mon -- 1 or JAN to 12 DEC (3 letter months In capital letters or
> numbers) or \*
>
> dow -- day of week (0 SUN or 6 SAT ) same working like mon or \*
>
> command -- eg echo "Hello World" \>\> \~/Desktop/hello.txt
>
> ![](vertopal_f009ea02842d4fe0a28e97064ab9d7b9/media/image2.png){width="6.268055555555556in"
> height="0.36944444444444446in"}
>
> ![A screenshot of a computer AI-generated content may be
> incorrect.](vertopal_f009ea02842d4fe0a28e97064ab9d7b9/media/image3.png){width="4.458955599300087in"
> height="0.729268372703412in"} the \* just means any so it selects
> random dates and times -- so whenever it does we will see

### Preference for editior

If you run ls -a to also show the hidden files -you will se
.selected_editor which contains the editior youhaev selected ie nano and
you can change it using nano

### Another cron schedule 

Mins -- you can literally have it to run every 0,15,30,45 you can have
that as your min (with no spaces). Or you can do \*/5 -- means run every
5 mins

Every 15 mins every 3 days = \*/15 \* \*/3

Only at 23:59 in only Jan and Dec on only on sun = 59 23 \* JAN,DEC SUN
echo"its almost monday"

Weekly backups at 23:59 on Fridays for every month of year :

59 23 \* \* FRI bash \~/bin/backup

On the backups lets have the backup folder bring in our home directory
In its own file named backups and edit our bash script to put it in the
backups folder

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_f009ea02842d4fe0a28e97064ab9d7b9/media/image4.png){width="6.268055555555556in"
height="1.2152777777777777in"}![A screen shot of a computer code
AI-generated content may be
incorrect.](vertopal_f009ea02842d4fe0a28e97064ab9d7b9/media/image5.png){width="2.266606517935258in"
height="0.5036898512685914in"}

![A computer screen shot of a computer program AI-generated content may
be
incorrect.](vertopal_f009ea02842d4fe0a28e97064ab9d7b9/media/image6.png){width="3.3341108923884515in"
height="2.243961067366579in"}

### Add backup to crontab

Weekly backups at 23:59 on Fridays for every month of year :

59 23 \* \* FRI bash \~/bin/backup

But we want it done every min

-   so cut the like then uncut the line then onto the next line to uncut
    the line then we can edit the second like easy copy and paste work

![](vertopal_f009ea02842d4fe0a28e97064ab9d7b9/media/image7.png){width="6.268055555555556in"
height="0.7347222222222223in"}

![A black background with green and white text AI-generated content may
be
incorrect.](vertopal_f009ea02842d4fe0a28e97064ab9d7b9/media/image8.png){width="3.0320100612423446in"
height="0.45726377952755903in"} ![A screen shot of a computer code
AI-generated content may be
incorrect.](vertopal_f009ea02842d4fe0a28e97064ab9d7b9/media/image9.png){width="2.832117235345582in"
height="0.7646106736657918in"} now we are going to wait another min to
see if it backups again

And you can check into your ![A screenshot of a computer AI-generated
content may be
incorrect.](vertopal_f009ea02842d4fe0a28e97064ab9d7b9/media/image10.png){width="3.825972222222222in"
height="0.6523567366579177in"}

So that work but updating every min not ideally were going to stop that
cron task
