<!--
SPDX-FileCopyrightText: 2022 J.C. Mariscal <jc0x0b@gmail.com>
SPDX-FileCopyrightText: 2022 Robin Vobruba <hoijui.quaero@gmail.com>
SPDX-License-Identifier: GFDL-1.3-or-later
-->

# Prusaish - OSH project directory structure standards

This repository exemplifies a minimal template for the structure of Free/Open
source hardware projects.

It promotes a practical, minimal style,
with emphasis on sources,
organisation for CAD files and documentation,
and git sub-modules for firmware and scripts.
Most directories are named after the file-type
(i.e. suffix or software) they contain.

## Definition

This standards machine-readable definition,
can be found in various formats here:

- [definition.csv](definition.csv)
  ([format](../../definition_format.md))
  \- source, machine-readable, contains all the data
  \- **use this for editing**
- [file-listing](
  https://software.development.fabcity.hamburg/template-osh-repo-structure-minimal/mod/unixish/listing.txt)
  \- like the output of `find` in a sample repo
  \- generated
- [tree](
  https://software.development.fabcity.hamburg/template-osh-repo-structure-minimal/mod/unixish/tree.html)
  \- like the output of `tree` in a sample repo
  \- generated, **recommended** for inspection

## Guiding principles & Inspirations

This standard is roughly derived from the [Prusa repo](
https://github.com/prusa3d/Original-Prusa-i3)
and [a few repos](https://github.com/fab-machines)
[by Daniele Ingrassia](https://github.com/satshakit)

Some of the inspirations:

- <https://gitlab.com/openflexure/openflexure-microscope>
- <https://github.com/prusa3d/Original-Prusa-MINI>
- <https://github.com/fab-machines/LaserDuo>
- <https://github.com/Creality3DPrinting/Ender-3>
- <https://github.com/fab-machines/Fabulaser-Mini>
- <https://github.com/NedalLive/Hypercube-NGen>
