---
title: "GB300 First steps & Multicore setup"
description: "First steps to take with GB300 retro handheld console"
image: "images/post/gb300-multicore/thumbnail.png"
date: 2024-08-10T16:56:47+06:00
draft: false
author: "Prosty"
tags: ["gb300", "sf2000", "multicore", "gpsp", "dynarec", "cfw", 'gba save']
categories: ["GB300 Retro Handheld"]
---

# GB300 Setup & First steps

The GB300 is a versatile handheld console, but to get the most out of it, a few important steps should be followed during the initial setup. 

This guide will walk you through the process, covering essential fixes and recommended enhancements.

## 1. Bootloader Fix
<p align="center">
  <img alt="Bootloader fix" src="/post/gb300-multicore/fee1.jpg#center" />
</p>

Before you can enjoy the full potential of your GB300, you need to address a critical issue with the bootloader. This fix is essential and must be completed before any other modifications.

   > **Note**: We will only need to take this step once, even if you change out the SD card down the line
#### Steps to Install the Bootloader Fix

1. **Download the GB300 Tool**: The tool necessary for applying the bootloader fix can be found on GitHub. You can download it from the following link: [GB300 Tool - GitHub Releases](https://github.com/nummacway/gb300tool/releases).

2. **Setup GB300 Tool**: Once the tool is downloaded, insert the SD card from GB300 into your PC, run the application, enter the drive/folder where your GB300 SD card is at. For me that's D:\
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/gbtool-intro.jpg#center" />
</p>

3. **Request bootloader fix from the menu**: Make sure you select the "Patch bootloader on next boot" option, eject the SD card
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/gbtool-2-bootloader.jpg#center" />
</p>

4. **Re-insert the SD card into GB300 and turn it on**: follow the on-screen instructions, once the console has booted you are ready to go to the next step. 

   > **Note**: Ensure that this step is completed before proceeding with any other modifications to avoid potential issues.

## 2. OPTIONAL: Replace the SD Card
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/fee2.jpg#center" />
</p>

The SD card included with the GB300 is known to be unreliable and prone to failure. It is highly recommended to replace it with a new one to avoid potential data loss or corruption.

#### Steps to Replace the SD Card

1. **Prepare a New SD Card**: Purchase a reliable SD card and format it to FAT32.

2. **Copy Data from the Original SD Card**: Simply copy all contents from the original SD card to the new one. This ensures that your console will run as expected with the new SD card.

You an also create an image out of your card and write it into a newly prepared SD card.

## 3. Install the Multicore
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/fee3.jpg#center" />
</p>

With Multicore you will be able to run both new emulators as well as more performant versions of the stock emulators. Eg. Thanks to the community work GB300 now works with GPSP with Dynarec - making vast majority of games playable, most of them in full FPS.

To unlock this potential, you need to install the Multicore software.

#### Steps to Install Multicore

1. **Download the Multicore**: The Multicore software can be found on GitHub. Download it from the following link: [Multicore - GitHub Releases](https://github.com/tzubertowski/gb300_multicore/releases).

2. **Unpack**: Once downloaded unpack the archive, eg. in my case that file is gb300_multicore_0.10_v0.3.0.7z. There should be one folder called "sdcard" extracted.
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/multicore-archive.jpg#center" />
</p>

3. **Copy the multicore contents**: copy everything that's within the "sdcard" folder
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/multicore-2.jpg#center" />
</p>

4. **Paste the contents on top of GB300 SD card**: simply navigate to the GB300 SD card and paste the multicore on top of the SD card, replace any files if asked for it
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/multicore-3.jpg#center" />
</p>


Aaand **that's it!** you've got the Multicore up and running. 

  > **Tip**: Always download the Multicore from the official release page on github. 3rd party compilations often have invalid or unoptimised config, illegal roms or outdated emulator cores.

## 4. USE THE MULTICORE
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/fee4.jpg#center" />
</p>

There are many ways to use the Multicore, I will present You with the easiest one ready out of the box

#### Simplified how-to
- unzip the ROM file
- place the ROM file into sd:/roms/NAME-OF-THE-SYSTEM folder
  - see [GitHub readme for list of supported folder names and systems](https://github.com/tzubertowski/gb300_multicore/blob/master/README.md#cores-in-this-release)
- run make-romlist.bat for Windows, make-romlist.sh for Osx/Linux


To play the game on GB300:
- run the game from ROMS category

  > **Tip**: It's vital you take those steps and run the game from ROMS category, as otherwise stock emulators will be used

#### Example - using GBA - Advance Wars 1
Let's assume I want to play **Advance Wars 1** from **GBA** on my GB300 using Multicore. I simply:

- **unzip** my ROM archieve so that I can copy the "game.gba" file, in my case that's
> Advance Wars (USA) (Rev 1).gba
- **copy** the file into SD:/roms/gba folder
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/use-1.jpg#center" />
</p>

- **run** make-romlist.bat as I'm using Windows
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/use-2.jpg#center" />
</p>

- once the process has finished I simply inject the SD card back into my GB300 and turn it on


**On the GB300**
- I navigate to ROMS category
- I run "gba; Advance Wars (USA) (Rev 1).gba" file
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/use-3.jpg#center" />
</p>

Notice the red screen indicating you are running Multicore
<p align="center">
  <img alt="Expansion bay dla PS2 fat" src="/post/gb300-multicore/use-4.jpg#center" />
</p>



**And that's it! Enjoy the game.**


## 5. OPTIONAL: Avoid Using Built-in ROMs

While the GB300 comes preloaded with ROMs, they are known to have various issues. For example, **Castlevania: Circle of the Moon** on GBA is notorious for freezing near the end, preventing you from finishing the game.

### Recommended Steps

- **Collect Your Own Game Set**: It's best to curate your own collection of ROMs, ensuring they are reliable and compatible with the GB300.


## Conclusion

By following these steps, you can significantly improve the performance and reliability of your GB300 handheld console. You also have learned how to install and use Multicore. Have questions? Ask us on [/r/GB300](https://www.reddit.com/r/GB300/)
 