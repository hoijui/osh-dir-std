<!--
SPDX-FileCopyrightText: 2022 Robin Vobruba <hoijui.quaero@gmail.com>
SPDX-License-Identifier: GFDL-1.3-or-later
-->

# Unixish - OSH project directory structure standards

In short: **Modular and generic**

The basic idea here,
is that each sub-part aka module is in a sub-directory of its own,
and internally uses the same structure like the main project.

## Definition

This standards machine-readable definition,
can be found in various formats here:

- [definition.csv](definition.csv)
  ([format](../../definition_format.md))
  \- source, machine-readable, contains all the data
  \- **use this for editing**
- [file-listing](
  https://osegermany.gitlab.io/osh-dir-std/mod/unixish/listing.txt)
  \- like the output of `find` in a sample repo
  \- generated
- [tree](
  https://osegermany.gitlab.io/osh-dir-std/mod/unixish/tree.html)
  \- like the output of `tree` in a sample repo
  \- generated, **recommended** for inspection

## Guiding principles & Inspirations

This standard is derived from the thinking outlined below,
inspired by the following, well proven and established standards
from the software world:

- [Unix/Linux/BSD directory structure](
  https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard)
- [Maven directory structure](
  https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html)

The main principle is ["Convention over configuration"](
https://en.wikipedia.org/wiki/Convention_over_configuration).

### Why modular

It makes lots of things easier:

- using sub-parts from within other projects
- including sub-parts as git sub-modules in multiple projects
- later extracting sub-parts as separate git repos,
  including all their history
- keeping repositories smaller,
  if a majority of the parts are git sub-modules
- use finer-grained access control,
  to grant access to only parts of the whole project
- swapping one implementation for an other
- keeping non-module, but binary-heavy dirs (e.g. images)
  also in a git sub-module,
  which allows to clean up history on them,
  from time to time\
  -> smaller and faster clones

### Why generic

It results in:

- overall less directories
- less standard names one has to remember
- projects looking more similar to each other,
  which may contribute to make designers feel "at home"
  when coming to an other project
- leads to less "structure-bloat"
- makes tooling easier and more robust

### Guiding rules

- use singular forms;
  e.g. `asset`, not `assets`
- use common short forms, if they exist;
  e.g. `img` not `image`
- for directories, use rather generic names,
  instead of specific ones:
  e.g. `img`, not `drawing` or `photo`

### Common directory names

These are generic directory names,
commonly found in soft- and hardware projects,
which we might want to use (in alphabetical order):

```csv
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

```csv
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

