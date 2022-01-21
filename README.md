# Template

This repository exemplifies a minimal template for the structure of Free/Open
source hardware projects.

When a user or maker lands on your page they should see:

A `README.<md|org|rst|...>` file and a `LICENSE` file.

Sample repository:

```sh
├── bom
│   ├── bom.md
│   └── bom.pdf
├── cad_mechanics
|   └──cad_2d
│   │   ├── dxf
│   │   │   └── subassembly_01_name_lasercut.dxf
│   │   └── svg
│   │        └── subassembly_01_name_vinyl_cut.stp
│   ├──cad_3d
│       ├── fcstd
│       ├── overall_machine.FCStd
│       ├── step
│       │   ├── subassembly_01_name_3d_printed.stp
│       │   ├── subassembly_02_name_laser_cut.stp
│       │   └── subassembly_03_name_machined.stp
│       └── stl
│           └── optional.stl
├── cad_electronics
│   ├── lib
│   │   ├── libname2.lib
│   │   └── libname.lib
│   ├── subassembly_pcbname2_otherdetails
│   │   ├── pcbname2.brd
│   │   └── pcbname2.sch
│   └── subassembly_pcbname_otherdetails
│       ├── pcbname.brd
│       └── pcbname.sch
├── datasheets_external_parts
|   ├──dataheets_mechanics
│   |   └── datasheetname.pdf
|   └──dataheets_electronics
│       └── datasheetname.pdf
├── docs
|   ├── drawings
|   |   ├── mechanics
|   |   |   ├── overall_machine_drawing.pdf
│   |   |   └── subassembly_01_drawing.pdf
│   |   └── electronics
|   |       ├── overall_machine_drawing.pdf
│   |       └── subassembly_01_drawing.pdf
│   └── manual
│       ├── manual_assembly.md/pdf
│       └── manual_operation.md/pdf
├── example
│   ├── example_01.foo
│   ├── example_01.md
│   └── example_01_settings.foo
├── firmware_git_submodule
├── img
├── LICENSE
├── README.md
├── scripts
│   ├── script01_git_submodule
│   └── script02_git_submodule
└── software/firmware_configuration
    ├── software1_settings
    │   └── software1.conf
    └── software2_settings
        └── software2.conf
```

## BOM

The BOM of the OSH, in pdf and editable format.

## cad_mechanics
### cad_2d

2D cad files organised by format and subassembly.
### cad_3d

3D cad files organised by format and subassembly.

## cad_electronics

Schematics of the machine design organised by PCB.

## datasheets

Datasheets of external parts and components of the OSH.
### datasheets_mechanics
### datasheets_electronics

## docs

### drawings

Technical drawings of the machine and machining tolerances of problem parts
### manual

Assembly manual of the machine

## examples

Examples of usage of the machine (i.e. STL file and print settings)

// is here meant the usage of the needed machines for manufacturing the osh parts? I would then call it cam_files
// or is it the config file for operating the finished assembled osh hardware, e.g. basic config file for 3D printer (dimension settings, control settings, ...), then I would call it config file. Or is this meant to be in the software_name settings?
// or is it a operating example/ application example for the osh/ machine, e.g. how the machine can be used

## firmware (git submodule)

Firmware of the project imported as a submodule, residing outside the repository

## img

Images of the


## scripts

Scripts, each in its separate git submodule.

## <software_name>_settings

Software settings for the project or machine.

## License and Copyright

FDL1.3 or newer , (c) J.C. Mariscal-Melgar, Pieter Hijma

## Contributors
