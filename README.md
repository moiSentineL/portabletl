# PortableTL
Guide for making TLauncher Portable and run on USBs, etc.
---
# Edits

Edit #4: Edited Download Links

Edit #5 (25-Nov-2022): Updated the PortableTL with better batch file and TL-Directoryeditor. Comes with TLauncher 2.86.

Edit #6 (29-Dec-2023): I never thought this project would turn out to be much helpful to many of you. I glad it worked out. I am sorry for the broken links, they have been fixed now. Happy Crafting and a Happy New Year!

**Latest Edit:** And then it struck me, I could just MOVE the whole thing to a GitHub repo and never worry about it anymore. And so I moved from [this reddit post](https://www.reddit.com/r/TLAUNCHER/comments/tjc9r6/tlauncher_on_usb_final/) to here.

---
# TL;DR

You can download the premade files. But really **READ** the tutorial to know the engineering behind the files and how to use it. 

Just extract it, and run the batch file.
**Make sure** you install your own version of Minecraft in the TLauncher.

File Info = ~160MB, self-extracting exe or zip

Download them via [here](https://github.com/moiSentineL/portabletl/releases/tag/latest)

Password (if there's any): moisentinel

# Lore

On February, 2021, I made [this](https://www.reddit.com/r/TLAUNCHER/comments/lj4qg7/tlauncher_portable_on_a_usb/?utm_source=share&utm_medium=web2x&context=3) post about creating a portable TLauncher which could be run from a USB. And in the whole year, I was procrastinating about it until u/diemitchell actually gave that post a Helpful Award. I felt so guilty I knew I had to make this quick. 
So here it is, a full tutorial (created first on March, 2022) on how to create your own Portable TLauncher which you can use on pretty much anything (except on school computers which are centuries old).

# Actual Tutorial
## Pre-requisites

Let's see what we need first. 
- A computer to install the dependencies
- An Internet connection for downloading files.
- A USB Flash Drive for the portability.

Once you have it ready, we can start it out by creating a folder (which we will copy over to the drive later). Name it anything. 
To make it easier for this tutorial, I am gonna call the directory "`~/portabletl`"

## Installing jPortable Launcher

We gonna need Java to run our TLauncher and Minecraft. That's where jPortable Launcher comes in.  It can run our .jar files easily on any computer without installing anything on that computer.

We will download it from [here](https://portableapps.com/apps/utilities/java_portable_launcher "here").

 Then we will install it on the folder we made earlier for this purpose. (i.e, `~/portabletl`).
 It's going to create a directory called "`JavaPortableLauncher`" which contains the "`JavaPortableLauncher.exe`" which is the actual thingy.
 
 ## Installing OpenJDK Temurin Portable (Java 17)
  
After installing jPortable Launcher, we are going to need a Java Runtime Environment. For that, I chose OpenJDK Temurin Portable (Java 17) is needed to run the newer versions of Minecraft (1.17.1+).

We will download it from [here](https://portableapps.com/apps/utilities/OpenJDK64 "here").

To install this we're gonna have to create another directory (folder) inside "`~/portabletl`" i.e. our main folder for installing.
We're gonna need to name it "`CommonFiles`". **This is really specific.** You **GOTTA** name it that way. 
After that, run the installer and pick the "`CommonFiles`" directory as the installing directory.

## Installing TLauncher

This part is actually easy. 

Just download the official zip file from [here](https://tlauncher.org/jar) and extract it into the main folder we created at the first i.e. "`~/portabletl`".

You can delete those `README` files. We don't need 'em. Also you can rename the `TLauncher-2.8xx.jar` to something simple like `tlauncher.jar`. That's entirely optional.

## Creating Batch File (optional, but recommended)

We can create a batch file to open TLauncher easily with just a click, or go the long way and run the jPortable Launcher every time and browse for the TLauncher.jar and open it, which wastes a lot of time. And frankly, we don't have enough patience to do all of that every time you wanted to play the game and relax. 

So, to solve that, we're gonna create a simple batch file to compete that problem.

First create a text document on the main folder, i.e. "`~/portabletl`". 

Enter this code in that.

    "JavaPortableLauncher/JavaPortableLauncher.exe" "TLauncher.jar"

And don't forget to replace the `"TLauncher.jar"` I have written here with the filename of the jar you've downloaded earlier. 

And now save it as `Run.bat` or something like that. **Just don't forget to add the `.bat` after that.**

You might see a Command Prompt window whenr running it, but that goes away soon.

### Explaining the Batch File. (for the nerds. you can skip it)

The Batch file opens the `TLauncher.jar` through `JavaPortableLauncher.exe` placed inside the `JavaPortableLauncher` directory. 

## Running it for the first time.

While running the batch file for first time, you will be greeted with a "Loading libraries" by TLauncher. That's just TLauncher setting up for the first time. 

After that, you can actually see the full TLauncher. And now you can proceed by installing your favourite versions and mods (use the folder button on TLauncher.)

Don't forget to adjust the settings add some some JVM arguments for better performance of your Minecraft. 

But we still have one problem...

## Minecraft Game Directory Editing

The most annoying thing here. So, TLauncher always runs from directory it ran from last time, which means a different location. 
Let's assume you ran TLauncher from `E:` Drive for the first time. It worked well. You insert the drive onto another computer and assume it mounts as `I:`.
And now TLauncher won't know that, it will try to run from the `E:` Drive, which doesn't have the libraries for the TLauncher and will try to download AGAIN. 

To solve that, I made a program which edits the last run directory to the drive's `.minecraft` directory.
You just have to run it the first time you plug it into a computer and that session will be ready to play for you. 

To learn more, check [this repo](https://github.com/moiSentineL/TL-directoryeditor#readme) out.
**Make sure to follow the instructions written there.**

## Ending steps

Finally, copy the main folder onto your USB Flash Drive. Run the TL-DirectoryEditor,
and run the batch file and hope that it works.

## You can now use TLauncher on any computer.

### I will try my best to answer any queries regarding this. Hope you'll not get any errors. You can create an issue on this repo for any enquiries.
## Happy Crafting!
