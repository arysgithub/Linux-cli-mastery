## Deleting Files and Folders

### Rm command to delete files and with wildcards 

Create file called deleteme using touch

![A screen shot of a computer program AI-generated content may be
incorrect.](vertopal_af4d7f78848b4d5898fee3a96f0b999d/media/image1.png){width="3.5700667104111985in"
height="1.1040212160979876in"}

Remove - rm -- then give it absolute or relative paths to delete a file

rm deleteme = deleted

![A computer screen shot of a computer code AI-generated content may be
incorrect.](vertopal_af4d7f78848b4d5898fee3a96f0b999d/media/image2.png){width="3.575097331583552in"
height="0.6365146544181978in"}

Deleteme in Docs folder use rm and absolute path to delete anywhere it
will be deleted

You can delete multiple files in one line even if the first is just the
relative path, the second is an absolute path and the 3^rd^ is an
absolute path

rm \*.txt = delete all files that end in .txt

rm file\* = delete any file that starts with file

rm \*2\* = removes all files with the number 2 in them

rm \*\[2,3\]\*= remove all files with the number 2 or 3 in them use of
\* and \[\]

### Deleting files and folders using rm and rmdir

Create a folder in home directory called -- mkdir delfolder

Remove the folder = rm delfolder = cannot remove a directory

Unless we give the rm option the -r = to delete it recursively

rm -r delfolder =this will delete the directory

### Now lets try this with brace expansion to create folders

![](vertopal_af4d7f78848b4d5898fee3a96f0b999d/media/image3.png){width="5.277237532808399in"
height="0.5946095800524934in"}

Now create files in the folders using brace expansion

![](vertopal_af4d7f78848b4d5898fee3a96f0b999d/media/image4.png){width="5.27330271216098in"
height="0.35696741032370954in"}

Lets try delete the folder with many other folders and files:

![A screen shot of a computer program AI-generated content may be
incorrect.](vertopal_af4d7f78848b4d5898fee3a96f0b999d/media/image5.png){width="3.0223140857392825in"
height="1.1046555118110237in"} and this is completed once you delete the
folder with rm -r delfolder/

You should be careful to not use the rm -r \* because that will delete
all your files

So you should use the -ri = recursively interactive -- which means it
the rm command will ask you if youd want to actually delete them

Lets try it with the -ri = so create the folder and other subfolders
with expansion -- mkdir -p delfolder/deleteme{1,2,3} then recreate the
files

So with our files back -- try delete everything: with ri

![A screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_af4d7f78848b4d5898fee3a96f0b999d/media/image6.png){width="3.276748687664042in"
height="2.0159306649168856in"}

### Remove empty files - rmdir

3 folders and 2 folders with 10 files

![](vertopal_af4d7f78848b4d5898fee3a96f0b999d/media/image7.png){width="6.268055555555556in"
height="0.6in"}

So folder 3 is completely empty -- rmdir delfolder/\* = remove the empty
files

![A computer screen shot of a program AI-generated content may be
incorrect.](vertopal_af4d7f78848b4d5898fee3a96f0b999d/media/image8.png){width="6.268055555555556in"
height="1.5583333333333333in"}

So folder 3 is removed -- reason why it removed 3 is because er had
delfolder/\* means the all folders within the delfolder. But if you had
just delfolder then it would return cannot remove delfolder

Delete all the 100s of files for the 2020 to 2025 years all in one
command

![A screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_af4d7f78848b4d5898fee3a96f0b999d/media/image9.png){width="6.268055555555556in"
height="0.9201388888888888in"} all deleted
