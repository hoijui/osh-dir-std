<!--
SPDX-FileCopyrightText: 2022 J.C. Mariscal <jc0x0b@gmail.com>
SPDX-FileCopyrightText: 2022 Robin Vobruba <hoijui.quaero@gmail.com>
SPDX-License-Identifier: CC0-1.0
-->

# OSH project directory structure standards

[![REUSE status](
    https://api.reuse.software/badge/gitlab.fabcity.hamburg/software/template-osh-repo-structure-minimal)](
    https://api.reuse.software/info/gitlab.fabcity.hamburg/software/template-osh-repo-structure-minimal)

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
use the reuse tool (`reuse spdx`) for more details.

