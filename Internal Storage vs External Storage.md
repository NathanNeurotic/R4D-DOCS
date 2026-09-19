# Internal Memory vs. External Memory

The **PlayStation 2** does not have an operating system, which means that storage is managed *independently by each application*. Programs can use the firmware's built-in modules, but these are available only for the internal hard drive (excluding the so-called proto kernel models). As a result, the supported logical structures vary depending on both the application and the storage device. In the following sections, I will explain these differences, which can be -- and often are -- confusing for people who are new to the PS2 homebrew scene.

## External Memory

| | |
|-|-|
| **Interface**        | USB, i.Link, SIO2 (via the Memory Card port) |
| **Partition Tables** | MBR, GPT, or none (MMCE supports only MBR) |
| **File Systems**     | FAT12, FAT16, FAT32, exFAT, EXT2 (the latter is supported exclusively by E2OPL) |

### USB

The first form of external storage supported by the **PlayStation 2** was **USB** (i.e. flash drives). Support for USB storage was even implemented in a few games (e.g. “Gran Turismo 4”). Initially, device compatibility was limited and, for some reason, noticeably better when using **FAT16** or even **FAT12** instead of **FAT32**. There was even a time when users swapped different versions of `USBD.IRX`, as a module extracted from a particular game or application would sometimes work with a specific USB device while others would not. Because many of these programs are closed source and have long since been abandoned by their authors, the most universally compatible option remains a flash drive with an **MBR** partition table and **a single partition** formatted with any of the file systems mentioned earlier.

### i.Link (FW400)

With the release of [PS2ESDL](https://sites.google.com/view/ysai187/home/projects/ps2esdl#h.p_DeSddFqr7A1v) (a game loader and one of the alternatives to USB Advance/Extreme and, of course, [Open PS2 Loader](https://github.com/ps2homebrew/Open-PS2-Loader)), support for **i.Link** (a **FireWire 400**-compatible standard) was introduced. The interface was only included in PlayStation 2 models produced during the middle of the console's lifespan (such as the SCPH-30004R) and never gained much popularity. It also requires an external power supply for devices such as hard drives or USB sticks.

### MX4SIO

A few years later, **MX4SIO** joined the family. It is an SDHC/SDXC card reader that plugs into a memory card slot (not to be confused with a **PlayStation 2 Memory Card**, as it is neither a Memory Card nor an emulator of one).

### MMCE

The successor to MX4SIO is **MMCE** (**Multi-purpose Memory Card Emulator**). Like MX4SIO, it provides access to a microSD card, while also emulating a real **PlayStation Memory Card** (PS1MC) or **PlayStation 2 Memory Card** (PS2MC). The selected memory card image is presented to the console as if it were a physical Memory Card.

## Internal Memory

| | |
|-|-|
| **Interface**        | PATA (SATA after board replacement in the Network Adaptor) |
| **Partition Tables** | APA (native), MBR, GPT, or none (the latter three via BDM) |
| **File Systems**     | PFS (native), EXT2 (Linux), RFS 3.5 (Linux), RAW (e.g. game disc images for the PS2), exFAT (the latter via BDM) |

**INTERNAL MEMORY** is a separate world, meaning a **PATA** (**Parallel ATA**) hard disk drive connected either through a **special external enclosure** via **PCMCIA** (SCPH-1xxxx models), a **Network Adaptor** via its dedicated port (SCPH-3xxxx/5xxxx models), or directly to the motherboard if you are skilled enough with a soldering iron ;) (SCPH-700xx models). Even if the Network Adaptor is unlicensed, counterfeit, or uses a replacement board that converts the original PATA interface to the newer **SATA** (**Serial ATA**) standard, such a solution is most often still referred to simply as **IDE** (as this is the commonly used term). You may also encounter the term **iHDD** (from **internal HDD**), but it is rarely used.

<span style="color: #D32F2F;">Connecting a hard drive via USB or i.Link does not make it an internal drive! Connecting, for example, flash card readers (e.g. those soldered directly to the motherboard) can make them an internal storage device. The key factor here is the target interface.</span>

## Partition Tables vs. Partitionless Storage

While users have no choice when it comes to the native environment (APA) or MMCE, BDM and older USB modules leave the question of whether to use a partition table or not. If you intend to use a USB stick with very old applications (e.g. Open PS2 Loader version 0.7), an MBR partition table is mandatory (they do not support GPT, or even a lack of a partition table). However, if you want to use a given device only with modern programs and have no plans to use it for anything other than the PS2 console, you can safely use exFAT directly on the device (starting from LBA0 instead of after the first 512 bytes/1 MiB).

