# 3D Sound (DSOAL w/ OpenAL Soft)

## Included 3D Sound Versions 

**`DSOAL (dsound.dll)`**
- **`Commit: 75f88e1bd923`**
- **`Commit Date: 2022-03-22-1516`**
- **`Build Date : 2022-03-24-0830`**

**`OpenAL Soft (dsoal-aldrv.dll)`**
- **`Commit: f2f83aaabba5`**
- **`Commit Date: 2022-04-01-1930`**
- **`Build Date : 2022-04-05-1339`**

## Description [(Video)](https://youtu.be/D7g2GmI2SeA)

These files will allow you to enable the following in-game settings: 
**`3D Sound`**, **`Environmental Effects`**, and **`3D Bias`**. This fix 
is equivalent to restoring lost game functionality caused by modern 
hardware no longer natively supporting these features (Such as Diablo 
II's Glide support requiring the use of a glide wrapper to enable the 
**`3DFX (Voodoo)`** card's effects like **`Perspective`** mode). In this 
instance, the lost settings were originally provided by **`Creative 
Sound`** cards like **`Sound Blaster`**. 

Have fun listening and playing with these amazing, and practically lost 
features. This works for all versions of Diablo II. No Diablo II files 
are required to be modified for this to work, it's an additive only 
change just like using the **`ddraw.dll`** for **`cnc-ddraw`**, and can 
be used on Vanilla Diablo II. 

The Cactus default installation already includes these two files and you 
simply need to enable the options you want in game. 

## Screenshot

![Sound Settings](https://i.imgur.com/2oTPc47.jpeg)

## Wine (Tested on Linux)

Follow the [Wine (Tested on Linux)](README-RENDERERS.md#wine-tested-on-linux)
section in the README-RENDERERS file for instructions on how to do this,
but add **`dsound`** to the list rather than **`ddraw`**. 

## Notes

### Crash on startup when using **`-ns`** and **`dsound.dll`**

![Error](https://i.imgur.com/ygCLcrr.png)

There's a bug with Diablo II where if you start the game with **`-ns`** 
and you are using the **`dsound.dll`**, the game will crash with an 
**`ACCESS_VIOLATION (c0000005)`** error. Simply remove the **`-ns`** 
when starting with the 3D sound system and everything should work. 
Alternatively, you can rename the **`dsound.dll`** to something else and 
then you'll be able to use **`-ns`** but you will lose **`3D Sound`**. 

This issue doesn't affect users that are using Singling since Singling 
actually skips the introduction cinematics completely, which 
coincidentally also skips the sound issue altogether. 

This bug also doesn't seem to be a **`DSOAL`** issue since I was only 
able to get debug logs from DSOAL when **`-ns`** wasn't used, which 
indicates that Diablo II itself had an issue starting up the sound 
system in the first place. 