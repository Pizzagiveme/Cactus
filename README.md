## Cactus <img src="https://i.imgur.com/mSwZJmr.png" height="35"/>
##### By: Jonathan Vasquez (fearedbliss)
##### Build: 2022-11-09-1230
##### [The Moving Caravan](https://themovingcaravan.com/) - A Diablo II Time Traveling Community (1.00 - 1.10) ([Videos](https://www.youtube.com/channel/UCxkGpI6vroZC7E10fRHAHiA))

## Screenshots

### Light Mode
![Cactus](https://i.imgur.com/7jEsddV.png)

### Dark Mode
![Cactus](https://i.imgur.com/n0YT7su.png)

### Out Of The Box Experience
![Cactus](https://i.imgur.com/gihWXVu.png)

### Settings (19 Material Design Colors Available + Light/Dark Mode)
![Cactus](https://i.imgur.com/sifWwiV.png)

### Add Entry
![Cactus](https://i.imgur.com/gD4Nptz.png)

### Edit Entry
![Cactus](https://i.imgur.com/N6OLOHC.png)

## Download

The version switcher source code can be downloaded at the [Cactus (Core)](https://github.com/fearedbliss/Cactus-Core) repo.

The Cactus Bundle is no longer available on GitHub since I want to provide a direct download location from my server (uptime is not guaranteed). [7-Zip](https://www.7-zip.org/download.html) must be
used to extract the archive since I'm using high compression. All releases are
hashed and PGP signed with the key: **`34DA 858C 1447 509E C77A D49F FB85 90B7 C4CA 5279`**,
which can be easily found at the link below. 

### [Download Cactus](https://xyinn.org/diablo/Cactus.7z)
### [PGP Public Key](https://keys.openpgp.org/search?q=34DA+858C+1447+509E+C77A+D49F+FB85+90B7+C4CA+5279)
### [Latest Release Hash](https://xyinn.org/diablo/Cactus.7z.SHA256.txt)
### [Latest Release Hash Signature](https://xyinn.org/diablo/Cactus.7z.SHA256.txt.sig)

## Description / History

Cactus started out as just a simple application that allowed you to 
easily and efficiently Time Travel between every version of Diablo II 
that ever came out, while maximizing disk space and enabling full 
character isolation between versions. However, even though Cactus itself 
still is just that, the Cactus Repository has evolved to become a 
centralized and historical archive, that aims to preserve every single 
Diablo II version that exists (**`Official Retail`** and **`Official Beta`** 
Releases). Cactus is a complete rewrite from scratch of my previous 
application called: **`Bliss Version Switcher`**. However, since Cactus is 
written in C#, it behaves as a native Windows application and allows it 
to integrate natively with the system. On the other hand, Bliss Version 
Switcher was written in Java and thus there were many limitations that 
lead to the Cactus rewrite.

This repository also includes several other utilities that I have either 
created or collected, which can help you play **`Vanilla`** Diablo II 
better. All Cactus Platforms are **`Vanilla`** by default. The only fix 
I made to all Platforms below **`1.12`** is to remove the CD requirement, 
since modern computers no longer have a CD drive (Blizzard already did 
this exact thing for **`1.12+`**). Other than that, the only other
modifications I provide are through **[`Singling`](README-SINGLING.md)**,
which only contains **`non-gameplay modifications`** and is
**`completely opt-in`**.

Furthermore, if you will be playing online, you should make a copy of 
the Vanilla Platform and use that one to connect to Battle.net (for 
example, copying the **`1.14d`** platform and calling it something like 
**`1.14d BNET`**). You can use your other platforms with the Singling
changes for local play.

Lastly, the **`cnc-ddraw`** video renderer and **`3D Sound`** support 
are included. **`cnc-ddraw`** is provided to improve video compatibility 
for all versions between **`1.00 - 1.13d`**. Blizzard removed 
**`DirectDraw`** support starting with **`1.14`**, and thus Cactus will 
only provide video support for versions before that. While the **`3D 
Sound`** support is provided to enable you to use the following lost 
in-game sound functionality: **`3D Sound`**, **`Environmental 
Effects`**, and **`3D Bias`**. 

Cactus requires a purchased copy of Diablo II **`(Original, Not Resurrected)`**
from Blizzard in order to have all of the game assets stored in the 
MPQs. Once you have these, they will be reused for all Cactus 
Platforms. 

For further information, please read the documentation below for 
anything you are interested in exploring.

## Cactus Repository

The following opt-in modifications and utilities are available in this repository:

#### [Singling](README-SINGLING.md)

A collection of non-gameplay modifications and fixes in order to improve the
Vanilla Diablo II Single Player & LAN Experience.

To use Singling, simply copy the Singling files for the version you want to
play from the **`2. Singling/1. Files`** folder, and replace the ones for
the equivalent version in your Platforms directory. To revert, use the files
in **`2. Singling/2. Stock`** instead.

#### [Renderers](README-RENDERERS.md)

Cactus includes and promotes the **`cnc-ddraw`** video renderer for 
Diablo II versions **`1.00 - 1.13d`**, which can help you run the game 
on newer systems with a higher window resolution (not a higher internal 
resolution), and the ability to use shaders to upscale the quality of 
the graphics in the game. Since Blizzard removed **`DirectDraw`** 
support in **`1.14+`**, you'll need to find an alternative video 
renderer for those versions. 

Please read the [**`README-RENDERERS`**](README-RENDERERS.md) for 
further explanation on this, for information on how to set it up, or for 
any known technical limitations. Definitely read the 
**`Recommendations`** section at least, or you will most likely 
encounter crashes if you've never played versions before **`1.14`** 
before. Blizzard has done major changes with how video configuration 
works starting in **`1.14`**. 

- [**`cnc-ddraw`**](https://github.com/CnCNet/cnc-ddraw) - This renderer
  reimplements the DirectDraw API for GDI, OpenGL, and Direct3D to improve
  compatibility with Windows XP - 10, and Wine. This renderer also supports
  the use of custom shaders - which will allow you to upscale the game so it
  looks a lot better - and even provides hotkeys (such as **`[Alt] + [Enter]`**)
  to switch between full screen and window mode.

##### [3D Sound (DSOAL w/ OpenAL Soft)](README-3D-SOUND.md)

Cactus includes the files required to allow you to enable the following 
lost in-game sound functionality: **`3D Sound`**, **`Environmental 
Effects`**, and **`3D Bias`**. 

Please read the [**`README-3D-SOUND`**](README-3D-SOUND.md) for more information.

## License

Released under the **[Simplified BSD License](LICENSE.txt)**.

## Requirements

- **.NET Framework 4.6.2 +**

## Installation Instructions 

### Installation Video

- **[Short Version (Recommended) (Cactus 2.4.1+) (29 Minutes)](https://youtu.be/kAFfc-kjTxE)**

### Install Cactus And Prepare MPQs

This section will help you install Cactus to the correct location and also help you
fix your MPQs so that they are compatible with the older versions of Diablo II.

**`Note:`** This fix is only needed if you want to play versions **`1.08 - 1.13d`**,
   if you are not planning to play those versions, you don't need to fix your MPQs.
   
1. Copy all of the files in the **`1. Files`** folder into your **`Diablo II Root Directory`**.

   **`Note:`** It's important that **`Cactus`** runs from inside your **`Diablo II Root Directory`**
   or you will get weird behavior in various situations like running **`-direct -txt`** mods or
   taking screenshots.

1. Run the **`FIX_MPQS_RUN_AS_ADMIN.bat`** inside the **`MpqFixer`** that you copied, as
   **`Administrator`**.

### Adding/Running A Platform

1. Open **`Cactus`**.
1. Click **`Settings`** and set your **`Diablo II Root Directory`** to your Diablo II folder. **`(Example: C:\Games\Diablo II)`**
1. Click **`Add`**.
1. Type in the name of the **`Platform`** you want to run. This should match a folder in the **`Platforms`**
   folder. (Example: If you want to run **`1.09b`**, type **`1.09b`**).
1. **`Optional (Recommended)`**: Type in a **`Label`** for this platform. If you label your platform, it will have its own dedicated
   save directory, allowing you to have multiple entries using the same platform but with different save locations.
   If you don't use a label, all the characters with this platform name will be stored in the same location (flat structure).
   You can have multiple entries using the same platform with and without labels as well. A label cannot be
   removed from an entry once created, but it can be renamed. A label cannot be added to an entry once created.
1. Enter the name of your **`Launcher`**. **`(Example: Game.exe, Alpaca.exe)`**
1. Enter the Flags you want (Example: **`-ns`**).
1. Click **`Add`**.
1. Select your newly added Platform and press **`Launch`**.

The game should start. If you are having video issues, please make sure you
have read the [**`README-RENDERERS`**](README-RENDERERS.md) and ensure that
it was configured properly.

**`NOTE`**: Make sure to leave the Cactus application running throughout your play sessions (you can minimize it).
Cactus keeps track of the running Diablo II processes it launches as to protect you from accidentally switching to
a different platform, and causing your **`Save Path`** to be updated to an incorrect location.

### Template & Labeling System

The Cactus Template & Labeling System allows you to be able to easily 
start using a few pretty cool and very interesting workflows, while
allowing you to re-use your existing platforms, thus minimizing the
amount of disk space used.

For example, let's say we want to play **`Solo Self Found`** as defined 
as **`Only using items that the character has found with their own 
hands`**, this pretty much means untwinked play. However, let's say you 
are also ok with using mules as a form of an extended stash for your 
main character. Thus, any items your main character finds, can be placed 
in storage, and will only be used by that main character specifically. 
If you were to do this manually, for each particular main character you 
made, it would quickly get out of hand since all the main characters and 
each individual main character's set of mules, would all be in the same 
folder. This is where the Templating & Labeling System kicks in. Now, we 
could simply make a new entry in Cactus pointing to an existing 
platform, and give it a particular label (Say the name of that specific 
main character) and play the game. A dedicate save folder with the given 
label will be created under the Saves directory for this platform. 

For example, I want to make a character called **`Isaac`**. Isaac will 
have their own set of mule characters as well and we'll call them 
**`Mule_A`**, **`Mule_B`**, and **`Mule_C`** for simplicity. This 
character will also be on **`1.09b`**. Thus, we can make a new entry for 
our **`1.09b`** platform with the label **`Isaac`**. Once we start the 
game, we will have the following structure in our Diablo II root 
directory (let's assume I already made the characters in-game): 

```
/Platforms/1.09b/

/Saves/1.09b/

/Saves/1.09b/Isaac/
/Saves/1.09b/Isaac/Isaac.d2s
/Saves/1.09b/Isaac/Mule_A.d2s
/Saves/1.09b/Isaac/Mule_B.d2s
/Saves/1.09b/Isaac/Mule_C.d2s
```

As you can see, this entry is fully isolated using its platform and 
label combination. Now, let's say you and your friends want to have some 
type of tournament on **`1.09b`**. No problem! You can quickly add 
another entry for the **`1.09b`** platform with another label, such as 
**`Tournament 2022`** and start it up. The same exact **`1.09b`** 
platform files that we used before will be re-used, and we will have a 
new save directory. Let's create a new character called **`Bethany`** 
and give Bethany a few mules as well. We'll call the mules the same as 
before, and since they are isolated, we can reuse the same muling naming 
scheme with no conflicts. So now our structure looks like this: 

```
/Platforms/1.09b/

/Saves/1.09b/

/Saves/1.09b/Isaac/
/Saves/1.09b/Isaac/Isaac.d2s
/Saves/1.09b/Isaac/Mule_A.d2s
/Saves/1.09b/Isaac/Mule_B.d2s
/Saves/1.09b/Isaac/Mule_C.d2s

/Saves/1.09b/Bethany/
/Saves/1.09b/Bethany/Bethany.d2s
/Saves/1.09b/Bethany/Mule_A.d2s
/Saves/1.09b/Bethany/Mule_B.d2s
/Saves/1.09b/Bethany/Mule_C.d2s
```

This is just one of the new workflows that our Templating & Labeling 
System enables. This workflow requires a modified **`D2gfx.dll`** to 
allow multiple instances of the game, allowing you to to mule between 
your main character and your mules via LAN. Singling provides this 
feature for the versions it supports. For all other versions, you'll 
need to find a copy of it online. 

Another workflow which I really like is using this labeling system to 
separate my **`Classic`** and **`Expansion`** characters. By using two 
separate labels to the same platform, we can have two separate save 
paths for them. If we did this, we would have the following: 

```
/Platforms/1.09b/

/Saves/1.09b/

/Saves/1.09b/Classic/

/Saves/1.09b/Expansion/

/Saves/1.09b/Isaac/
/Saves/1.09b/Isaac/Isaac.d2s
/Saves/1.09b/Isaac/Mule_A.d2s
/Saves/1.09b/Isaac/Mule_B.d2s
/Saves/1.09b/Isaac/Mule_C.d2s

/Saves/1.09b/Bethany/
/Saves/1.09b/Bethany/Bethany.d2s
/Saves/1.09b/Bethany/Mule_A.d2s
/Saves/1.09b/Bethany/Mule_B.d2s
/Saves/1.09b/Bethany/Mule_C.d2s
```

You can pretty much label your platforms whatever you want as long as 
the name can be used for the folder on your hard drive. If you are using 
some illegal symbols like **`/`**, then Cactus will properly detect that 
and give you the appropriate message so that you can fix it. You can 
also omit the label if you want and that works perfectly fine with the 
above scenarios. Let's say you wanted to have a **`1.09b`** platform and 
have everything in there without caring about labels (essentially a flat 
layout, although you can also have a flat layout with a label, it just 
depends on how you want to organize stuff), go ahead and create an entry 
with the platform name **`1.09b`** and leave the label blank. Launching 
the game will just point the save path to the **`/Saves/1.09b/`** folder 
and your files will be placed in there. Assuming we then created a 
character called **`Leslie`**, we would then have the following 
structure: 

```
/Platforms/1.09b/

/Saves/1.09b/
/Saves/1.09b/Leslie.d2s

/Saves/1.09b/Classic/

/Saves/1.09b/Expansion/

/Saves/1.09b/Isaac/
/Saves/1.09b/Isaac/Isaac.d2s
/Saves/1.09b/Isaac/Mule_A.d2s
/Saves/1.09b/Isaac/Mule_B.d2s
/Saves/1.09b/Isaac/Mule_C.d2s

/Saves/1.09b/Bethany/
/Saves/1.09b/Bethany/Bethany.d2s
/Saves/1.09b/Bethany/Mule_A.d2s
/Saves/1.09b/Bethany/Mule_B.d2s
/Saves/1.09b/Bethany/Mule_C.d2s
```

It's just another folder after all ;). The nice thing about this is that 
since all of these are sharing the same platform, switching between 
these entries is extremely fast since no files need to change on your 
hard drive, but rather we simply just update the registry save path, and 
you are back in the action. Have fun! 

## Using Cactus like a Service

Cactus has some basic tracking of processes that it launches in order to 
ensure that there are no accidental launches of other versions or 
combinations of the game that would cause your Save Path location to be 
changed mid-game. Thus it is essential for Cactus to remain running 
while you are playing. If you are always going to be running Diablo II 
via Cactus, you may want to go into the Cactus Settings and toggle the 
**`Minimize to System Tray`** option so that it doesn't take up space in 
your taskbar. I personally like having it show in the taskbar but that's 
just preference ;D. 

## Moving Cactus To A New Computer

If you want to move all of your Platforms, Characters, and Diablo II folder
to another machine, you will need to:

1. Copy your entire Diablo II folder to your new computer.
1. Open **`Cactus`**.
1. Click **`Settings`** and change your **`Diablo II Root Directory`** to match the location on your new computer.
1. Click **`Reset`**.
1. Now **`Launch`** whatever Platform you want.

Clicking **`Reset`** will cause Cactus to reconfigure itself by removing 
some files from your **`Diablo II Root Directory`** and wiping the 
**`Last Ran`** box on the entry that has it. Once you launch the game, 
the registry will properly point to your appropriate save location and 
your platform files will be copied back to your Diablo II root folder. 
In some rare cases (only on first install), you may need to do a little 
bit of manual organization in your Diablo II root folder to get things 
aligned properly. Once aligned, it's all tracked and automatic. 

## Updating Files In The Platforms folder

If you update any files in your Platforms folder, then click the 
**`Reset`** button, and run it again. This will cause Cactus to 
re-install the files with the new ones. 

## OMAHGOD! My Characters Are Gone! Cactus Deleted Them!!!

Cactus comes with [built in safety features](https://github.com/fearedbliss/Cactus-Core/blob/master/Cactus/FileGenerator.cs)
specifically designed to protect critical directories and files, which 
includes the save directories. Thus it is impossible for Cactus to have 
deleted them. Cactus also only operates within the Diablo II root 
directory so it also wouldn't be possible for Cactus to delete saves 
that are in **`1.14d+`**'s new save directory that is in your personal 
folder. 

Since Cactus is **`A Modern Version Switcher & Character Isolator`**, it 
will update the registry location of where the game should look for the 
saves. For example, if you are playing a **`Platform`** called 
**`1.05b`** with a **`Label`** called **`Chinchilla`**, the files for 
this platform would logically be located under **`Platforms/1.05b/`**, 
and the saves would be located under **`Saves/1.05b/Chinchilla/`**. Both 
directories are located inside your Diablo II folder. Thus, when the 
game starts, your characters are properly isolated and protected. If 
this is the first time you launched a game with Cactus, and you 
previously just had a regular Diablo II installation, then it would seem 
as if all your characters got deleted, or magically dissapeared. 
However, they are simply located in the original location that your 
computer saved them to. If you were playing **`1.14d+`**, they most 
likely are located at: 

**`%USERPROFILE%/Saved Games/Diablo II`** 

If you were playing **`1.13d`** or below, they are inside the Diablo II 
folder itself under a folder called **`save`**. 

Lastly, always remember to keep backups when running Third Party Tools 
or Modifications. 

## Cactus switches versions but I don't see the Diablo II window and there are no errors either.

If switching versions with Cactus doesn't actually launch the game but you also
don't notice any errors, this could be an indication that either your Video Settings
are not correct, or that you may need to run Cactus in Admin Mode. I've noticed that
if I have Diablo II installed on the **`C:\`** drive (i.e **`C:\Games\Diablo II`**),
I would need to run Cactus at least once in Admin Mode for it to work properly, but
if I installed Diablo II on another drive (i.e **`D:\Games\Diablo II`**), it would
work fine without Admin privileges. I'm pretty sure this is due to the **`C:\`**
drive generally being a protected drive.

Another thing to note is that I observed that I only needed to run Cactus once in Admin
Mode for this to "stick" and continue working even if I opened Cactus in the future without
Admin rights, although I haven't tested if this persists across reboots, but it possibly may.
I've also noticed that even when there was a problem, some versions would work,
and some wouldn't. Specifically versions **`1.00 - 1.06b`** worked, but **`1.07 - 1.13d`**
didn't.

Lastly, make sure that there are no zombie Diablo II processes running in the background (Task Manager),
that can cause the version switcher to either not switch away or something else. I know that
the new telemetry executables added to **`1.14d`** (i.e **`SystemSurvey.exe`** and **`BlizzardError.exe`**)
are not needed for the game to actually function, and can lock the process for a bit after you close
the game. The Cactus platforms do not contain these files since I've deleted them, however, if you
are installing from a fresh copy of Diablo II from Blizzard, it will have them.

## File Read Error on Diablo II Start Up

![Error](https://i.imgur.com/DQMcHlM.png)

If you are receiving the above error, it may be possible that some of 
your MPQs are still hidden from Cactus' previous behavior before version 
**`2.2.0`**. For newer versions of Cactus, Cactus will automatically 
rename the following MPQs back to normal whenever you either 
**`Launch`** a platform, or if you already have an entry that was 
**`Last Ran`**, when you press the **`Reset`** button as well. If for 
whatever reason that still doesn't work, you can go to your Diablo II 
root directory and make sure that the following **`4`** Expansion MPQs 
are properly named: **`d2exp.mpq`**, **`d2xvideo.mpq`**, 
**`d2xmusic.mpq`**, and **`d2xtalk.mpq`**. If you see any of them with 
the **`.bak`** extension, simply remove that extension and everything 
should be good. If you are receiving this error but those files are in 
place, then it is something else not related to Cactus. 

## Game Screenshots

![1.00](https://i.imgur.com/uugMn48.jpg)
![1.05b](https://i.imgur.com/901u4V7.jpg)
![1.07](https://i.imgur.com/zHD9s5L.jpg)
![1.08](https://i.imgur.com/sUiFKqN.jpg)
![1.09b](https://i.imgur.com/JZ9bIOy.jpg)
![1.10](https://i.imgur.com/Vw4yaDM.jpg)
![1.13d](https://i.imgur.com/XiQheXy.jpg)
![1.14d](https://i.imgur.com/pojq3Jw.jpg)
