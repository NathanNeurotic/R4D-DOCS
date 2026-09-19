---
layout: default
title: "Glossary"
---

# Glossary

Below you will find all the mysterious acronyms, abbreviations, and terms I use throughout the guides. This includes basic IT and PS2 scene terminology that you may encounter, for example, on social media.

- - -

<a id="apa"></a>
### APA

**A**ligned **P**artition **A**llocated is a native [partition table](#pt) format for the PS2 that can only be used on internal storage media. It is the only one from which the PS2 can start [System Update](#osdupd).

I recommend reading the following guide: [Internal Storage vs. External Storage](Internal%20Storage%20vs%20External%20Storage.md).

- - -

<a id="apajail"></a>
### APAJ

**APA**-**J**ail combines two formats: [APA](#apa) and [MBR/GPT](#pt), allowing the PS2 to start [System Update](#osdupd) while keeping the [exFAT](#fs) partition fully accessible on a PC without any additional software.

I recommend reading the following guide: [Internal Storage vs. External Storage](Internal%20Storage%20vs%20External%20Storage.md) or the [PS2HDH](https://www.psx-place.com/resources/ps2-hdd-decryption-helper.1507/) documentation.

- - -

<a id="appid"></a>
### AppID

AppID is a unique identifier for a homebrew application used in [SAS and mSAS](#sas) packages.

I recommend reading the following guide: [SAS and microSAS Packages](SAS%20and%20microSAS%20Packages.md).

- - -

<a id="bdm"></a>
### BDM

**B**lock **D**evice **M**anager combines support for [USB](#usb), [i.Link](#ilink), [MX4SIO](#mx4sio), and internal drives (excluding native [APA](#apa)/[PFS](#pfs) support), including [partition tables](#pt) (in addition to [MBR](#mbr), also [GPT](#gpt)) and [file systems](#fs) (such as the recently added [exFAT](#exfat)).

- - -

<a id="bdma"></a>
### BDMA

**BDMA**ssault is a wrapper that acts as a translation layer for USB modules, allowing them to support [exFAT](#exfat) on [USB](#usb), [i.Link](#ilink), [MX4SIO](#mx4sio), [MMCE](#mmce), internal disks, or even [UDPBD](#udpbd) (a network-based block device protocol).

- - -

### BIOS

The PlayStation 2 does not have a BIOS. Although technically incorrect, this term is very commonly used to refer to the console's [firmware](#firmware).

- - -

### BL

See the [BootLoader](#bootldr) entry for more information.

- - -

<a id="bootldr"></a>
### BootLoader

A **bootloader** is a small piece of software that runs when a system is powered on or reset. Its primary purpose is to initialize the hardware and load the software required to start the system. Depending on the system, it may also perform hardware checks, configure system components, verify the software being loaded, or select between different boot options.

- - -

<a id="bootstrap"></a>
### Bootstrap

A **bootstrap** is a program that initializes essential system components and loads the software required to continue the boot process.

- - -

### BOOTROM

BOOTROM is one of the chips that contains the [firmware](#firmware) used by PS2 consoles.

- - -

<a id="cfw"></a>
### CFW

**C**ustom **F**irm**w**are is the original [firmware](#firmware) modified in any way. While the [BOOTROM](#bootrom) and [DVDROM](#dvdrom) are read-only memories and cannot be overwritten in any way, on [DESR](#models) models, the [DVRP](#dvrp) firmware can be flashed from a [UDM](#udm) package.

- - -

### Chasis

See the [models](#models) entry for more information.

- - -

<a id="cli"></a>
### CLI

**C**ommand-**L**ine **I**nterface allows users to interact with software by entering commands as text. On the PS2, there are not many purely CLI applications, e.g. [Nutrino](#ntr) and RadShell.

You can read more on [Wikipedia](https://en.wikipedia.org/wiki/Command-line_interface).

- - -

### CMOS

CMOS is a colloquial term sometimes used to refer to the PS2's battery-backed [RTC](#rtc) and its associated settings and configuration data. Strictly speaking, the PS2 does not have a dedicated CMOS memory.

- - -

<a id="coh"></a>
### COH

See the [models](#models) entry for more information.

- - -

<a id="dashboard"></a>
### Dashboard

A dashboard is a user interface that provides access to the main functions, applications, and settings of a system. It typically serves as the main entry point for interacting with the system after it starts.

A few examples:

- [OSD-XMB](https://github.com/HiroTex/OSD-XMB)
- [PS2 Browser](#osdsys)
- [XEB+](http://www.hwc.nat.cu/ps2-vault/hwc-projects/xebplus/)

- - -

<a id="deckard"></a>
### Deckard

Deckard is a PowerPC 405GP-based processor used in later PS2 models to emulate the original MIPS R3000A-based IOP as well as the DEV9 Controller and Interface. It provides compatibility with software designed for the original IOP while also handling I/O operations and peripherals.

- - -

<a id="desr"></a>
### DESR

See the [models](#models) entry for more information.

- - -

<a id="dev1"></a>
### DEV1

**Dev.olution Mode 1** is a feature of many [modchips](#modchip) that allows `mc0:/BOOT/BOOT.ELF` to be launched when the console starts if the user holds down the appropriate button (usually **R1**).

- - -

<a id="dev2"></a>
### DEV2

**Dev.olution Mode 2** is a feature of many [modchips](#modchip) that allows `hdd0:__boot/boot.elf` to be launched when the console starts if the user holds down the appropriate button (usually **R1**).

- - -

<a id="dev3"></a>
### DEV3

**Dev.olution Mode 3** is a feature of some [modchips](#modchip) that allows an application to be launched when the console starts if the user holds down the appropriate button. The exact path can vary, and DEV3 has also not been a standard name for this feature across all modchips (for example, Modbo uses the name MASS as the BootMode option in its settings).

- - -

<a id="dev4"></a>
### DEV4

**Dev.olution Mode 4** is a feature of **DMS4 Pro/E.Z.I. Pro** [modchips](#modchip) that allows an application stored on the modchip's internal flash to be launched when the console starts if the user holds down the appropriate button.

- - -

<a id="dnas"></a>
### DNAS

**D**ynamic **N**etwork **A**uthentication **S**ystem is a proprietary Sony authentication system used by the PS2 to verify the console and game when connecting to online services. It can use information about the console hardware and software for authentication, copy protection, and game data management.

- - -

<a id="dongle"></a>
### Dongle

A dongle is a hardware device used to provide authentication or other security functions. In the PS2, a dongle can take the form of a device similar to a [PS2 Memory Card](#ps2mc), but unlike a regular Memory Card, its primary purpose is to authenticate the system rather than to store user data.

The **COH-H10020 Security Dongle** is a special type of memory card used by the arcade [models](#models), which served as a core peripheral of the **Namco System246**, **System256**, and **Konami Python1** units. It uses different firmware for its controller chip and is authenticated by the arcade version of the [MechaCon](#mechacon). The dongle stores a bootloader provided by Sony, as well as the game software and system drivers.

- - -

<a id="dragon"></a>
### Dragon

See the [MechaCon](#mechacon) entry for more information.

- - -

<a id="dsp"></a>
### DSP

**D**igital **S**ignal **P**rocessor is a chip responsible for signal processing in the PS2 optical disc drive. Some DSP revisions, most notably the **CXD3098Q**, can cause the [MechaCon](#mechacon) to crash when reading certain discs, potentially resulting in damage to the laser's focus/tracking coils and their driver IC.

- - -

<a id="dtlh"></a>
### DTL-H

See the [models](#models) entry for more information.

- - -

<a id="dtlt"></a>
### DTL-T

See the [models](#models) entry for more information.

- - -

### DVDROM

DVDROM is one of the chips that contains the [firmware](#firmware) used by PS2 consoles.

- - -

<a id="dvdv"></a>
### DVDV

DVDV is unofficial an abbreviation for [DVD-Video](https://en.wikipedia.org/wiki/DVD-Video).

- - -

<a id="dvr"></a>
### DVR

See the [models](#models) entry for more information.

- - -

<a id="dvrp"></a>
### DVRP

**D**igital **V**ideo **R**ecording **P**rocessor is a dedicated co-processor used exclusively in the DESR [models](#models). It is responsible for most [DVR](#dvr) functionality, as well as handling HDD access and various DRM and security-related functions. It is based on the **Fujitsu MB91302A** microcontroller and runs [firmware](#firmware) stored on an external NOR flash. The firmware can be updated using [UDM](#udm) packages, although there is no official method for updating the DVRP firmware directly. It can be updated using homebrew software or official system update discs, which update the entire system, including the DVRP firmware along with other system data.

- - -

<a id="ecc-non-ecc"></a>
### ECC / non-ECC

**E**rror **C**orrection **C**ode is additional data used to detect and correct errors caused by physical memory. A standard [PS2MC](#ps2mc) uses 512-byte data pages with an additional 16-byte area containing ECC and other metadata, making each physical page 528 bytes in total. A **non-ECC** memory card image contains only the 512-byte data portion of each page, without the additional ECC data. This is the format used by [MMCE](#mmce) devices such as [SD2PSX](#mmce) or applications like [OPL](#opl). This distinction is important when working with [VMC](#vmc): a memory card image containing ECC data cannot normally be used where, for example, an MMCE expects a non-ECC image, and vice versa.

- - -

### EE

See the [Emotion Engine](#ee) entry for more information.

- - -

<a id="eeprom"></a>
### EEPROM

**E**lectrically **E**rasable **P**rogrammable **R**ead-**O**nly **M**emory is a type of non-volatile memory used by the PS2 to store small amounts of system-specific data. Depending on the console model and [MechaCon](#mechacon) version, this includes drive calibration data, the console model, PS2 ID, DVD Player settings, [OSDSYS](#osdsys) configuration, and other hardware- and region-specific data.

- - -

<a id="elf"></a>
### ELF

ELF is the native executable file format for the PS2. On the [Emotion Engine](#ee) side, `*.elf` files are executed, while on the [IOP](#iop) side, `*.irx` files are used.

You may have already come across other extensions. This is because executable files can be signed and/or encrypted, depending on their intended purpose. There is no strict naming convention here, as even Sony used different extensions... For example, files in installation packages:

| | |
|-|-|
| *.xlf | for `hdd0:/PP.*`, `hdd0:/PC.*`, and system (`hdd0:/__*`, `hdd0:/.__*`) partitions |
| *.xin | for the `hdd0:/__mbr` partition |

On a [PS2 Memory Card](#ps2mc), however, the files are signed but still use the `*.elf` extension. Similarly, after installation on a hard drive, they also use `*.elf`.

An old, scene-specific, but still widely used extension is `*.kelf`, although it is gradually being replaced by `*.xlf` (in theory, the same could apply to `*.kirx`, but so far, they haven't been used anywhere by any software).

- - -

<a id="ee"></a>
### Emotion Engine

**E**motion **E**ngine is the main processor of the PlayStation 2. It is a MIPS R5900-based processor responsible for executing the main program code and coordinating most of the console's processing. It also integrates two Vector Units (VUs) and a Graphics Interface (GIF), which are used for tasks such as vector processing and transferring data to the [Graphics Synthesizer](#gs).

- - -

<a id="emu"></a>
### EMU

**Emu**lator is a software that imitates the behavior of a different system, allowing software designed for one platform, such as a game console, to run on another platform. Emulators can also emulate peripherals, such as joypads (e.g. [BlueRetro](https://github.com/darthcloud/BlueRetro)) or [memory cards](#mmce).

Few examples of **PlayStation** emulators:

| Project Name                                             | Target Platform |
|-|-|
| [DKWDRV](https://github.com/DKWDRV/DKWDRV)               | PS2 |
| [Ember](https://github.com/Gageformer/Ember)             | PS2 |
| [POPS](#pops)                                            | PS2 |
| [PS2PSXe]()                                              | PS2 |

Few examples of **PlayStation 2** emulators:

| Project Name                                             | Target Platform |
|-|-|
| [Iris](https://github.com/allkern/iris)                  | PC |
| [PCSX2](https://pcsx2.net/)                              | PC |
| [PCSX2x6](https://github.com/PS2Homebrew-arcade/pcsx2x6) | PC |

- - -

<a id="esr"></a>
### ESR

**E**verybody **S**eeks **R**edemption is a homebrew game loader application. Its main variants are [CLI](#cli)-based (R9b/R9c/R10f); there are two official [GUI](#gui)s (GUI TEST2 light/dark) and one GUI that supports all major CLI versions (ESR Launcher).

ESR expects a **Fake DVD-Video** (so-called **ESR Disc**) containing the game. Normally, the disc drive only passes through, for example, a DVD-R with non-game content -- it checks whether the [UDF](#udf) table contains DVD-Video files. The ESR Patcher (an application that modifies disc images) therefore leaves [ISO9660](#iso9660) intact while modifying UDF to make it look like a real DVD-Video disc, thereby fooling the drive.

- - -

### ESR Disc

See the [ESR](#esr) entry for more information.

- - -

### exFAT

exFAT is one of the [file system](#fs) formats that can be used on storage media. You can read about where and when it can be used in the following guide: [Internal Storage vs. External Storage](Internal%20Storage%20vs%20External%20Storage.md).

- - -

### Fake DVD-Video

See the [ESR](#esr) entry for more information.

- - -

### FAT12 / FAT16 / FAT32

The FAT family consists of [file system](#fs) formats that can be used on storage media. You can read about where and when it can be used in the following guide: [Internal Storage vs. External Storage](Internal%20Storage%20vs%20External%20Storage.md).

- - -

<a id="fdvdb"></a>
### FDVDB

**F**ree **DVD** **B**oot is a DVD Player exploit.

I recommend reading the following guide: [How to Hack PlayStation 2 in 2026](How%20to%20Hack%20a%20PlayStation%202%20in%202026.md).

- - -

<a id="fhdb"></a>
### FHDB

**F**ree **HDB**oot is an [OSDSYS and HDD OSD](#osdsys) patcher. All versions are usually installed as a [System Update](#osdupd).

I recommend reading the following guide: [How to Hack PlayStation 2 in 2026](How%20to%20Hack%20a%20PlayStation%202%20in%202026.md).

- - -

<a id="filesystem"></a>
### File System

A file system is a method used to organize, store, and manage data on storage media. It defines how files and directories are created, stored, and accessed by an operating system or other software. Different file systems have different limitations, such as allowed characters in file and directory names, maximum file sizes, and the size of storage media or partitions they can be used on.

I recommend reading the following guide:  [Internal Storage vs. External Storage](Internal%20Storage%20vs%20External%20Storage.md).

- - -

<a id="firmware"></a>
### Firmware

Firmware is software permanently stored in a device's memory that provides low-level functionality and controls how the hardware operates. In standard PS2 models, including **SCPH** (retail units), **DTL-H** (debug kits), and **KDL** (TVs), the firmware is stored in dedicated chips (**BOOTROM**, **DVDROM**, and **[NVM](#eeprom)**) and is responsible for initializing the hardware and providing the basic functionality required to start the system. In the case of **DESR** ([DVRs](#dvr)), **DTL-T** (dev kits), and **COH** (arcades), the firmware is also stored in a few additional chips.

- - -

<a id="fmcb"></a>
### FMCB

**F**ree **McB**oot is an [OSDSYS](#osdsys) patcher. Up to and including version 1.8c, it was also an exploit. All versions are usually installed as a [System Update](#osdupd).

I recommend reading the following guide: [How to Hack PlayStation 2 in 2026](How%20to%20Hack%20a%20PlayStation%202%20in%202026.md).

- - -

### FS

FS is an abbreviation for [file system](#fs).

- - -

<a id="ftp"></a>
### FTP

**F**ile **T**ransfer **P**rotocol is a network protocol used to transfer files between devices.

- - -

### FW

FW is an abbreviation for [firmware](#firmware).

- - -

<a id="gameid"></a>
### GameID

Sony assigns a unique catalog number to every licensed game, with a separate number for each region and edition. On the box and disc label, it takes the form `SCES-12345`, while on the disc it is used as the executable filename: `SCES_123.45`. Each game with a specific **GameID** also looks for its save using a corresponding name on the memory card, e.g. `mc0:/BESCES_12345/BESCES_12345`.

Devices such as [MMCE](#mmce), together with a game loader (e.g. [OPL](#opl)), use the GameID to determine the [VMC](#vmc) for each game.

- - -

<a id="gpt"></a>
### GPT

GPT is one of the [partition table](#pt) formats that can be used on storage media. You can read about where and when it can be used in the following guide: [Internal Storage vs. External Storage](Internal%20Storage%20vs%20External%20Storage.md).

- - -

<a id="gs"></a>
### Graphics Synthesizer

**G**raphics **S**ynthesizer is the main graphics processor of the PlayStation 2. It is responsible for rendering graphics and generating video output. The GS receives graphics data from the [Emotion Engine](#ee) through the Graphics Interface (GIF) and uses its own 4 MiB of embedded **eDRAM** as video memory (**VRAM**) to store and process framebuffer data, textures, and other graphics-related data.

- - -

### GS

See the [Graphics Synthesizer](#gs) entry for more information.

- - -

<a id="gsm"></a>
### GSM

**G**raphics **S**ynthesizer **M**ode Selector is a homebrew application for upscaling video output.

- - -

<a id="gui"></a>
### GUI

**G**raphical **U**ser **I**nterface allows users to interact with software through graphical elements such as windows, buttons, menus, and icons.

You can read more on [Wikipedia](https://en.wikipedia.org/wiki/Graphical_user_interface).

- - -

<a id="hdd"></a>
### HDD

**H**ard **D**isk **D**rive is a storage device that uses magnetic disks to store data. In the PS2, HDDs can be connected internally through a [Network Adaptor](#nwa) or used externally with compatible models.

- - -

<a id="hddid"></a>
### HDD ID

**HDD ID** is a sector located in the [Service Area](#servicearea) of original hard drives sold by Sony with DESR and DTL-H [models](#models), the Linux Kit, and [PSBBN](#psbbn). It is used for drive encryption on DESR models.

- - -

### HDD OSD

See the [OSDSYS](#osdsys) entry for more information.

- - -

<a id="hhd"></a>
### HHD / SHDD / SSHD

**H**ybrid **H**ard **D**rive is a storage device combining an HDD and flash memory in a single physical drive. The flash memory is typically used as a cache for frequently accessed data, providing some of the performance benefits of an SSD while retaining the capacity of an HDD.

- - -

<a id="hosdm"></a>
### HOSDM

**HOSDM**enu is an [HDD OSD](#osdsys) patcher. It is usually started by [OSDMBR](#osdmbr), [PS2BBL](#ps2bbl), or [PS2BBLE](#ps2bble).

I recommend reading the following guide: [How to Hack PlayStation 2 in 2026](How%20to%20Hack%20a%20PlayStation%202%20in%202026.md).

- - -

### HOSDSYS

See the [OSDSYS](#osdsys) entry for more information.

- - -

### HW

Abbreviation for hardware.

- - -

<a id="ilink"></a>
### i.Link

i.Link is Sony's implementation of the **IEEE 1394** standard, commonly known as **FireWire 400**. It provides high-speed data transfer and is available on selected PS2 models. Devices connected via i.Link may require external power, as the power supplied by the PS2's i.Link port is not sufficient for all devices.

Models equipped with an i.Link port: SCPH-**3**XXXX

- - -

<a id="ihdd"></a>
### iHDD

iHDD is an abbreviation for **I**nternal **HDD**. It is rarely used.

- - -

<a id="ide"></a>
### IDE

**I**ntegrated **D**rive **E**lectronics is a standard for connecting storage devices, commonly used for [PATA](#pata) interfaces.

- - -

### IRX

See the [ELF](#elf) entry for more information.

- - -

<a id="iop"></a>
### IOP

**I**/**O** **P**rocessor is a secondary processor in the PS2 responsible for handling input/output operations and controlling various peripherals. In older models, it is based on the MIPS R3000A architecture and is also used to maintain compatibility with PlayStation hardware. Starting with [SCPH](#models)-75K models, it was replaced by [Deckard](#deckard), which emulates it.

- - -

<a id="iso9660"></a>
### ISO9660

ISO9660 is the [file system](#fs) used on [PSXCD](#psxcd) (Mode 2: 2366), [PS2CD](#ps2cd) (Mode 2: 2352) and [PS2DVD](#ps2dvd) (Mode 1: 2048) discs. Both PS1 and PS2 use the 8.3 Level 1 variant.

See the [Mode](#mode) entry for more information.

- - -

<a id="kdl"></a>
### KDL

See the [models](#models) entry for more information.

- - -

### KELF

See the [ELF](#elf) entry for more information.

- - -

### KIRX

See the [ELF](#elf) entry for more information.

- - -

<a id="lb"></a>
### LB

**L**oad**B**OOTer is a minimalistic loader whose only purpose is to start `mc?:/BOOT/BOOT.ELF`. It is used as a [System Update](#osdupd) executable replacement to significantly reduce the installation size.

- - -

<a id="lbfn"></a>
### LbFn

**LbFn** is a homebrew file manager application.

- - -

<a id="mg"></a>
### MagicGate

**M**agic**G**ate is a Sony copy-protection technology used by the PS2 to authenticate [PS2 Memory Cards](#ps2mc) and protect certain data stored on them, as well as for the encryption of [XLF](#elf) and [XRX](#elf) files. It uses cryptographic keys shared between the console and the Memory Card, with different key sets used for retail, development, prototype, and arcade systems (one is currently unknown).

- - -

<a id="masterdisc"></a>
### Master Disc

A disc image patched in a way that allows it to be recognized and accepted by DTL-H [models](#models). It is also used by [MechaPwn](#mechapwn).

- - -

<a id="mbr"></a>
### MBR

MBR is one of the [partition table](#pt) formats that can be used on storage media. You can read about where and when it can be used in the following guide: [Internal Storage vs. External Storage](Internal%20Storage%20vs%20External%20Storage.md).

- - -

<a id="mca"></a>
### MCA

**M**emory **C**ard **A**nnihilator is a homebrew application for formatting memory cards and creating or restoring their images.

- - -

### MCP2

See the [MMCE](#mmce) entry for more information.

- - -

<a id="mcfs"></a>
### MCFS

**M**emory **C**ard **F**ile **S**ystem is the official [file system](#fs) used on [PlayStation 2 Memory Cards](#ps2mc).

- - -

<a id="mechacon"></a>
### MechaCon

**Mecha**nics **Con**troller is a dedicated microcontroller responsible primarily for controlling the PS2 optical drive. It also handles various security-related functions, including game disc authentication, [MagicGate](#mg), and [XLF](#elf) decryption. On SCPH-500XX and later [models](#models), MechaCon (Dragon) also inherited the functionality of the [SysCon](#syscon) chip, which was removed from the system. It can load patches from [NVM](#nvm), a feature exploited by [MechaPwn](#mechapwn).

- - -

<a id="mechapwn"></a>
### MechaPwn

**MechaPwn** is a homebrew application that exploits an update feature of the Dragon [MechaCon](#mechacon) to modify its region and configuration flags. Depending on the [model](#models), it can disable PS1/PS2 disc region checks, change the console's reported region, and the [OSDSYS](#osdsys) and DVD Player regions.

I recommend reading the following guide: [How to Hack PlayStation 2 in 2026](How%20to%20Hack%20a%20PlayStation%202%20in%202026.md).

- - -

### MG

See the [MagicGate](#mg) entry for more information.

- - -

### MicroSD / uSD / μSD

See the [SD Card](#sdcard) entry for more information.

- - -

<a id="mmce"></a>
### MMCE

**M**ultipurpose **M**emory **C**ard **E**mulator, which, as the name suggests, is an emulator of the PlayStation and PlayStation 2 Memory Card. Examples include **SD2PSX** ([original DIY project](https://sd2psx.net/)), **Kaico SD2psx**, **Bitfunx PSxMemCard Gen2** (and Gen1), and **8BitMods MemCard PRO2**. An MMCE imitates a real memory card, so the console sees it as a real one or even an arcade dongle, providing 100% compatibility with all models.

Every MMCE uses [VMC](#vmc) files stored on a [MicroSD](#sdcard) card, exposing each one (one at a time) to the console as a real memory card. Every MMCE also uses the **MMCE communication protocol**, which allows applications that support it to, for example, access its SD card directly (see [mount points](#mount-point)).

I recommend reading the following guide: [Everything You Need to Know About SD2PSX](Everything%20You%20Need%20to%20Know%20About%20SD2PSX.md).

- - -

<a id="modchip"></a>
### Modchip

A modchip is a special chip soldered to the console that tricks the PS2 optical drive into believing that the program being run is on a CD/DVD-ROM, when it is actually on a CD/DVD-R (greatly simplified, of course). The best modchips were **Crystal Chip**, **DMS**, and **Matrix Infinity**. None of these are currently in production. The most popular modchips were and still are their cheap clones, such as **Modbo** and **Ripper**.

- - -

<a id="mode"></a>
### Mode

In the context of **game loaders**, Mode refers to special modes that add or remove specific patches.

In the context of [modchips](#modchip), Mode refers to [DEV1](#dev1)/[DEV2](#dev2)/[DEV3](#dev3)/[DEV4](#dev4) features.

In the context of a [file system](#fs) on an **optical disc**, Mode refers to the sector size (e.g. 2048, 2366, or 2352 bytes).

- - -

<a id="models"></a>
### Models

The primary way to identify PS2 models is by the designation found on the console's sticker and packaging. However, it is worth noting that this is not always precise, as significant differences may exist within the same model that are relevant to a particular use case, such as the presence of a specific chip or a different [firmware](#firmware) version.

| Series  | Description                                  | Examples |
|-|-|-|
| `SCPH`  | Retail models                                | `SCPH-10000`, `SCPH-90004` etc. |
| `DESR`  | DVR models                                   | `DESR-7700` etc. |
| `KDL`   | TV model with an integrated PS2              | `KDL-22PX300` |
| `DTL-T` | Development kits, also known as **PS2 TOOL** | `DTL-T10000` etc. |
| `DTL-H` | Debug kits, also known as **PS2 TEST**       | `DTL-H10000` etc. |
| `COH`   | Arcade models                                | `COH-H30000` etc. |

**Note**: The last two digits in **SCPH** series are the region code. In the homebrew scene, entire series are commonly referred to as SCPH-**10K**, **30K**, **70K**, and **90K**.

Unfortunately, even motherboard designations (`GH-<number>`) are not always sufficient, and modchip manufacturers developed their own unofficial naming system. If you have ever come across terms such as v1 or v13, these are the designations we are referring to.

And Sony, of course, has its own precise identification system (**Chassis Type**), which is well documented for the so-called **Fat** models (SCPH-10K to SCPH-50K). Chassis designations also exist for the so-called **Slim** models (SCPH-70K and later), but they are much less well documented and are primarily indicated by a small chassis type indicator on the console's label.

Chassis is the official name for a specific hardware revision of the PS2. It describes the console's physical and electronic design, including the motherboard, optical drive, and other components. Multiple models may use the same chassis, while the same model may have been produced with different chassis revisions.

For more information, I recommend visiting the following pages:

- [Chassis types](https://www.psdevwiki.com/ps2/index.php/Chassis_types)
- [Motherboards](https://www.psdevwiki.com/ps2/index.php?section=43&title=Motherboards)
- [SKU Models](https://www.psdevwiki.com/ps2/SKU_Models)

- - -

<a id="mp"></a>
### Mount Points

In the PS2 environment, mount points usually correspond to devices. Depending on the software and logical structure, the same devices may have different mount point names.

| | | |
|-|-|-|
| `cdfs:/`     | Optical Disc Drive.                                             | All homebrew software |
| `cdrom0:\`   | Optical Disc Drive.                                             | CDVDMAN |
| `mc0:/`      | PS1/PS2 Memory Card in the 1st slot                             | All software |
| `mc1:/`      | PS1/PS2 Memory Card in the 2nd slot                             | All software |
| `mc?:/`      | PS1/PS2 Memory Card in any slot                                 | All software |
| `mass:/`     | All [BDM](#bdm) devices                                         | All legacy homebrew software |
| `mass*:/`    | All [BDM](#bdm) devices (e.g. `mass0:/`)                        | Some legacy homebrew software |
| `usb:/`      | [USB](#usb) devices                                             | wLE R3Z, oLE |
| `usb*:/`     | [USB](#usb) devices if more than one (e.g. `usb0:/`)            | wLE R3Z, oLE, OSDM, PS2BBLE |
| `ilink:/`    | [i.Link](#ilink)                                                | wLE R3Z, oLE, OSDM, PS2BBLE |
| `mx4sio:/`   | [MX4SIO](#mx4sio)                                               | wLE ISR, wLE R3Z, oLE, OSDM, PS2BBLE |
| `mmce0:/`    | [MMCE](#mmce) in the 1st slot                                   | wLE ISR, wLE R3Z, oLE, OSDM, PS2BBL, PS2BBLE |
| `mmce1:/`    | [MMCE](#mmce) in the 2nd slot                                   | wLE ISR, wLE R3Z, oLE, OSDM, PS2BBL, PS2BBLE |
| `hdd0:/`     | Internal HDD ([APA](#apa)/[APAJ](#apajail)) on 1st IDE channel  | Some legacy homebrew software |
| `hdd1:/`     | Internal HDD ([APA](#apa)/[APAJ](#apajail)) on 2nd IDE channel  | wLE R3Z, oLE |
| `dvr_hdd0:/` | Internal HDD ([APA](#apa)) on 1st IDE channel but 2nd APA index | wLE, wLE R3Z, oLE |
| `ata0:/`     | Internal HDD ([BDM](#bdm)/[APAJ](#apajail)) on 1st IDE channel  | wLE R3Z, oLE |
| `ata1:/`     | Internal HDD ([BDM](#bdm)/[APAJ](#apajail)) on 2nd IDE channel  | wLE R3Z, oLE |
| `xfrom0:/`   | Internal flash                                                  | wLE XFW, wLE R3Z, oLE, XOSDMBR |

**Note 1:** `ilink:/` is availble only on SCPH-30K [models](#models).<br />
**Note 2:** `dvr_hdd0` is availble only on DESR [models](#models).<br />
**Note 3:** `xfrom0:/` is availble only on SCPH-50K (hypothetically via the [Network Adaptor](#nwa)) and DESR [models](#models).

- - -

### MPWN

See the [MechaPwn](#mechapwn) entry for more information.

- - -

<a id="mx4sio"></a>
### MX4SIO 

A storage device connected to **SIO2** (the interface to which ports such as the Memory Card ports are connected), just like a genuine Memory Card or an MMCE. MX4SIO is the conceptual predecessor of [MMCE](#mmce). It is intended exclusively for gaming and cannot emulate a [PlayStation 2 Memory Card](#ps2mc).

- - -

### NA / NWA

See the [Network Adaptor](#nwa) entry for more information.

- - -

<a id="nbd"></a>
### NBD

**N**etwork **B**lock **D**evice is a protocol that allows block devices to be accessed directly over a network.

- - -

<a id="nwa"></a>
### Network Adaptor

A **N**etwork **A**daptor is an expansion device that provides the PlayStation 2 with network connectivity. The original Sony NA supports Ethernet and, on [models](#models) equipped with an [IDE](#ide) interface, also provides a connection for an internal hard disk drive. The NA can be connected to SCPH-30K and SCPH-50K models; on newer models, it is built in, but without the possibility of connecting a [PATA](https://en.wikipedia.org/wiki/Parallel_ATA) drive as on older models (with the exception of SCPH-700XX, which requires hard soldering). On SCPH-10K models, the NA cannot be connected, as they have their own dedicated external HDD connected via [PCMCIA](https://en.wikipedia.org/wiki/PCMCIA).

[SATA](https://en.wikipedia.org/wiki/SATA) disks can be connected, but only using unlicensed Network Adaptors (not recommended because they do not fully imitate the original and are not fully compatible with all software), or by using so-called SATA boards for the original NA.

- - -

<a id="ntr"></a>
### NTR

**N**eu**tr**ino is a homebrew application, mainly used for playing games from disc images. While it is a [CLI](#cli) application, it needs to be run with arguments or via a dedicated [GUI](#gui).

I recommend reading the following guide: [Neutrino GUI Flavors](Neutrino%20GUI%20Flavors.md).

- - -

### NVM

See the [EEPROM](#eeprom) entry for more information.

- - -

### NVRAM

See the [EEPROM](#eeprom) entry for more information.

- - -

<a id="odd"></a>
### ODD

ODD is an abbreviation for **O**ptical **D**isc **D**rive.

- - -

<a id="odde"></a>
### ODE / ODDE

ODDE is an abbreviation for **O**ptical **D**isc **D**rive **E**mulator. Currently, no such device exists for the PS2.

- - -

<a id="ofw"></a>
### OFW

**O**fficial **F**irm**w**are is the original, unmodified [firmware](#firmware) provided by the manufacturer.

- - -

<a id="ole"></a>
### OLE

**O**mni **L**aunch**E**LF is a homebrew file manager application.

I recommend reading the following guide: [unofficial LaunchELF Flavors](App%20Flavors%20-%20unofficial%20LaunchELF.md).

- - -

<a id="opl"></a>
### OPL

**O**pen **P**S2 **L**oader is a homebrew application for playing games from disc images.

I recommend reading the following guide: [Open PS2 Loader Flavors](App%20Flavors%20-%20Open%20PS2%20Loader.md).

- - -

### OPNPS2LD

Old abbreviation for **Op**e**n PS**2 **L**oa**d**er. It is still in use in some environments.

See the [OPL](#opl) entry for more information.

- - -

<a id="osdsys"></a>
### OSDSYS

OSDSYS is the official [dashboard](#dashboard) called **PS2 Browser**, and is part of the [firmware](#firmware). 

While Sony left itself the possibility of updating OSDSYS, it never used it except in the case of the so-called **HDD OSD** (a version of OSDSYS with support for internal storage, allowing games and applications to be launched from it; also known as **HOSDSYS**). The homebrew scene made extensive use of this, most notably in the form of [FMCB](#fmcb)/[FHDB](#fhdb) and [OSDM](#osdm)/[HOSDM](#hosdm).

- - -

<a id="osdupd"></a>
### OSD Update

The official mechanism for loading firmware patches and replacements from a [PS2MC](#ps2mc). Another term often used for this mechanism is **System Update**. Homebrew programs use it to e.g. modify [OSDSYS](#osdsys). The most commonly installed program as a OSD Update is [FMCB](#fmcb).

- - -

<a id="osdm"></a>
### OSDM

**OSDM**enu is an [OSDSYS](#osdsys) patcher. It is usually started by [LB](#lb), [ProtoPwn](#protopwn), [PS2BBL](#ps2bbl), or [PS2BBLE](#ps2bble).

I recommend reading the following guide: [How to Hack PlayStation 2 in 2026](How%20to%20Hack%20a%20PlayStation%202%20in%202026.md).

- - -

<a id="osdmbr"></a>
### OSDMBR

OSDMBR is an advanced [bootstrap](#bootstrap) used to initialize hardware and launch programs. It is installed inside `hdd0:/__mbr`.

I recommend reading the following guide: [How to Hack PlayStation 2 in 2026](How%20to%20Hack%20a%20PlayStation%202%20in%202026.md).

- - -

<a id="osdxmb"></a>
### OSDXMB

**OSD**-**XMB** is a [dashboard](#dashboard) that aims to replicate the [XMB](#xmb) known from the [PS3](#consoles) as faithfully as possible. It was written using [Athena](), a **JavaScript** runtime environment, so both OSD-XMB itself and all its plugins are written in **JavaScript**.

- - -

<a id="osk"></a>
### OSK

**O**n-**S**creen **K**eyboard is a virtual keyboard displayed on screen that allows users to enter text using a controller, mouse, or other input device instead of a physical keyboard.

- - -

<a id="pata"></a>
### PATA

**P**arallel **A**dvanced **T**echnology **A**ttachment is a standard for connecting storage devices using a parallel data interface. It is also commonly known as [IDE](#ide). Original disks for SCPH, DESR, and DTL-H [models](#models) have special [firmware](#firmware) required for some functionality.

- - -

<a id="pt"></a>
### Partition Table

A partition table is a data structure stored on a storage device that describes the partitions on it, including their locations, sizes, and types. Common partition table formats include [MBR](#mbr) and [GPT](#gpt); however, natively, the PS2 has its own, [APA](#apa).

- - -

<a id="pcmcia"></a>
### PCMCIA

**P**ersonal **C**omputer **M**emory **C**ard **I**nternational **A**ssociation is a standard for expansion cards originally developed for portable computers. The term is also commonly used to refer to the physical card interface and its associated form factor.

- - -

<a id="pfs"></a>
### PFS

**P**layStation **F**ile **S**ystem is official [file system](#fs) used on [APA](#apa)-formatted internal storage.

On newer Sony consoles, such as the [PSV/PSTV](#consoles), [PS4](#consoles), and [PS5](#consoles), PFS refers not to a file system, but to a special encrypted container for various types of data. Do not confuse PFS on the PS2 with PFS on other consoles. These are two completely different things.

- - -

<a id="pgif"></a>
### PGIF

**P**layStation **G**raphics **I**nter**f**ace (not an official abbreviation) is a hardware interface used by the PS2 to communicate with the emulated PlayStation GPU. It is primarily used by [PS1DRV](#emu) when running PlayStation games. On [Deckard](#deckard) models, it is fully emulated.

- - -

<a id="pmap"></a>
### PMAP

**P**layStation **2** **M**echacon **A**djustment **P**rogram is a tool for calibrating and adjusting the optical disc drive. It allows both electrical and mechanical adjustment, including laser calibration and skew adjustment.

- - -

<a id="pops"></a>
### POPS

**POPS** is the first PlayStation emulator ever designed by Sony, officially distributed with the game Bishi Bashi Special 3 on one of the [PSBBN](#psbbn) channels. The homebrew scene was able to decrypt it, and it is still used as the main PS1 emulator, with patches applied on the fly by [POPStarter](#popstarter).

- - -

<a id="popsldr"></a>
### POPSLoader

A [GUI](#gui) for [POPStarter](#popstarter) that makes it user-friendly and easier to use.

- - -

<a id="popstarter"></a>
### POPStarter

A patcher for [POPS](#pops) that significantly extends its functionality.

- - -

<a id="protopwn"></a>
### ProtoPwn

**ProtoPwn** is an exploit for so-called protokernel [models](#models) that exploits a vulnerability in the [OSDSYS](#osdsys) update code to enable arbitrary code execution.

I recommend reading the following guide: [How to Hack PlayStation 2 in 2026](How%20to%20Hack%20a%20PlayStation%202%20in%202026.md).

- - -

### PS2 Browser

See the [OSDSYS](#osdsys) entry for more information.

- - -

<a id="ps1mc"></a>
### PS1MC

[PlayStation Memory Card](https://www.psdevwiki.com/ps1/Memory_Card). You may also come across the **PSXMC** acronym. It is the official and only device on which you can **save** PS1 games.

- - -

<a id="ps2mc"></a>
### PS2MC

[PlayStation 2 Memory Card](https://www.psdevwiki.com/ps2/Memory_Card). It is the official and only device on which you can **save** PS2 games (except for a few game titles that allowed saving to the internal disk).

Because the PS2MC has a [file system](#fs) (called [MCFS](#mcfs)), users can also **store** PS1 saves on it, like any other data, for example, a [System Update](#osdupd).

- - -

<a id="ps2bbl"></a>
### PS2BBL

**P**lay**S**tation **2** **B**asic **B**oot **L**oader is a simple application whose purpose is to initialize the hardware and launch other programs.

- - -

<a id="ps2bble"></a>
### PS2BBLE

**P**lay**S**tation **2** **B**asic **B**oot **L**oader **E**xtended is a simple application whose purpose is to initialize the hardware and launch other programs. It has a GUI and includes several new features (additional search paths, a clock, temperature display, etc.).

- - -

<a id="psbbn"></a>
### PSBBN
**P**lay**S**tation **B**road**b**and **N**avigator is an optional Linux distribution that served as a [dashboard](#dashboard) for Japanese models. It has the same functionality as [HDD OSD](#osdsys), but also allows users to access and download content from the internet. We can say that PSBBN was a precursor to the PlayStation Store, which later appeared on other Sony consoles.

For unknown reasons, ;) PSBBN is often confused with PS2BBL. Both are completely different things.

- - -

<a id="psbbndp"></a>
### PSBBN DP / PSBBN DEP

**PSBBN D**efinitive **P**atch (older name: **PSBBN D**efinitive **E**nglish **P**atch) is a toolkit that reformats the entire internal drive to [APA-Jail](#apajail), installs [PSBBN](#psbbn), and translates it into various of languages.

- - -

<a id="ps2cd"></a>
### PS2CD

PS2CD is a disc containing a PlayStation 2 game distributed on a [Compact Disc](https://en.wikipedia.org/wiki/Compact_disc). The term usually refers to the original media (PS2CD-ROM, so-called "blue disc").

- - -

<a id="ps2dvd"></a>
### PS2DVD

PS2DVD is a disc containing a PlayStation 2 game distributed on a [Digital Versatile Disc](https://en.wikipedia.org/wiki/DVD). The term usually refers to the original media (PS2DVD-ROM, so-called "yellow disc").

- - -

<a id="ps2l"></a>
### PS2L

**PS2** **L**auncher is a fork of Open PS2 Loader, a homebrew application for playing games from disc images.

I recommend reading the following guide: [Open PS2 Loader Flavors](App%20Flavors%20-%20Open%20PS2%20Loader.md).

- - -

<a id="psxcd"></a>
### PSXCD

PSXCD (or, if you prefer, **PS1CD**) is a disc containing a PlayStation game. The term usually refers to the original media (PSXCD-ROM, so-called "black disc").

- - -

### PSXMC

See the [PS1MC](#ps1mc) entry for more information.

- - -

### PSXMCG1 / PSXMCG2

See the [MMCE](#mmce) entry for more information.

- - -

### PT

See the [Partition Table](#pt) entry for more information.

- - -

<a id="r4d"></a>
### R4D

**R**ecovery **for** **D**ummies is a USB stick image containing various preconfigured software focused on servicing and exploiting the PS2.

- - -

<a id="ram"></a>
### RAM

PS2 [models](#models) use several types of system memory, depending on the model and its purpose.

| Type      | Capacity | Models             | Purpose |
|-|-|-|-|
| RDRAM     | 32 MiB   | SCPH and DTL-H     | standard RAM |
| RDRAM     | 64 MiB   | DESR               | standard RAM |
| RDRAM     | 128 MiB  | DTL-T              | standard RAM |
| EDO RAM   | 2 MiB    | SCPH-70K and older | modules storage |
| EDO RAM   | 4 MiB    | COH                | modules storage |
| EDO RAM   | 8 MiB    | DESR and DTL-T     | modules storage |
| DDR-SDRAM | 4 MiB    | SCPH-75K and newer | modules storage (2 MiB used by Deckard itself) |

Notes:

- Games cannot use the extra RAM. For them, the available address space is always 32 MiB (on the EE side) and 2 MiB (on the IOP/Deckard side).
- DDR-SDRAM replaces EDO RAM in [Deckard](#deckard) models.
- IOP RAM is shorthand for EDO RAM.

- - -

<a id="riptopl"></a>
### RiptOPL

**Ript**o's **O**pen **P**S2 **L**oader is a homebrew application for playing games from disc images.

I recommend reading the following guide: [Open PS2 Loader Flavors](App%20Flavors%20-%20Open%20PS2%20Loader.md).

- - -

<a id="rtc"></a>
### RTC

**R**eal-**T**ime **C**lock is a hardware clock that keeps track of the current date and time. In the PS2, it is powered by a CR2032 coin cell when the console is turned off.

- - -

<a id="sa"></a>
### SA

SA is an abbreviation for [Service Area](#servicearea).

- - -

<a id="sas"></a>
### SAS / mSAS

**S**ave **A**pplication **S**ystem** and **m**icro **S**ave **A**pplication **S**ystem** packages are bundled applications that include metadata and configuration files, allowing users to easily add and remove applications themselves.

I recommend reading the following guide: [SAS and microSAS Packages](SAS%20and%20microSAS%20Packages.md).

- - -

<a id="sata"></a>
### SATA

**S**erial **A**dvanced **T**echnology **A**ttachment is a standard for connecting storage devices using a serial data interface. While it is the successor to [PATA](#pata), connecting a SATA drive to a PS2 requires additional hardware, such as a custom [Network Adaptor](#nwa) or a SATA board for the original one.

- - -

<a id="save-container"></a>
### Save Container

A Save Container is an archive containing a game save. PSX game saves are individual files and, apart from their names, do not contain any other significant metadata. PS2 game saves are folders containing the game save itself, icons, icon metadata, as well as important file timestamps and attributes. To avoid losing any of this information when copying saves to, for example, a USB stick, archiving programs allow them to be packed into formats such as `*.psu`.

**PlayStation** container formats:

| Extension | Native for:               |
|-|-|
| *.mcs     | MemCard Rex, PSXGameEdit  |
| *.psv     | PS3                       |

**PlayStation 2** container formats:

| Extension | Native for:               | Preserve Timestamps |
|-|-|-|
| *.cbs     | Code Breaker              | no  |
| *.max     | Action Replay Max         | no  |
| *.psu     | EMS Linker, PS2 apps      | yes |
| *.psv     | PS3                       | yes |
| *.sps     | GameShark                 | no  |
| *.xps     | Xploder                   | no  |

- - -

<a id="scph"></a>
### SCPH

See the [models](#models) entry for more information.

- - -

<a id="sdcard"></a>
### SD Card

An SD Card is a removable flash memory card used to store data and transfer it between compatible devices. In the context of this guide, SD Cards are primarily used as storage media for PS2-related applications and devices such as [MMCE](#mmce) and [MX4SIO](#mx4sio), but they can also be used as [USB](#usb)/[i.Link](#ilink) storage media via a dedicated reader. Not every SD Card is compatible with MX4SIO/MMCE, for reasons that are currently unknown.

SD Cards are available in different physical formats, with **standard SD** and **MicroSD** being the most common. While MicroSD cards can be used in devices designed for standard SD Cards with a suitable adapter, they should be avoided due to potential compatibility issues.

- - -

### SD2PSX

See the [MMCE](#mmce) entry for more information.

- - -

<a id="sd2psxtd"></a>
### sd2psXtd

[sd2psXtd](https://github.com/sd2psXtd/firmware) is [firmware](#firmware) for [SD2PSX](#mmce) and all devices based on it.

- - -

<a id="servicearea"></a>
### Service Area

**S**ervice **A**rea is a reserved area on a hard drive that contains part of the disk [firmware](#firmware), configuration, and other data used for drive maintenance and operation, including the [HDD ID](#hddid) sector.

- - -

<a id="smb"></a>
### SMB

SMB is a network-based protocol. It is used for streaming disc images and transferring files. The majority of PS2 applications support only SMB v1. Some support SMB v2 ([RiptOPL](#opl)), while some others support SMB v3 ([smbLaunchELF/NETFS](#wle)).

- - -

<a id="sms"></a>
### SMS / SMS3

**S**imple **M**edia **S**ystem is a homebrew media player application. SMS**3** is a reworked modern version, introduced to distinguish the 3.0 line from the old 2.9 version.

- - -

<a id="consoles"></a>
### Sony Consoles

**PS2** is an abbreviation for the **P**lay**S**tation **2** console, which probably needs no explanation. **PSX**, on the other hand, is a bit more complicated, as it comes from the project's codename: **P**lay**S**tation-**X**. Long ago, even before the release of the PlayStation One (i.e. the smaller version of the PSX; not to be confused with the PlayStation Classic), the PSX acronym became commonly used to refer to this console. Later on, the **PS1** abbreviation became increasingly popular -- and today it is the dominant one. Unfortunately for all old farts like me, Sony released a special PS2 model designated **DESR**, which they called... PSX. Throughout any of my guides, whenever you see PSX, it refers exclusively to the PlayStation, because I have a syntactic fetish and reject neologisms. ;)

| | |
|-|-|
| PS1 (PSX :P) | PlayStation |
| PS2          | PlayStation 2 |
| PS3          | PlayStation 3 |
| PS4          | PlayStation 4 |
| PS5          | PlayStation 5 |
| PSC          | PlayStation Classic |
| PSP          | PlayStation Portable |
| PSV/PSTV     | PlayStation Vita/TV |

- - -

<a id="sopl"></a>
### sOPL

**S**table **O**pen **P**S2 **L**oader is a homebrew application for playing games from disc images.

I recommend reading the following guide: [Open PS2 Loader Flavors](App%20Flavors%20-%20Open%20PS2%20Loader.md).

- - -

<a id="ssd"></a>
### SSD

**S**olid-**S**tate **D**rive is a storage device that uses flash memory to store data instead of magnetic disks. SSDs have no moving parts and are generally faster and more resistant to physical shock than HDDs. However, compatibility with the PS2 may vary for unknown reasons.

SSDs are strongly recommended for [HDD OSD](#osdsys) and [PSBBN](#psbbn) because they significantly reduce the time required to parse the [APA](#apa) chain.

- - -

### SW

Abbreviation for softmware.

- - -

<a id="syscon"></a>
### SysCon

**Sys**tem **Con**troller is a **Toshiba TMP87C807U** microcontroller used in early PS2 models to manage various system-level functions, such as power management, front-panel buttons, and thermal management. Starting with the SCPH-50K [models](#models), its functionality was integrated into [Dragon](#mechacon).

- - -

### System Update

See the [OSD Update](#osdupd) entry for more information.

- - -

<a id="udf"></a>
### UDF

**U**niversal **D**isk **F**ormat is the [file system](#fs) used on [PS2DVD](#ps2dvdrom) discs (Mode 1: 2048). The PS2 uses UDF version 1.02.

See the [Mode](#mode) entry for more information.

- - -

<a id="udm"></a>
### UDM

UDM is an official [firmware](#firmware) package format for [DVRP](#dvrp).

- - -

<a id="udpbd"></a>
### UDPBD

UDPBD is a network-based block device protocol. It is used only for streaming disc images.

- - -

<a id="udpfs"></a>
### UDPFS

UDPFS is a network-based protocol. It is used for streaming disc images and transferring files.

- - -

<a id="usb"></a>
### USB

**U**niversal **S**erial **B**us is a standard for connecting peripheral devices and transferring data. The PlayStation 2 is equipped with USB **1.1** ports, so newer USB 2.0 and USB 3.x devices are backward compatible with them, but they cannot operate at their full speed when connected to a PS2. Not every USB device is compatible with the PS2, even if it uses a compatible USB standard.

- - -

<a id="ule"></a>
### uLE / uLaunchELF

**u**nofficial **L**aunch**E**LF is a homebrew file manager application.

I recommend reading the following guide: [unofficial LaunchELF Flavors](App%20Flavors%20-%20unofficial%20LaunchELF.md).

- - -

<a id="uopl"></a>
### uOPL

**u**nofficial **O**pen **P**S2 **L**oader is a homebrew application for playing games from disc images.

I recommend reading the following guide: [Open PS2 Loader Flavors](App%20Flavors%20-%20Open%20PS2%20Loader.md).

- - -

<a id="vmc"></a>
### VMC

A **V**irtual **M**emory **C**ard and a **memory card image** are terms that refer to the same thing and are used interchangeably. Although [Open PS2 Loader](#opl) and [Neutrino](#ntr) have a feature called VMC, it should not be confused with VMC in [MMCE](#mmce). In OPL and Neutrino, VMC is a software feature that provides virtual memory card functionality by modifying the way the game accesses the memory card. In MMCE, VMC refers to a memory card image that is exposed to the console as a genuine memory card, with the emulation performed at the hardware level.

**PlayStation** VMC formats:

| Extension | Native for:               | Raw |
|-|-|-|
| *.ddf     | [VirtualGameSystem](#emu) | no  |
| *.gme     | DexDrive                  | no  |
| *.mc1     | [MCP2](#mmce)             | yes |
| *.mcd     | [SD2PSX](#mmce)           | yes |
| *.mcr     | [ePSXe](#emu)             | yes |
| *.srm     | [RetroArch](#emu)         | yes |
| *.vm1     | [PS3](#consoles)          | yes |
| *.vmc     | [POPS](#pops)             | yes |
| *.vgs     | [VirtualGameSystem](#emu) | no  |
| *.vmp     | [PSP](#consoles)          | no  |

**PlayStation 2** VMC formats:

| Extension | Native for:               | Raw | [ECC](#ecc-non-ecc) | Encryption |
|-|-|-|-|-|
| *.bin     | PS2 apps                  | yes | no  | no  |
| *.mc2     | [MCP2](#mmce)             | yes | no  | no  |
| *.mcd     | [SD2PSX](#mmce)           | yes | no  | no  |
| *.ps2     | [PCSX2](#emu)             | yes | yes | no  |
| *.vm2     | [PS3](#consoles)          | yes | yes | no  |
| *.vme     | [PS3](#consoles)          | yes | yes | yes |

- - -

<a id="wle"></a>
### wLE / wLaunchELF

**double**-**u**nofficial **L**aunch**E**LF is a homebrew file manager application.

I recommend reading the following guide: [unofficial LaunchELF Flavors](App%20Flavors%20-%20unofficial%20LaunchELF.md).

- - -

<a id="wopl"></a>
### wOPL

**Double** **U**nofficial **O**pen **P**S2 **L**oader is a homebrew application for playing games from disc images.

I recommend reading the following guide: [Open PS2 Loader Flavors](App%20Flavors%20-%20Open%20PS2%20Loader.md).

- - -

<a id="x2p"></a>
### X2P

**X**box **to** **P**layStation is a homebrew application for playing games from disc images. Originally, it was an April Fools' joke to disguise [OPL](#opl) as a real Xbox [emulator](#emu).

I recommend reading the following guide: [Open PS2 Loader Flavors](App%20Flavors%20-%20Open%20PS2%20Loader.md).

- - -

<a id="xeb"></a>
### XEB / XEB+

**X**treeme **E**lite **B**oot **Plus** is a [dashboard](#dashboard) that, although it imitates the [XMB](#xmb), prioritizes its multimedia capabilities over its primary purpose of launching applications and offers great flexibility when designing plugins. It was written using [Enceladus](), a **Lua** runtime environment, so both XEB+ itself and all its plugins are written in **Lua**.

- - -

### XIN

See the [ELF](#elf) entry for more information.

- - -

### XLF

See the [ELF](#elf) entry for more information.

- - -

<a id="xmb"></a>
### XMB

**Cross** **M**edia **B**ar is a type of menu first used in [DESR and KDL](#models), later continued on the [PSP and PS3](#consoles), and eventually abandoned on newer models.

- - -

<a id="xosdmbr"></a>
### XOSDMBR

Similar to [OSDMBR](#osdmbr), XOSDMBR is a [bootloader](#bootloader), but it is installed on `xfrom0:/`.

I recommend reading the following guide: [How to Hack PlayStation 2 in 2026](How%20to%20Hack%20a%20PlayStation%202%20in%202026.md).

- - -

<a id="yade"></a>
### YADE

**Y**et **A**nother **D**VD **E**xploit is a DVD Player exploit.

I recommend reading the following guide: [How to Hack PlayStation 2 in 2026](How%20to%20Hack%20a%20PlayStation%202%20in%202026.md).

- - -

<br />Berion<br />2026-09-12

<p align="right"><small>➜ Go back to <a href="index.md">main page</a></small></p>
