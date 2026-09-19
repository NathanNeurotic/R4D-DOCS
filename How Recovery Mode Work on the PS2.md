---
layout: default
title: "How Recovery Mode Work on the PS2"
---

# How Recovery Mode Work on the PS2

Recovery mode is not implemented in the official firmware (the so-called BIOS) of SCPH and KDL models. COH and DESR are separate hardware categories and require a separate guide. Normally, users never need recovery mode.

The PS2 firmware (**BOOTROM** and **DVDROM**) is stored on ROM chips, which, as the name suggests, are read-only and therefore cannot be overwritten. Software such as **Browser 2.00** (HDD OSD), **PlayStation Broadband Navigator** (PSBBN), and **Linux**, however, is installed on the hard disk and can be reinstalled from the original installation disc on supported configurations. The same applies to the **DVD-Video Player** update stored on the PS2 Memory Card.

The problem arises with exploits, which often require another exploit to install them. Since users typically have access to only one exploit -- or can use only one because of their console model or lack of the required hardware -- a recovery mode that ignores the user's configuration and allows any application to be launched becomes extremely useful.

Of course, recovery can also be performed using any available [attack vector](How%20to%20Hack%20a%20PlayStation%202%20in%202026.html), such as another PS2 Memory Card with Free McBoot (FMCB), an internal hard disk drive, Free DVD Boot (FDVDB), and so on. However, the purpose of recovery mode is to use the same exploit that is already installed -- one that is still functional, but whose configuration and/or resources have become corrupted and need to be restored or replaced.

## LoadBOOTer (LB)

It does not have a recovery mode, but it does not need one. It is usually used only to launch PS2BBL/PS2BBLE.

## PlayStation 2 Basic Boot Loader ([PS2BBL](https://github.com/israpps/PlayStation2-Basic-BootLoader))

When the application starts, it looks for the following file on the USB stick:

- mass:/PS2BBL/CONFIG.INI

`CONFIG.INI` is the configuration file that will be loaded instead of the one stored on, for example, the PS2 Memory Card.

Both [FAT32](https://en.wikipedia.org/wiki/Fat32) and [exFAT](https://en.wikipedia.org/wiki/ExFAT) are supported. MBR partition tables are supported, while [GPT](https://en.wikipedia.org/wiki/GUID_Partition_Table) partition tables are not. If GPT is used, the USB stick will not be detected.

## PlayStation 2 Basic Boot Loader Extended ([PS2BBLE](https://github.com/saildot4k/PlayStation2-Basic-BootLoader-Extended))

When the application starts and cannot find a configuration INI, it looks for the following file on the USB stick:

- mass:/RESCUE.ELF

Both [FAT32](https://en.wikipedia.org/wiki/Fat32) and [exFAT](https://en.wikipedia.org/wiki/ExFAT) are supported. MBR partition tables are supported, while [GPT](https://en.wikipedia.org/wiki/GUID_Partition_Table) partition tables are not. If GPT is used, the USB stick will not be detected.

## Free McBoot ([FMCB](https://sites.google.com/view/ysai187/home/projects/fmcbfhdb))

When the application starts, it looks for the following files on the USB stick:

- mass:/RESCUE.ELF
- mass:/FREEMCB.CNF

`RESCUE.ELF` is an arbitrary, unencrypted executable that is launched instead of the modified `rom0:OSDSYS`. It is recommended to use the **wLE** file manager (any version) for this purpose. `FREEMCB.CNF` is the configuration file that is loaded instead of the one stored on the PS2 Memory Card.

Only [FAT32](https://en.wikipedia.org/wiki/Fat32) on [MBR](https://en.wikipedia.org/wiki/Master_boot_record) is supported. If [GPT](https://en.wikipedia.org/wiki/GUID_Partition_Table) is used, the USB stick will not be detected. If [exFAT](https://en.wikipedia.org/wiki/ExFAT) is used, FMCB will freeze (without **BDMAssault** drivers). All other file system is also unsupported, and the USB stick will not be detected, just as with GPT.

## OSDMenu ([OSDM](https://github.com/pcm720/OSDMenu))

It does not have a recovery mode, but it does not need one. It is usually launched from LoadBOOTer, PS2BBL, or PS2BBLE.

<br />Berion<br />2026-08-19

<p align="right"><small>➜ Go back to <a href="{{ site.baseurl }}/">main page</a></small></p>
