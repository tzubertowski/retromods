---
title: "SF2000/GB300 First steps & Multicore setup"
description: "First steps to take with SF2000/GB300 retro handheld console"
image: "images/post/gb300-multicore/thumbnail2.png"
date: 2025-07-18T10:56:47+06:00
draft: false
author: "Prosty"
tags: ["gb300", "sf2000", "multicore", "gpsp", "dynarec", "cfw", 'gba save']
categories: ["GB300 Retro Handheld"]
---

# SF2000/GB300 First steps & Multicore setup

This article covers the installation of our software modification called **Multicore** for **Datafrog SF2000** and **GB300** handhelds.

There are many ways to use Multicore. In this short guide, we'll cover the **simplest** method. More advanced tools for customisation are linked at the end.

---

### 0. Table of Contents
- [1. Prerequisites](#1-prerequisites)
- [2. Installing the Multicore](#2-installing-the-multicore)
- [3. Using the Multicore](#3-using-the-multicore)
  - [3.1 Adding ROMs](#31-adding-roms)
  - [3.2 Reloading ROM list & running games](#32-reloading-rom-list--running-games)
- [4. OPTIONAL: Tips & Tricks](#4-optional-tips--tricks)
  - [4.1 Change Game Boy palette](#41-change-game-boy-games-palette)
  - [4.2 GBA and GB/C RTC settings](#42-gba-and-gbc-rtc-settings)
  - [4.3 Editing core options & community scripts](#43-editing-core-options-and-other-cool-scripts)
  - [4.4 Menu integration & advanced tools](#44-running-games-from-main-menu-categories--other-customisation)
- [5. Updating GB300 to v2](#5-updating-gb300-to-v2-software-version)

---

### Step 1: Prerequisites
<p align="center">
  <img alt="Step 1" src="/post/gb300-multicore/step1.jpg#center" />
</p>

- A Datafrog SF2000 or GB300 handheld
- An SD card reader (via phone or PC) to transfer files to the SD card
- If you're using a **GB300**, make sure you're on **GB300 v2**. See [Updating GB300 to v2 software version](#5-updating-gb300-to-v2-software-version)

---

### Step 2: Installing the Multicore
<p align="center">
  <img alt="Step 2" src="/post/gb300-multicore/step2.jpg#center" />
</p>

1. Insert your SD card into your computer or phone
2. Download the [latest stable release of Multicore](https://github.com/tzubertowski/gb300_multicore/releases)
   - ⚠️ **Make sure you download the archive for your correct device (GB300 or SF2000)**
3. Unzip the archive
4. Copy everything inside the `sdcard` folder to the **root** of your SD card
   - Replace any files if prompted
<p align="center">
  <img alt="Multicore Archieve step 1" src="/post/gb300-multicore/multicore-2.jpg#center" />
</p>
<p align="center">
  <img alt="Multicore Archieve step 2" src="/post/gb300-multicore/multicore-3.jpg#center" />
</p>

5. You should now see a `cores` folder on the root of the SD card
<p align="center">
  <img alt="Multicore Archieve step 32" src="/post/gb300-multicore/step3.png#center" />
</p>

6. Put the SD card back into your device and power it on
7. On first boot, your device may perform a **bootloader fix update** (this is automatic and only happens once)
8. It's recommended you remove the `sd:\UpdateFirmware` folder once **bootloader fix update** has been installed
9. Done! Multicore is now installed 🎉

---

### 3. Using the Multicore
<p align="center">
  <img alt="Step 3" src="/post/gb300-multicore/step3.jpg#center" />
</p>

This guide focuses on the **simplest, tool-free** usage.

#### 3.1 Adding ROMs

1. Place **unzipped** ROMs into their respective system folders under `sd:/roms/*`
2. Check the list of supported systems and emulators [here](https://github.com/tzubertowski/gb300_multicore?tab=readme-ov-file#cores-in-this-release)
3. Example:
   - To add *Pokémon Fire Red*, copy the file like this:
     ```
     sd:/roms/gba/PokemonFireRed.gba
     ```

#### 3.2 Reloading ROM List & Running Games

Whenever you add new games, you must **regenerate** the ROM list.

**Recommended Option 1: On the device**
- Navigate to:
<br>
`
User, ROMS & SETTINGS → Game list → js2000;rom_list_generators.js.gba
`
- Press **A** to generate the ROM list
- Your game will now appear under:
<br>
`
User, ROMS & SETTINGS → Game list → gba;PokemonFireRed.gba
`
<br><br>
**Option 2: On your computer**
- Run `make-romlist.bat` from the SD card (`sd:/make-romlist.bat`)

---

### 4. OPTIONAL: Tips & Tricks
<p align="center">
  <img alt="Step 4" src="/post/gb300-multicore/step4.jpg#center" />
</p>

#### 4.1 Change Game Boy Games Palette

You can customise the colour palette for Game Boy games:
- Run the script:
<br>
`
User, ROMS & SETTINGS → Game list → js2000;gambatte_pallete_picker.js.gba
`

#### 4.2 GBA and GB/C RTC Settings

You can also manage RTC (Real-Time Clock) settings directly:
- Run:
<br>
`
User, ROMS & SETTINGS → Game list → js2000;rtc_settings_manager.js.gba
`

#### 4.3 Editing Core Options and Other Cool Scripts

The community has created additional helpful scripts, such as the config editor. Browse the script library:
- [JS2000 script examples](https://github.com/axgdev/js2000/tree/main/examples)

#### 4.4 Running Games from Main Menu Categories & Other Customisation

For more advanced customisation, check out these tools:

- [Multicore ROM Helper](https://github.com/fjdogar/multicore_rom_helper/releases)
- [GB300/SF2000 Tool](https://github.com/nummacway/gb300-sf2000-tool)
- Read Q_ta's detailed guide on [Discord](https://discord.com/channels/741895796315914271/1345638715057246268)

---

### 5. Updating GB300 to v2 Software Version
<p align="center">
  <img alt="Step 5" src="/post/gb300-multicore/step5.jpg#center" />
</p>

If you're using GB300 with v1 firmware or you're not sure:

1. Format the SD card to **FAT32**
2. Download:
 - [Minimal backup](https://archive.org/details/sd-card-default-sem-r-0-ms_202501)
 - (Full backup not linked due to ROMs being included)
3. Unzip the archive **directly** to the SD card
 - You should now see folders like `bios`, `resources`, `roms`, etc. on the root

Done! You can now follow the [Multicore installation instructions](#2-installing-the-multicore).

---

Happy gaming! 🕹️
```
