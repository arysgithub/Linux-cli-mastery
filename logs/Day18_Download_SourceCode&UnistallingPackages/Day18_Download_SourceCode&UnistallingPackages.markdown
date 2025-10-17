## DOWLOADING SOURCE CODE through repositories 

https://help.ubuntu.com/community/Repositories/CommandLine

run the command -- sudo nano /etc/apt/source.list.d/ubuntu.sources

you will have a config file that he system choses which files to
download

you will see there is \# for the dec-src that is the source code and all
the source code is commented out so just delte the \# save the file and
exit the nano

![A screenshot of a computer screen AI-generated content may be
incorrect.](vertopal_bb7eaa802c944ea8b016a0f441fae95a/media/image1.png){width="6.268055555555556in"
height="3.2270833333333333in"}

Next to the types add the deb-src after the deb

**🧠 Why your file looks different**

**In newer Ubuntu versions (like 22.04 and later), APT no longer uses:**

**/etc/apt/sources.list**

**for main configuration --- instead, it uses .sources files (like the
one you opened:\
/etc/apt/sources.list.d/ubuntu.sources).**

**These .sources files are YAML-like and define repositories in a
structured way --- they don't use \# deb-src lines anymore.**

**🧰 What you're seeing in your screenshot**

**Your file currently contains:**

**Types: deb**

**URIs: http://gb.archive.ubuntu.com/ubuntu/**

**Suites: plucky plucky-updates plucky-backports**

**Components: main restricted universe multiverse**

**Signed-By: /usr/share/keyrings/ubuntu-archive-keyring.gpg**

**...and similar for security updates.**

**👉 The line Types: deb means binary packages only --- no source
code.**

**To enable source code, you simply add deb-src to the Types line.**

**✅ Correct configuration (with source code enabled)**

**Edit the file again:**

**sudo nano /etc/apt/sources.list.d/ubuntu.sources**

**Then modify both sections to look like this:**

**Types: deb deb-src**

**URIs: http://gb.archive.ubuntu.com/ubuntu/**

**Suites: plucky plucky-updates plucky-backports**

**Components: main restricted universe multiverse**

**Signed-By: /usr/share/keyrings/ubuntu-archive-keyring.gpg**

**Types: deb deb-src**

**URIs: http://security.ubuntu.com/ubuntu/**

**Suites: plucky-security**

**Components: main restricted universe multiverse**

**Signed-By: /usr/share/keyrings/ubuntu-archive-keyring.gpg**

**💾 Then save and exit**

-   **Press Ctrl + O, then Enter to save**

-   **Press Ctrl + X to exit**

![A computer screen with white text AI-generated content may be
incorrect.](vertopal_bb7eaa802c944ea8b016a0f441fae95a/media/image2.png){width="6.268055555555556in"
height="2.5034722222222223in"}**🔄 Update your repositories**

**After saving, run:**

**sudo apt-get update**

![A computer screen shot of a computer code AI-generated content may be
incorrect.](vertopal_bb7eaa802c944ea8b016a0f441fae95a/media/image3.png){width="6.268055555555556in"
height="1.4256944444444444in"}

**You'll now be able to download source code using:**

![A computer screen with white text AI-generated content may be
incorrect.](vertopal_bb7eaa802c944ea8b016a0f441fae95a/media/image4.png){width="6.268055555555556in"
height="1.6409722222222223in"}

**FROM NOW ON SINCE THE DEV-SRC HAS BEEN ADDED EVERYTIME YOU WANT TO
DOWNLAOD ANY SOURCE CODE ALL YOU TYPE IS**

**sudo apt-get sources \<package name\>**

**note if you go into the source code packages and install them that way
you will lose the ability to auto install them through the package
manager.**

**So if you have the choice to install from source and package manager
-- make sure you do it throufh the repositories package manager so you
can then easily auto update when you run the sudo update etc commands**

# Uninstalling packages

To clean up everything

Sudo apt-get remove \<package name\>

-   But this is not the preferred way to do it -- coz there is config
    files will be left behind

Remove package and all its config files = sudo apt-get purge packageName

-   The purge will remove the package and the config

> ![A screenshot of a computer program AI-generated content may be
> incorrect.](vertopal_bb7eaa802c944ea8b016a0f441fae95a/media/image5.png){width="6.268055555555556in"
> height="2.2319444444444443in"}

But sometimes when you install packages they have 10+ other dependencies
that are packages that are required for that thing to work so we also
need to uninstall those:

-   To remove the dependencies package = sudo apt-get autoremove

Auto removes will auto remove any dangaling dependencies that are no
longer required

![A computer screen shot of a program AI-generated content may be
incorrect.](vertopal_bb7eaa802c944ea8b016a0f441fae95a/media/image6.png){width="6.268055555555556in"
height="3.504166666666667in"}

When you download and install a package it becomes saved locally on your
computer, that is then upacked and then stored on your system -- the 2
step process means the compressed file is just stored so need to delete
these

-   These are stored at cd /var/cache/apt/archives and do an ls

![A screenshot of a computer program AI-generated content may be
incorrect.](vertopal_bb7eaa802c944ea8b016a0f441fae95a/media/image7.png){width="3.56796697287839in"
height="2.888646106736658in"} there is quite a few deb files -- so we
need to remove them and you can do ls -lh and see how much space is
taken up.

You can be in your home directory and delete them by doing -- sudo
apt-get clean

![](vertopal_bb7eaa802c944ea8b016a0f441fae95a/media/image8.png){width="4.095138888888889in"
height="1.0270833333333333in"} If you only want to get rid of only
archives that can NOLONGER be accessed by the ubuntu systems -- you use
the sudo apt-get autoclean = so only deletes the ones you can no longer
download from the ubuntu repositiories

<https://help.ubuntu.com/community/Repositories/CommandLine>
