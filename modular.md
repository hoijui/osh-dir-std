<!--
SPDX-FileCopyrightText: 2022 Robin Vobruba <hoijui.quaero@gmail.com>
SPDX-License-Identifier: CC0-1.0
-->

# Modular and generic

The basic idea here,
is that each sub-part aka module is in a sub-directory of its own,
and internally uses the same structure like the main project.

## Why modular

It makes lots of things easier:

* using sub-parts from within other projects
* including sub-parts as git sub-modules
* later extracting sub-parts as separate git repos,
  including all their history
* keeping repositories smaller (if all/most sub-parts are git sub-modules)
* allowing for finer-grained access control to only parts of the whole project
* swapping one implementation for an other

## Why generic

It results in:

* overall less directories
* less standard names one has to remember
* projects looking more similar to each other,
  which may contribute to make designers feel "at home"
  when coming to an other project
* leads to less "structure-bloat"
* makes tooling easier and more robust

## Guiding rules

* if there is only possibly one (file) of something within a project/module,
  it should be in the root, for examples: `bom.csv`, `README.md`, `LICENSE.txt`
* use singular forms;
  e.g. `asset`, not `assets`
* use common short forms, if they exist;
  e.g. `img` not `image`
* use rather generic names, instead of specific ones, for directories;
  e.g. `img`, not `drawing` or `photo`

## Common directory names

These are generic directory names,
commonly found in soft- and hardware projects,
which we might want to use (in alphabetical order):

```
assembly(-guide)
asset(s)
bin vs script(s)
build vs target vs site vs export
cfg (vs config(s))
ci
design(s)
doc(s) (vs document(s) vs documentation)
el(ectro(nics))
img (vs image(s))
man(ual)
mech(anics)
media
mod vs module
part(s)
res(ource(s))
src (vs source(s))
test
usr vs user(-guide)
var vs misc
```

and the same, grouped into clusters of potential conflict or overlap:

```
bin
ci

asset
img
media
res
var

design
el
mech

build
target
site
export

cfg

doc
man
usr
assembly

part
mod

src
test
```

## Painting the structure

```
LICENSE.txt
README.md
bom.csv
assembly.recipe.ttl
manu.vf_recipe.ttl
recycle.recipe.ttl

bin/build
bin/test
bin/release
bin/ci

res/some-config.xml
res/asset/media/img/drawing-1.png
res/asset/media/img/animation-1.gif
res/asset/media/img/screenshot-1.jpg
res/media/img/diagram-1.svg
res/var/datasheet-x.pdf

design/el/main.pro
design/el/main.sch
design/el/main.kicad_pcb
design/el/plate.pro
design/el/plate.sch
design/el/plate.kicad_pcb
design/mech/case.fcstd
design/mech/case-alternative.fcstd

build/site/
build/doc/assembly/
build/doc/man/
build/doc/usr/
build/export/

doc/assembly/main.md
doc/assembly/chap-1/sec-1.md
doc/assembly/chap-1/sec-2.md
doc/assembly/chap-1/sec-3.md
doc/man/main.md
doc/man/chap-1/sec-1.md
doc/man/chap-1/sec-2.md
doc/man/chap-1/sec-3.md
doc/usr/main.md
doc/usr/chap-1/sec-1.md
doc/usr/chap-1/sec-2.md
doc/usr/chap-1/sec-3.md
doc/recycling/main.md
doc/recycling/chap-1/sec-1.md
doc/recycling/chap-1/sec-2.md
doc/recycling/chap-1/sec-3.md

mod/module-a/
mod/module-b/

src/
test/
```

the same in `tree` form
(created from the above with
`mkdir tmp; cd tmp; echo "..." | ../lst2fs`):

```
.
|____assembly.recipe.ttl
|____README.md
|____LICENSE.txt
|____bom.csv
|____test
|____doc
| |____man
| | |____main.md
| | |____chap-1
| | | |____sec-2.md
| | | |____sec-1.md
| | | |____sec-3.md
| |____recycling
| | |____main.md
| | |____chap-1
| | | |____sec-2.md
| | | |____sec-1.md
| | | |____sec-3.md
| |____usr
| | |____main.md
| | |____chap-1
| | | |____sec-2.md
| | | |____sec-1.md
| | | |____sec-3.md
| |____assembly
| | |____main.md
| | |____chap-1
| | | |____sec-2.md
| | | |____sec-1.md
| | | |____sec-3.md
|____recycle.recipe.ttl
|____res
| |____media
| | |____img
| | | |____diagram-1.svg
| |____some-config.xml
| |____var
| | |____datasheet-x.pdf
| |____asset
| | |____media
| | | |____img
| | | | |____animation-1.gif
| | | | |____drawing-1.png
| | | | |____screenshot-1.jpg
|____bin
| |____release
| |____ci
| |____test
| |____build
|____build
| |____export
| |____doc
| | |____man
| | |____usr
| | |____assembly
| |____site
|____manu.vf_recipe.ttl
|____design
| |____mech
| | |____case.fcstd
| | |____case-alternative.fcstd
| |____el
| | |____main.kicad_pcb
| | |____main.sch
| | |____plate.sch
| | |____plate.kicad_pcb
| | |____plate.pro
| | |____main.pro
|____src
|____mod
| |____module-b
| |____module-a
```