---
layout: default
title: "How to Install Applications"
---

# How to Install Applications

The PlayStation 2 does not have a built-in operating system. As a result, there has never been an official standard for either application naming or their installation locations on the PS2 Memory Card. Developers of homebrew applications -- unofficial software created by the community -- never followed a common convention because Sony never defined one.

In practice, this means that, apart from Sony software, any application can be placed in any directory and launched from virtually any location. The same applies to configuration files. Over the years, the most commonly used directories have included `mc0:/APPS/` (late Free McBoot era), `mc0:/BOOT/` (primarily used as an exit target for applications and as the boot location for the DEV1 feature of compatible modchips), `mc0:/SYS-CONF/` (various settings), as well as completely custom directories chosen by individual application authors (for example, `mc0:/SMS/`).

The first attempt at standardization came in the form of **UMCS** and **SAS**, originally created by **TnA** and later further developed by our team (including my own contribution, microSAS). Without going into the technical details, applications distributed in the SAS and microSAS formats are packaged as PSU files. Although the PSU format was originally designed for keeping PlayStation 2 save data, it also works remarkably well as an archive format for applications. When extracted, a PSU package produces a directory containing the executable, icons, metadata, and any additional files required by the application. If you would like to learn more about the differences between SAS and microSAS, see the dedicated guide: [SAS and microSAS Packages](SAS%20and%20microSAS%20Packages.html).

## Install mSAS/SAS Applications

1. Insert the R4D USB stick into your console.
2. Launch **double-unofficial LaunchELF R3Z** (abbreviated as **wLE R3Z**) using any method available to you. Alternatively, you can use any other version of unofficial LaunchELF, as all of them support extracting PSU packages.
3. Navigate to the appropriate category in `usb:/APPS/Save Application System (microSAS)/packages/` (in other versions of wLE, the mount point is named `mass:/` instead of `usb:/`). Copy one or more PSU packages by pressing **R1** on the controller and selecting **Copy** from the context menu displayed on the right.

<p align="center"><img src="./images/wle_msas_copy.png" alt="mSAS Copy"/></p>

4. After copying the package(s), navigate to `mc0:/` (the PS2 Memory Card in Slot **1**) or `mc1:/` (Slot **2**), enter it, then press **R1** and select **Extract PSU** (**psuPaste** in most versions of wLE -- <span style="color: #D32F2F;">not **Paste**</span>). If you are using my preconfigured Free McBoot installation, all extracted microSAS applications will automatically appear in the main menu.

<p align="center"><img src="./images/wle_msas_psupaste.png" alt="mSAS Extract"/></p>

5. After extraction, new folders should appear, such as `APP_OPL`. The folder names depend on the application you extracted and follow the `<TAG>_<NAME>` naming convention.

<p align="center"><img src="./images/wle_msas_view.png" alt="mSAS View"/></p>

## Install Non-mSAS/SAS Applications

If you have an application distributed as a single **ELF** file, you can place it virtually anywhere, for example on a PS2 Memory Card. However, keep in mind that **OSDSYS** (the PS2 Browser) treats standalone files located in the root of the PS2 Memory Card, as well as files stored in directories that do not contain `icon.sys` and/or `icon.icn`, as **Corrupted Data**. For this reason, I recommend either not copying such applications to the PS2 Memory Card at all or placing them in the `BOOT` directory, which most likely already contains the required icon metadata.

If you already have an application installed somewhere, for example on the internal hard drive, and you want to update it, provided it is not distributed as an mSAS or SAS package, simply replace the existing executable with the new one. For example, many users have **Open PS2 Loader** (OPL) installed on the `hdd0:/+OPL/` partition as `OPNPS2LD.ELF`. In that case, simply copy a newer file with the same name from your USB drive to the `+OPL` directory and overwrite the existing one.

The procedure is similar to the previous section: **Copy** → **Paste** (<span style="color: #D32F2F;">do not confuse this with **psuPaste** or **Extract PSU**</span>).

## Add Applications to the Main Menu

Applications that are not distributed in the mSAS or SAS format do not automatically appear in the **Free McBoot** menu (or your current configuration may not include them). Likewise, no applications appear in the **OSDMenu** menu by default. If you want them to be accessible from the main menu, you can easily add them using **R3Configurator**.

1. Launch the application and select the loader type and the device from which it should attempt to load the configuration. Once selected, **R3Configurator** automatically loads the corresponding configuration file if it exists. For example, if you choose **Free McBoot** and the first PS2 Memory Card, it loads `mc0:/SYS-CONF/FREEMCB.CNF`. Likewise, if you choose **OSDMenu**, it loads `OSDMENU.CNF` etc.

<p align="center"><img src="./images/r3cfg_main.png" alt="R3Configurator: Main Menu"/></p>

2. Select **Edit menu entries**. A list of all menu entries stored in the configuration file will be displayed. Highlight the position where you want to insert a new entry, press the **Square** button, and select **Insert**.

<p align="center"><img src="./images/r3cfg_list.png" alt="R3Configurator: List"/></p>

3. Set the entry name using **Edit name**. Then configure one or more paths below it (shown as **(not set)**) by selecting the desired ELF executable. Simply browse to the target device and press **Cross** on the executable.

<p align="center"><img src="./images/r3cfg_edit.png" alt="R3Configurator: Edit Menu"/></p>

4. Press the **Start** button to **Save** the configuration, then exit the application. Your newly added application should now appear in the main menu.

## Recommended Applications

Depending on your installation method and configuration, you may be missing some essential applications. For example, **KELFBinder-mSAS** and **Free McBoot & Free HDBoot Installer ISR-RIP** install only the exploit, bootloader, OSDSYS patchers, and file manager, leaving the choice of additional software entirely up to the user. This keeps the installation as small as possible and avoids unnecessary bloatware. Alternatively, you may already own a PS2 Memory Card with **Free McBoot** (FMCB) and simply want to update its outdated applications without changing anything else.

In such cases, I recommend adding the following applications to your PS2 Memory Card or internal hard drive:

| Application Name                  | Purpose |
|-|-|
| ESR R9b & R10f                    | Support for fake DVD-Video game discs (CLI). |
| ESR Launcher                      | Same as above, but with all R9c and R10f versions encapsulated in a GUI. |
| Double Unofficial Open PS2 Loader | Commonly known as wOPL, a superior OPL fork (PS2 game loader). |
| RiptOPL                           | Another Open PS2 Loader fork (PS2 game loader). |
| Neutrino                          | Lightweight PS2 game loader (CLI). |
| Modulo                            | GUI frontend for Neutrino. |
| DKWDRV                            | Better than Sony PS1DRV; also a PS1 emulator on Deckard models (SCPH-75K and newer). |
| POPSLoader                        | GUI for POPStarter (wrapper for the PS1 emulator called POPS). |
| Apollo Save Tool                  | Save Data management utility. |
| double-unnoficial LaunchELF R3Z   | wLE R3Z, a superior wLE ISR fork. |

<br />Berion<br />2026-07-31

<p align="right"><small>➜ Go back to <a href="index.html">main page</a></small></p>
