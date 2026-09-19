# How to Back Up Save Data

On the PS2, game saves are stored exclusively on a **PS2 Memory Card**. A PS1 Memory Card is used only for PS1 game saves because it is both too small (128 KiB) and uses a completely different, incompatible logical structure.

**Save Data** is essentially a directory identified by a unique save ID (for example, `BESCES_12345`). In theory, backing up a save could be as simple as copying its directory from `mc0:/` to `mass:/` (`usb:/` in wLE R3Z). Unfortunately, <span style="color: #D32F2F;">this is one of the most common mistakes made by inexperienced users</span>. Some games use the timestamp (stored in the **MCFS**, the Memory Card File System) as a form of copy protection. Simply copying the save directory may change or lose the original timestamp. For games that validate this timestamp, the value stored by the file system must match the one stored within the save. Otherwise, the save will be detected as corrupted. Additionally, some games use file or directory names containing characters that are not permitted by FAT32 and exFAT. To solve both of these issues, the **PSU** format was introduced many years ago. A PSU file is a container that stores both the save data and all associated metadata, allowing the save to be restored without losing any information.

This guide describes two methods for exporting and importing saves in the PSU format. A third option is to create a complete image of the memory card (e.g. using **Memory Card Annihilator**), but that approach is intended for different purposes and is therefore outside the scope of this guide. However, it can also serve as an additional backup.

## Method A: Apollo Save Tool

**Apollo Save Tool** is a save management application. It supports most commonly used save container formats, both types of PlayStation memory cards, USB storage devices (formatted as **FAT32** with an **MBR** partition table), and `host:/`.

1. Launch **Apollo Save Tool** using your preferred method. Press **Right** on the D-pad until you reach the vase icon labeled **Saves**.

<p align="center"><img src="./images/apollo_main.png" alt="Apollo: Main Menu" /></p>

2. Select **Bulk Saves Management**.

<p align="center"><img src="./images/apollo_sav_bup_1.png" alt="Apollo: Saves 1" /></p>

3. Select **.PSU Export All Saves to Backup Storage**, then choose **Copy Saves to Backup Storage (mass:/)** to export the saves to your USB stick.

<p align="center"><img src="./images/apollo_sav_bup_2.png" alt="Apollo: Saves 2" /></p>

4. Wait until all progress bars reach **100%** and a confirmation message appears indicating that the saves have been exported to `mass:/PS2/SAVEDATA/`. Press **Cross** to dismiss the message, then press **Circle** a few times to return to the main menu and exit the application.

All exported saves will be located in `mass:/PS2/SAVEDATA/*.psu` and will use the following naming format: `<GameID>_<Date YYYY-MM-DD>_<Time HHMMSS>.psu` (for example: `SCES50294_2026-07-30_105959.psu`).

To **restore** saves, follow the same procedure, except that in step 1 you must select **Ext Saves** (short for **External Saves**) instead of **Saves**. Then, choose **Copy all Saves to Memory Card**.

<p align="center"><img src="./images/apollo_sav_restore.png" alt="Apollo: Restore Saves" /></p>

## Method B: unofficial LaunchELF

You can also back up and restore saves using any version of **unofficial LaunchELF** (uLE) or **double-unofficial LaunchELF** (wLE). Although these applications are primarily file managers, they can also create and extract PSU files. I recommend **wLE R3Z**, as it supports all currently available storage devices.

1. Launch **double-unofficial LaunchELF R3Z** (abbreviated as **wLE R3Z**) using your preferred method.

2. Navigate to `mc0:/` (the PS2 Memory Card in Slot **1**) or `mc1:/` (Slot **2**). Press the **L1** button to change the display mode to **Show Content as**: **Game Title + Details** and **Sort Content by**: **Game Title**. Then press the **Triangle** button to close the popup and apply the changes.

<p align="center">
	<img src="./images/wle_sav_list_1.png" alt="wLE: List 1" />
	<img src="./images/wle_sav_list_2.png" alt="wLE: List 2" />
</p>

3. Mark all save folders by pressing the **Square** button, or select only the ones you want to back up by pressing the **Circle** button on each folder.

4. Press the **R1** button and select **Copy**.

<p align="center"><img src="./images/wle_sav_copy.png" alt="wLE: Copy Saves" /></p>

5. Return to the device list and open `usb:/` (in other versions of wLE, the mount point is named `mass:/` instead). Then press the **R1** button and select **Create PSU** (**psuPaste** in most versions of wLE -- <span style="color: #D32F2F;">not **Paste**</span>). After the export is complete, the new PSU files should appear in the destination you selected.

<p align="center"><img src="./images/wle_sav_makepsu.png" alt="wLE: Create PSU" /></p>

To **restore** saves, follow the same procedure, except that instead of **Create PSU**, choose **Extract PSU** (**psuPaste** in most versions of wLE -- <span style="color: #D32F2F;">not **Paste**</span>).

<br />Berion<br />2026-07-31

<p align="right"><small>➜ Go back to <a href="index.md">main page</a></small></p>