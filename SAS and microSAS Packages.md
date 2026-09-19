---
layout: default
title: "SAS and microSAS Packages"
---

# SAS and microSAS Packages

**SAS** and **mSAS** packages are bundled applications that include metadata and configuration files, allowing users to easily add and remove applications themselves. Simply select a PSU file in the file manager, copy it, and use the `psuPaste` (uLE and most wLE versions) / `Extract PSU` (wLE R3Z) option to paste it onto a **PlayStation 2 Memory Card** (for more details, see this [guide](How%20to%20Install%20Applications.html)).

## Differences Between SAS and mSAS

Although the two package families are more or less compatible with each other, the two projects have slightly different goals and therefore differ in some respects. Below is a list to help you determine which "faction" better suits your needs.

### Application ID

The application identifier (**APP ID**) consists of a category tag, a unique folder name, and, optionally, the application version if it is important to preserve it. In most cases, both projects use the same APP IDs, but there are a few cases where they differ (mainly in category assignment, such as `EMU_X2P` (SAS) vs. `APP_X2P` (mSAS)).

### Timestamp

In **SAS**, all timestamps are generated at once when the packages are created. This gives each package a unique timestamp and allows them to be sorted very well alphabetically in the save menu.

In **mSAS**, all applications within a given category use the same timestamp. This makes sorting work well at the category level, but much worse when it comes to alphabetical ordering. However, the advantage of this approach is that individual packages are easy to create or edit. The author does not need to use a special script for this or worry about checksums that could change for the same application.

| Timestamps (mSAS)   | Tag | Purpose |
|-|-|-|
| 2090-01-01 00:00:01 | APP | Game Loaders |
| 2089-01-01 00:00:01 | APP | Utilities |
| 2088-01-01 00:00:01 | APP | Multimedia |
| 2087-01-01 00:00:01 | PS1 | PS1 Emulation |
| 2086-01-01 00:00:01 | EMU | Retro Emulation |
| 2085-01-01 00:00:01 | GME | Homebrew Games |
| 2083-01-01 00:00:01 | DBG | Debugging & Development Tools |
| 2082-01-01 00:00:01 | DST | Diagnostic & Service Tools |
| 2081-01-01 00:00:01 | RTE | Runtime Environments |
| 2080-01-01 00:00:01 | SYS | System Apps |

<small>The 2084 timestamp is not used.</small>

### Metadata

**SAS** packages contain `INSTALL.PBT` files (for Crystal Chip modchips) and a `title.cfg` file containing all parameters, similar to `GameID.cfg` for games and OPL Manager.

**mSAS** does not contain PBT files (they take up very little space but are only used by relatively rare chips), and its `title.cfg` is limited to the minimum required parameters, since most of them are completely unnecessary for homebrew applications.

In the near future, both projects will probably be extended to include `app.cfg` (a newer version of `title.cfg`).

### Icons

The 3D icons in **SAS** are unique, with each one having its own shape, etc. In **mSAS**, all icons take the form of a cube styled to look like a cardboard box, each featuring its own logo. The naming also differs.

| Purpose  | SAS      | mSAS              |
|-|-|-|
| Listing  | list.icn | icon_listview.icn |
| Copying  | copy.icn | icon_copy.icn     |
| Deleting | del.icn  | icon_delete.icn   |

In the near future, both projects will probably be extended to include a 2D icon file: `app.png` (cover art).

## Where to Find Packages?

All packages can be found in the **Recovery for Dummies** (R4D) project, in the following directories:
```
/APPS/Save Application System (SAS)/
/APPS/Save Application System (microSAS)/<category>/

```
Officially, **mSAS** packages cannot be found online anywhere outside R4D. **SAS** packages, on the other hand, can be found in the GitHub Releases of some projects. They are also available in:

- the [ps2wiki](https://ps2wiki.github.io/sas-apps-archive/) repository
- the [ps2homebrewstore](https://ps2homebrewstore.com/) repository

## File Formats

For now, **PSU** is used. This format was originally designed for game saves, but since every version of uLE and wLE supports it, it was chosen when the standard was established. Unfortunately, it has one major drawback: it does not support subfolders. To address this, **TAR** will probably be used in the future (with a dedicated PAX header to preserve all timestamps).

## Destination

Where should the packages be extracted?

| Path                     |  |
|-|-|
| mc?:/                    | PS2 Memory Card |
| mass:/APPS/              | USB (old nomenclature) |
| usb:/APPS/               | USB (new nomenclature) |
| hdd0:/__common/APPS/     | Internal Disk, recommended location |
| hdd0:/__common/OPL/APPS/ | Internal Disk, OPL resources (new path) |
| hdd0:/+OPL/APPS/         | Internal Disk, OPL resources (old path) |

<small>Keep in mind that only a small number of apps support the internal disk. Almost none support MMCE devices, so mmce0 is not included in the list.</small>

<br />Berion<br />2026-08-19

<p align="right"><small>➜ Go back to <a href="index.html">main page</a></small></p>
