<!--
SPDX-FileCopyrightText: 2025 Nils Weiher <nils.weiher@ose-germany.de>
SPDX-License-Identifier: GFDL-1.3-or-later
-->

# Modularish - OSH project directory structure standards

In short: **Modular and accessible**

The prunix directory standard provides a structure that is flexible but not completely generic, in order to provide better accessibility while supporting machine readability.

The standard was merged from the directory standards [unixish](https://gitlab.com/OSEGermany/osh-dir-std/-/blob/main/mod/unixish/README.md) and [prusaish](https://gitlab.com/OSEGermany/osh-dir-std/-/blob/main/mod/prusaish/README.md) and adjusted to the requirements of Open Source projects that integrate hardware, software, documentation and design elements.

## Definition

This standards machine-readable definition, can be found in various formats here:

- [definition.csv](definition.csv)
  ([format](../../definition_format.md))
  \- source, machine-readable, contains all the data
  \- **use this for editing**
- [file-listing]()
  \- like the output of `find` in a sample repo
  \- generated
- [tree]()
  \- like the output of `tree` in a sample repo
  \- generated, **recommended** for inspection

## Guiding principles & Inspirations
To apply the standard preferably use the standard folder names below. These should represent the typical structure required for hardware, software, documentation and design. If additional folders are required follow the rules below the standard folder names.

### Standard folder names

Legend
**Folder name**: description [typical file format examples]

- **docs**: documentation & supplementary material
    - **guides**: documentation content
    - **media**: documentation related media files, e.g. technical drawings
    - **appendix**: supplementary material, e.g. calculations
- **mechanics**: Mechanics CAD source files
    - **2d**: 2D CAD files
        - **layout**: subassembly files [.dxf, .svg]
        - **lib**: external library files
    - **3d**: 3D CAD files
        - **project**: contains the subassembly project files
        - **layout**: subassembly files [.fcstd]
        - **export** subassembly export files [.step, .stl]
        - **lib**: external library files
- **electronics**: Electronic CAD source files
    - **project**: contains the project files
    - **layout**: contains the pcb layout files
    - **schematics**: contains the schematic files
    - **kicad** contains project, layout and schematic files for kicad (need to be in one place)
    - **export** export files for pcb [.grb]
    - **lib**: external library files
- **src**: software source code, like scripts, etc.
- **conf**: configuration files
- **submodules**: external repositories included in the project
- **assets**: binary files
- **media**: embedded media files
- *BOM.csv*: Central bill of materials (BOM)
- *LICENSE.md*: central license file
- *README.md*: central readme file

LICENSE.md and README.md files are allowed on all levels. A license file in a specific subsection replaces the central licence for that same subsection.  

The folder structure can also be reproduced in subfolders, if required. Specifically lib, media, export and src can be replicated to create consistent structures. Binary files [images, pdf, ...] need to be placed in seperate folders due to machine readability.


### Additional folders
For additional folders prefer names from the unixish directory standard: https://gitlab.com/OSEGermany/osh-dir-std/-/blob/main/mod/unixish/README.md
- use as much hierarchy as needed and as little as possible
- if subfolders are required apply the same logic as above, preferrably use standard names (e.g. src/conf)
- if individual folders are required use the following conventions:
    - use common abbreviations (e.g. cfg: configuration, img: image)
    - otherwise use clear prescriptive form (e.g. design)
    - prefer singular form