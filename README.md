<!--
SPDX-FileCopyrightText: 2022 J.C. Mariscal <jc0x0b@gmail.com>
SPDX-FileCopyrightText: 2022-2023 Robin Vobruba <hoijui.quaero@gmail.com>
SPDX-License-Identifier: CC0-1.0
-->

# OSH project directory structure standards

[![License: GFDL-1.3-or-later](
    https://img.shields.io/badge/License-GFDL--1.3--or--later-blue.svg)](
    https://spdx.org/licenses/GFDL-1.3-or-later.html)
[![REUSE status](
    https://api.reuse.software/badge/gitlab.fabcity.hamburg/software/template-osh-repo-structure-minimal)](
    https://api.reuse.software/info/gitlab.fabcity.hamburg/software/template-osh-repo-structure-minimal)

[![In cooperation with FabCity Hamburg](
    https://raw.githubusercontent.com/osegermany/tiny-files/master/res/media/img/badge-fchh.svg)](
    https://fabcity.hamburg)
[![In cooperation with Open Source Ecology Germany](
    https://raw.githubusercontent.com/osegermany/tiny-files/master/res/media/img/badge-oseg.svg)](
    https://opensourceecology.de)

## Motivation

Why do we need directory standards?

1. to be able to extract meta-data:
    1. easy indexing (and thus finding) of projects
    2. easy comparing of projects
    3. allows to write software tools that deal with project repos
2. find your way around quickly and easily in different projects

## Standards documented in this repo

- [Prusaish](mod/prusaish/README.md):
  Promotes a practical, minimal style,
  with emphasis on sources,
  and git sub-modules for firmware and scripts.
  Most directories are named after the file-type
  (i.e. suffix or software) they contain.

- [Unixish](mod/unixish/README.md) (**favored**):
  Each sub-part (aka module) is in a sub-directory of its own,
  and internally uses the same structure like in the project root,
  recursively.
  Most directories are named after the abstract/generic function
  of their content.

## Other structure templates

- <https://www.sciencedirect.com/journal/hardwarex>
- <https://osf.io/wgk7q/>

## License

The most relevant content of this repo
is licensed under the `GFDL-1.3-or-later`.
Use the REUSE tool (`reuse spdx`) for more details.

## Funding

This project was funded by the European Regional Development Fund (ERDF)
in the context of the [INTERFACER Project](https://www.interfacerproject.eu/),
from January 2022 (project start)
until March 2023.

![Logo of the EU ERDF program](
    https://cloud.fabcity.hamburg/s/TopenKEHkWJ8j5P/download/logo-eu-erdf.png)
