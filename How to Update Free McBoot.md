# How to Update Free McBoot

If Free McBoot is installed as a **System Update** (OSD Update), it cannot be updated directly. This is because the existing installation must first be uninstalled before the new version can be installed. This requirement makes little sense, even for users with a cross-linked installation (commonly referred to as a "Multi Install"), since the old installation still has to be removed before the new one can be installed. The recommended approach is to back up your save data to another device or another PS2 Memory Card, perform a **full format**, and then install the new version (see **Scenario I**).

If you have a PS2 Memory Card with Free McBoot installed, it is your only PS2 Memory Card, and you do not have any other entry point, you probably do not want to **risk** losing your working setup. Instead, you can safely install the newer configuration, which is designed for mSAS packages, including the new CNF, the BDMA wrapper, and other related components (see **Scenario II**).

As you can see, this is more of a roadmap or a hub for dedicated guides than a tutorial. Each topic is complex enough to deserve its own guide. Good luck!

## Scenario I: Clean Install

### Step A. Back Up Your Saves

If you don't have any save data that you want to keep, you can skip this step and move on to the next one.

Otherwise, I recommend exporting all save data to the *.psu* file format. Do not simply copy the save folders (for example, from a memory card to a USB stick). Some games use timestamps to verify save data integrity, and those timestamps can be altered during a regular copy operation. A **PSU** container preserves all MCFS (the file system used by PS2 Memory Cards) attributes, including the original timestamps.

You can find detailed instructions in the [How to Back Up Save Data](How%20to%20Back%20Up%20Save%20Data.md) guide, which describes several methods for creating and restoring backups.

### Step B. Format the PS2 Memory Card

Instead of using **Uninstall Free McBoot**, **Uninstall Multi-Install**, or manually deleting files, it is best to format the PS2 Memory Card and completely erase its contents. Use the **Full** format option instead of **Quick**. During a full format, any bad blocks that are detected are marked and excluded from the file system. PS2 Memory Cards are now an aging technology, and their NAND flash memory can wear out over time. Identifying bad blocks before installing for example Free McBoot, helps avoid potential issues, including problems with storing save data.

You can find detailed instructions in the [How to Format Memory Cards](How%20to%20Format%20Memory%20Cards.md) guide, which describes the process.

> **<span style="color: #D32F2F;">WARNING:</span>** If this is your only PS2 Memory Card, **do not** turn off or reset the console after formatting. Otherwise, you will no longer have a working exploit or a way to restore it. After formatting is complete, press **Select** to open the file browser. Navigate to `mass0:/APPS/KELFBinder-mSAS/` and run the *.elf* file located there to continue the installation.

### Step C. Install the Exploit

Run **KELFBinder-mSAS** using any available method and install exploits for all supported models and regions. Detailed instructions can be found in the [How to Install System Update Exploit](How%20to%20Install%20Exploit.md) guide.

After completing this step, you will have installed **LoadBOOTer** as the System Update, **PS2 Basic Boot Loader Extended** as the Boot Loader, **Free McBoot** versions 1.8c and 1.966 as OSDSYS patchers, **OSDMenu** as an additional OSDSYS patcher (yes, all three at once), and **wLaunchELF R3Z** as the file manager.

### Step D. Install Applications

The last step is to add additional software, such as game loaders, alternative file managers, and emulators. Start any version of **uLE** or **wLE**, then copy `usb:/APPS/Save Application System (microSAS)/packages/<category>/*.psu` and use **<span style="color: #D32F2F;">psu</span>Paste** (**Extract PSU** in **wLE R3Z**) to extract them to `mc0:/` (1st slot) or `mc1:/` (2nd slot). They will automatically appear in the patched OSDSYS menu provided by **Free McBoot**. (**OSDMenu** can launch applications from the saves view, so no applications will be pinned to the main menu.)

You can find detailed instructions in the [How to Install Applications](How%20to%20Install%20Applications.md) guide, which describes the process.

## Scenario II: SYS-CONF Replacement

### Step A. Back Up SYS-CONF

Updating the configuration files consists of replacing the contents of the **SYS-CONF** folder on the PS2 Memory Card. Before doing so, I recommend making a backup of the entire `mc0:/SYS-CONF/` directory in case you decide to revert to your previous setup or restore files that are not included in the **PSUja** project configuration (more information is provided later in this guide), such as `IPCONFIG.DAT`.

For this, I recommend using **wLE R3Z** and simply copying the folder from the PS2 Memory Card to a USB stick (`usb:/`; depending on the wLE version, this mount point may be named `mass:/`).

### Step B. Install New SYS-CONF

The procedure is identical to the one described for installing mSAS packages in the guide: [How to Install Applications](How%20to%20Install%20Applications.md). The only difference is that, instead of copying applications, you should copy only the `usb:/MISC/containers/PSUja/new/System Configuration.psu` file and, following the same procedure described in that guide, extract it onto the PS2 Memory Card (**Extract PSU**; **psuPaste** in other wLE versions). This will overwrite the existing **SYS-CONF** folder.

### Step C. Cleaning

It is worth removing old files and outdated applications that are no longer in use to make space for new ones:

- Delete the `APPS` folder, as it is no longer needed. Each **mSAS** package is extracted into its own folder.
- You will probably no longer need `BOOT`. Some applications have a hardcoded path to `mc0:/BOOT/BOOT.ELF`, so if you still need this file, keep it together with `icon.sys` and all `*.icn`/`*.ico` files. By default, `BOOT.ELF` is an old wLE version from one of the early releases (which can additionally be replaced with a newer version).

### Step D. Install Applications

The last step is to add additional software, such as game loaders, file managers, and emulators. Start any version of **uLE** or **wLE**, then copy `usb:/APPS/Save Application System (microSAS)/packages/<category>/*.psu` and use **<span style="color: #D32F2F;">psu</span>Paste** (**Extract PSU** in **wLE R3Z**) to extract them to `mc0:/` (1st slot) or `mc1:/` (2nd slot). They will automatically appear in the patched OSDSYS menu provided by **Free McBoot** if you followed what was described in Step B.

You can find detailed instructions in the [How to Install Applications](How%20to%20Install%20Applications.md) guide.

<br />Berion<br />2026-07-31

<p align="right"><small>➜ Go back to <a href="index.md">main page</a></small></p>