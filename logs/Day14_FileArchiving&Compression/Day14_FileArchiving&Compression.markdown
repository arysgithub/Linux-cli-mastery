## File Archiving and Compression -- to create backups and restore

Our tarball is our archive Creating a tarball -- putting your files in
one place to make it easier to store- TARBALLS ARE CONTAINERS TO STORE
FILES IN FOR COMPRESSION

Archiving -- 1) make tarball (JUST CONTAINS FILES) 2) compression

First make a tarball -- tar command

Tar command then give 3 options -c to create a new archive then v to
speak to us ad talk to us (optional) f it lets tar command accept files
then tell what we want to call the files.tar and what to put into the
tarball

Tar -cvf ourArchive.tar file\[1-3\].txt

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_c06fa03a05e145dc8edb657a1b120f68/media/image1.png){width="6.268055555555556in"
height="2.9875in"}

In order to create a tarball, there is extra data so the total file will
be bigger than the files on their own before compression.

![](vertopal_c06fa03a05e145dc8edb657a1b120f68/media/image2.png){width="6.268055555555556in"
height="0.4076388888888889in"}

file extension in Linux don't really mean anything and can be changed
its for humans convience to double check it's a proper tar file use the
file and ourArchive.tar and it should give the data

![](vertopal_c06fa03a05e145dc8edb657a1b120f68/media/image3.png){width="6.268055555555556in"
height="0.5715277777777777in"} it is a real tar archive even if you
change to a random extension the linux wouldn't be affected and would
understand the true nature.

### How to extract the details of the tar command to see them and check whats inside

Use tar -tf ourArchive.tar = t is for test label and check what\'s
inside f is for file = gives the names of the files inside

### Deleted our files but still have our archive of tar how to extract files back

tar -xvf ourArchive.tar = x for extract and the remainder is the same
and it will exract them back to the directory you ran the command.

When extracted, is the tarball empty?? NO -- the files are still inside
the tarball -- it never leaves unless you delete them

### Compress Tarball to make smaller and save space on our HDD

2 compression algos on Linux system -- gzip bzip2

Gzip -- faster, less compression power

Bzip2 -- more compression size smaller, but more compression power

gzip ourArchive.tar = compressed in place and the result will have
ourArchive.tar.gz

![A screen shot of a computer screen AI-generated content may be
incorrect.](vertopal_c06fa03a05e145dc8edb657a1b120f68/media/image4.png){width="6.268055555555556in"
height="1.3569444444444445in"}

The file size reduced - ![A screenshot of a computer AI-generated
content may be
incorrect.](vertopal_c06fa03a05e145dc8edb657a1b120f68/media/image5.png){width="2.318076334208224in"
height="0.962311898512686in"}

### HOW to reverse gzip

gunzip ourArchive.tar.gz = unzips the gzip and you can run the ls and
file

### how to bzip2 -- used on large files eg videos 

bzip2 ourArchive.tar = will have a .bz2 info

to unzip use = bunzip2 ourArchive.tar.bz2

![A computer screen shot of a computer program AI-generated content may
be
incorrect.](vertopal_c06fa03a05e145dc8edb657a1b120f68/media/image6.png){width="4.126501531058618in"
height="1.4730314960629922in"}

### Other compression algo 

Xz algo

### How to create zip files

Not as compressed as gzip or bzip2

Its simple tho -- zip testing.zip file1.txt 2.txt 3.txt

![A screenshot of a computer AI-generated content may be
incorrect.](vertopal_c06fa03a05e145dc8edb657a1b120f68/media/image7.png){width="4.018734689413823in"
height="0.6491590113735783in"} the zip is what you can use on other O/S
by default and to

Unzip -- you just unzip testing.zip and then just agree to unzip

### Create archive and compression In one command 

Raw files to compressed archive In 1 go

Gzip:

Tar -cvf ourArchive.tar file\[1-3\].txt and to do it with gzip
compression -- cvzf and add .gz manually to tar so = Tar -cvzf
ourArchive.tar.gz file\[1-3\].txt

And you can check with the file

Bzip2:

Tar -cvf ourArchive.tar file\[1-3\].txt and to do it with bzip2
compression -- cvjf and add .bz2 manually to tar so = Tar -cvjf
ourArchive.tar.bz2 file\[1-3\].txt

### Extract archive and compression In one command 

Gzip:

Tar -xvf ourArchive.tar.gz - so all you have to do is add the z to xvzf
and done

For bzip2:

Tar -xvjf ourArchive.tar.bz2

Link -
<https://www.rootusers.com/gzip-vs-bzip2-vs-xz-performance-comparison/>
