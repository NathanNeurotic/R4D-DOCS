# Current source status

This file tracks gaps in the documentation bundle currently imported into R4D DOCS. It is not a substitute for the guides themselves.

## Supplied documentation

The current repository contains all Markdown guides present in the supplied `tutorials.zip`, including the work-in-progress disc guide. Internal links that clearly referred to an existing guide under a slightly different filename were normalized for the site.

Three already-referenced guides were not present in the supplied archive, so placeholder pages exist until their real Markdown is available:

- `Neutrino GUI Flavors.md`
- `How to Format Memory Cards.md`
- `How to Install Exploit.md`

## Supplied binary assets

The source archive contains **31 image files** under `images/`. The current GitHub connector can write repository text/Git objects but cannot directly consume binary files from a conversation upload, so those supplied image binaries still need to be added to the repository's `images/` directory through a binary-capable Git/GitHub upload path. The Markdown filenames have been left intact so adding that directory later requires no documentation rewrite.

## Referenced images not present in the supplied archive

The following image filenames are referenced by the Markdown but were not included in `tutorials.zip`:

- `images/apollo_main.png`
- `images/apollo_sav_bup_1.png`
- `images/apollo_sav_bup_2.png`
- `images/apollo_sav_restore.png`
- `images/opl_ople.png`
- `images/opl_ps2l.png`
- `images/opl_riptopl.png`
- `images/opl_wopl_1.png`
- `images/opl_wopl_2.png`
- `images/opl_wopl_3.png`
- `images/r3cfg_edit.png`
- `images/r3cfg_list.png`
- `images/r3cfg_main.png`
- `images/r4d_fmcb.png`
- `images/r4d_osdm.png`
- `images/wle_msas_copy.png`
- `images/wle_msas_psupaste.png`
- `images/wle_msas_view.png`
- `images/wle_sav_copy.png`
- `images/wle_sav_list_1.png`
- `images/wle_sav_list_2.png`
- `images/wle_sav_makepsu.png`

The archive also contains `images/defraggler_1.png`, which is not referenced by the current Markdown.
