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
├── cad_2d
│   ├── dxf
│   │   └── subassembly_01_name_lasercut.dxf
│   └── svg
│       └── subassembly_01_name_vinyl_cut.stp
├── cad_3d
│   ├── fcstd
│   ├── overall_machine.FCStd
│   ├── step
│   │   ├── subassembly_01_name_3d_printed.stp
│   │   ├── subassembly_02_name_laser_cut.stp
│   │   └── subassembly_03_name_machined.stp
│   └── stl
│       └── optional.stl
├── cad_sch
│   ├── lib
│   │   ├── libname2.lib
│   │   └── libname.lib
│   ├── subassembly_pcbname2_otherdetails
│   │   ├── pcbname2.brd
│   │   └── pcbname2.sch
│   └── subassembly_pcbname_otherdetails
│       ├── pcbname.brd
│       └── pcbname.sch
├── datasheets
│   └── datasheetname.pdf
├── docs
│   ├── electronics
│   └── mechanical
├── drawings
│   ├── overall_machine_drawing.pdf
│   └── subassembly_01_drawing.pdf
├── examples
│   ├── example_01.foo
│   ├── example_01.md
│   └── example_01_settings.foo
├── firmware_git_submodule
├── img
├── LICENSE
├── manual
│   ├── manual_assembly.pdf
│   └── manual_operation.pdf
├── README.md
├── scripts
│   ├── script01_git_submodule
│   └── script02_git_submodule
├── software1_settings
│   └── software1.conf
└── software2_settings
    └── software2.conf
```

## BOM

The BOM of the OSH, in pdf and editable format.

## cad_2d

2D cad files organised by format and subassembly.
## cad_3d

3D cad files organised by format and subassembly.

## cad_sch

Schematics of the machine design organised by PCB.

## datasheets

Datasheets of external parts and components of the OSH.

## docs

## drawings

Technical drawings of the machine and machining tolerances of problem parts

## examples

Examples of usage of the machine (i.e. STL file and print settings)

## firmware (git submodule)

Firmware of the project imported as a submodule, residing outside the repository

## img

Images of the

## manual

Assembly manual of the machine

## scripts

Scripts, each in its separate git submodule.

## <software_name>_settings

Software settings for the project or machine.

## License and Copyright

FDL1.3 or newer , (c) J.C. Mariscal-Melgar, Pieter Hijma

## Contributors
