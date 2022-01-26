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
* including sub-parts as git sub-modules in multiple projects
* later extracting sub-parts as separate git repos,
  including all their history
* keeping repositories smaller,
  if a majority of the parts are git sub-modules
* use finer-grained access control,
  to grant access to only parts of the whole project
* swapping one implementation for an other
* keeping non-module, but binary-heavy dirs (e.g. images)
  also in a git sub-module,
  which allows to clean up history on them,
  from time to time\
  -> smaller and faster clones

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

* use singular forms;
  e.g. `asset`, not `assets`
* use common short forms, if they exist;
  e.g. `img` not `image`
* for directories, use rather generic names,
  instead of specific ones:
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
(created from the above with `lst2fs`):

```
.
├── bin
│   ├── build
│   ├── ci
│   ├── release
│   └── test
├── build
│   ├── doc
│   │   ├── assembly
│   │   ├── man
│   │   └── usr
│   ├── export
│   └── site
├── design
│   ├── el
│   │   ├── main.kicad_pcb
│   │   ├── main.pro
│   │   ├── main.sch
│   │   ├── plate.kicad_pcb
│   │   ├── plate.pro
│   │   └── plate.sch
│   └── mech
│       ├── case-alternative.fcstd
│       └── case.fcstd
├── doc
│   ├── assembly
│   │   ├── chap-1
│   │   │   ├── sec-1.md
│   │   │   ├── sec-2.md
│   │   │   └── sec-3.md
│   │   └── main.md
│   ├── man
│   │   ├── chap-1
│   │   │   ├── sec-1.md
│   │   │   ├── sec-2.md
│   │   │   └── sec-3.md
│   │   └── main.md
│   ├── recycling
│   │   ├── chap-1
│   │   │   ├── sec-1.md
│   │   │   ├── sec-2.md
│   │   │   └── sec-3.md
│   │   └── main.md
│   └── usr
│       ├── chap-1
│       │   ├── sec-1.md
│       │   ├── sec-2.md
│       │   └── sec-3.md
│       └── main.md
├── mod
│   ├── module-a
│   └── module-b
├── res
│   ├── asset
│   │   └── media
│   │       └── img
│   │           ├── animation-1.gif
│   │           ├── drawing-1.png
│   │           └── screenshot-1.jpg
│   ├── media
│   │   └── img
│   │       └── diagram-1.svg
│   ├── var
│   │   └── datasheet-x.pdf
│   └── some-config.xml
├── src
├── test
├── assembly.recipe.ttl
├── bom.csv
├── LICENSE.txt
├── manu.vf_recipe.ttl
├── README.md
└── recycle.recipe.ttl
```