## APA vs. APA-Jail

**APA** is the native storage environment used by the **PlayStation 2** for internal hard disk drives. **APA-Jail**, on the other hand, is a hybrid structure combining APA with MBR or GPT (there are several types of **APAJ**: Type A/A2/A3, Type B/B2/B3, and the abandoned Type C). It is not an official partitioning scheme, but rather an interesting type of hack that creates the world's first hybrid disk at the logical structure level. The purpose of APA-Jail is to maintain 100% compatibility with applications that understand only APA (for example, the PS2 firmware cannot boot **Free HDBoot** without APA), while at the same time allowing the contents of exFAT partitions to be managed from Windows/Linux/macOS without the need for dedicated tools. The PS2 environment cannot see the PC environment (from the PS2 perspective, the entire disk appears to be APA, which is obviously not true), while the PC environment can detect that the PS2 environment exists, although it cannot access it. The area used by the PS2 is encapsulated inside a hidden RAW partition.

For more details, see the `readme.pdf` of the [PS2 HDD Decryption Helper](https://www.psx-place.com/resources/ps2-hdd-decryption-helper.1507/) (**PS2HDH**) project, where the internal structure is described in detail. PS2HDH can format a drive as APA-Jail and can also convert existing APA drives to APA-Jail, although with some limitations. APAJ is widely used in the [PlayStation Broadband Navigator Definitive Project](https://github.com/CosmicScale/PSBBN-Definitive-Project) (**PS2BBN DP**).

## Drivers

As on any platform, dedicated drivers, or more precisely modules, are required to support specific devices and logical structures. Unfortunately, modules that support "everything on everything" do not exist and are unlikely to ever exist.

Currently, we can distinguish three environments:

1. The first supports APA and PFS, i.e. the native partition table and file system -- exclusively on internal memory.
2. The second handles external memory, but without MMCE, as well as internal memory using external-style logical structures (MBR/GPT/none and all FAT variants).
3. The third is MMCE.

To make things even more complicated for the average user, remember that older applications use older modules, and newer ones cannot use them without significant code changes. This means that older applications cannot take advantage of BDM because they rely on dedicated modules for specific devices and file systems, which cannot simply be replaced.

### Block Device Manager (BDM)

**BDM** combines support for USB, i.Link, MX4SIO, and internal drives (excluding native APA/PFS support), including partition tables (in addition to MBR, also GPT) and file systems (such as the recently added exFAT). BDM is the first attempt at driver unification in the PS2 scene.

### MMCEMAN

**MMCEMAN** is used for communication with MMCE, primarily providing access to the microSD card (as of writing, it expects nothing more than FAT32/exFAT on MBR). It does not replace BDM and remains a dedicated driver for MMCE.

### Wrappers

**Some** legacy programs may benefit from so-called wrappers, which act as a translation layer for USB modules, allowing them to support **exFAT on USB**, **i.Link**, **MX4SIO**, **MMCE**, **internal disk**, or even **UDPBD** (a network-based block device protocol).

- [ATA Assault](https://github.com/saildot4k/ATA-Assault) (for exFAT HDD)
- [BDMAssault](https://github.com/israpps/BDMAssault) (for exFAT USB)
- [BDMAssault](https://github.com/israpps/BDMAssault/releases/tag/mx4sio) (for MX4SIO)
- [BDMAssault](https://psx-place.com/threads/bdmassault.42352/post-377562) (for i.Link and UDPBD)
- [MMCEMAN for POPStarter](https://github.com/ps2-mmce/mmceman/releases/tag/popstarter) (for MMCE)

## Cluster & Sector Size

The optimal cluster size for the drivers used on the **PlayStation 2** is **32 KiB**. Do not go below **4 KiB** or above **64 KiB** unless you want to experience performance issues. The cluster size can only be set when formatting **FAT** and **exFAT** file systems. **PFS** always uses its default cluster size.

When it comes to sector size, the drivers and libraries used on the **PlayStation 2** support only **512 B** sectors. A storage device such as a hard disk drive may use a physical sector size of **4 KiB** (so-called **4K** or **Advanced Format**), but it must internally emulate **512 B** sectors (known as **512e**) for compatibility. Native **4096 B** sectors are not supported.

<span style="color: #D32F2F;">Be careful not to confuse the **cluster** size with the **sector** size (a common mistake). The cluster size is defined by the file system and, in theory, can be any value allowed by its specification. The sector size is defined by the device firmware and cannot be changed.</span>

<br />Berion<br />2026-08-01

<p align="right"><small>➜ Go back to <a href="index.md">main page</a></small></p>