# unofficial LaunchELF Flavors

The **LaunchELF** project gave rise to **LbFn** <sup>[[1](https://wiki.nika-2ch.net/?appli/LbFn)] [[2](https://github.com/ps2homebrew/LbFn)]</sup> and a plethora of **unofficial LaunchELF** forks. So many of the latter have been created that it can be difficult for anyone who does not actively follow the so-called scene to choose the right one. Below is a list of uLE versions, arranged in chronological order based on when the projects first appeared. Each entry includes a brief description of how it differs from the others.

*The abbreviated name for **unofficial LaunchELF** is **uLE**, but you may also come across **wLE** (from **double-unofficial LaunchELF**) and **uLaunchELF**/**wLaunchELF**. Throughout the list below, I will use the abbreviated form.*

### uLaunchELF 4.42d <sup>[[1](http://psx-scene.com/forums/f113/unofficial-launchelf-v4-42-a-37242/)] [[2](https://web.archive.org/web/20141104153858/http://psx-scene.com/forums/f113/unofficial-launchelf-v4-42-a-37242/)] </sup>

The last version of uLE developed by *EP* and *Dlanor*, and in my opinion the last thoroughly tested release with the fewest bugs. It is also worth mentioning the experimental **4.40h** version, which is the only release in this line that works with older versions of the PCSX2 emulator (although **wLE** does as well, so there is little point in keeping this one).

### wLaunchELF 4.43a (2019-01-14) <sup>[[1](https://sites.google.com/view/ysai187/home/projects/fmcbfhdb)]</sup>

Thanks primarily to the work of *SP193* and *AkuHak*, the project evolved from version 4.42d, with several longstanding bugs fixed and the libraries and modules updated to the then-latest versions. This release was distributed as part of the FMCB v1.966 package and, in my opinion, is another solid release.

### wLaunchELF v4.43a (rolling release) <sup>[[1](https://github.com/ps2homebrew/wLaunchELF)]</sup>

Development of wLE continued, driven in part by the work of *Balika* and *Julian Uy*, this time without separate stable, thoroughly tested releases. Added support for **2 TiB** HDDs, all **HDD partitions on DESR models** (`dvr_hdd0:/__xdata` and `dvr_hdd0:/__xcontents`), and **fake DVD-Video discs** for **Free DVD Boot** and **ESR**.

### wLaunchELF kHn (2020-08-10) <sup>[[1](https://cdn.discordapp.com/attachments/652863740370485258/742327866854998116/wLE_kHn_20200810.7z)] [[2](https://www.psx-place.com/resources/unofficial-launchelf-khn.1534/)]</sup>

Fork based on one of the wLE versions, modified by *krHACKen*. It allows **renaming any HDD partition** as well as **launching PSX games** from **VCD** disc images (that is, it actually launches **POPStarter** with the appropriate parameters). Versions of wLE kHn were released not only as **ELF**, but also as **XIN** (a signed ELF for the `hdd0:/__mbr` partition), **XLF** (a signed ELF for `hdd0:/PP.*` partitions), a disk image, and a CD image for the so-called Swap Trick.

### wLaunchELF XFW <sup>[[1](https://github.com/xfwcfw/uLaunchELF/commit/927fd4af0467be28ad2070273611f4d33cf31f59)]</sup>

Fork based on one of the wLE versions, modified by *Balika*. Adds support for reading the **internal NAND flash** memory (`xfrom0:/`) on DESR models.

### wLaunchELF ISR 4.43x (rolling release) <sup>[[1](https://github.com/israpps/wLaunchELF_ISR)] [[2](https://israpps.github.io/projects/wlaunchelf-isr)] [[3](https://www.psx-place.com/threads/wlaunchelf-4-43x_isr.32655/)]</sup>

Fork based on one of the wLE versions, modified by *El_isra*. It recognizes and allows editing of text files with the following extensions: **CFG**, **CNF**, **CHT**, and **INI**. It also preserves the modification timestamp of `mc?:/LAUNCHELF.CNF`, preventing it from interfering with the **Fortuna** and **OpenTuna** exploits. Depending on the edition (there are a plethora of variants for each release), it supports exFAT on [external storage](Internal%20Storage%20vs%20External%20Storage.md), **MX4SIO**, **MMCE**, and **dongles** on COH models.

### wLaunchELF ISR HDD 4.43x <sup>[[1](https://github.com/israpps/wLaunchELF_ISR_HDD)] [[2](https://www.psx-place.com/threads/wlaunchelf-isr_hdd.34075/)]</sup>

Fork based on one of the wLE versions, modified by *El_isra* and *Alexparrado*. Allows **copying files from USB to the Attributes area** of any **APA** partition.

### SmbLaunchELF / NETFS <sup>[[1](https://github.com/sahlberg/wLaunchELF/tree/smb2)] [[2](https://github.com/sahlberg/wLaunchELF)] [[3](https://www.psx-place.com/threads/smblaunchelf.32434/)]</sup>

Fork based on one of the wLE versions, modified by *Ronnie Sahlberg*. It adds support for **NFS**, **SMB** v2/v3 and simplifies the syntax of their configuration file relative to SMB v1.

### wLaunchELF R3Z 4.50 (and newer) <sup>[[1](https://github.com/saildot4k/wLaunchELF_R3Z)]</sup>

The first wLE fork (based on wLE ISR), which unifies all previously unique features and adds new ones (except for NFS and SMB). wLE R3Z supports all devices, mount points, partition tables, and file systems. It is the first wLE to support **both IDE channels**; `ata*:/` (an internal exFAT-formatted HDD); **APA-Jail** for both environments simultaneously; as well as the **UDPFS** network protocol. wLE R3Z dropped support for JPG, FTP, and Host.

<br />Berion<br />2026-08-01

<p align="right"><small>➜ Go back to <a href="index.md">main page</a></small></p>