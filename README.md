# ShellSaber

ShellSaber is a mod manager written in POSIX-compliant shell script to support
Beat Saber modding on Linux.

## Why?

Linux has no mod managers besides
[QBeat and Beataroni](https://github.com/geefr/beatsaber-linux-goodies)
(written and maintained by [geefr](https://github.com/geefr)). While these are
great tools in their own right, QBeat (which is now discontinued) cannot keep
track of currently installed mods, and Beataroni is GUI-only (and, like this
script, is in early stages of development). ShellSaber takes a different
approach. By keeping track of dependencies, ShellSaber is able to remove
orphaned dependencies quickly and easily. Symlinking means that no files have to
be moved, and all mod files stay in one place.

## Installation

Download `installshaber` from the latest release, run `chmod +x installshaber`,
then execute it. Distro-specific packages are in the works, and contributions for
such would be much appreciated!

## Setup

You will usually need to customise a config file for ShellSaber to work. To do
this, you should copy the default config file (either
`~/.local/share/shaber/default/config` or `/etc/shaber/config`) to
`~/.config/shaber/config`. You can then change `bs_dir` to where your Beat Saber
installation is, and `bs_version` to the latest version supported by the api
([BeatMods](https://beatmods.com)). The `api_url` variables should be left as
their default.

## Usage

###### Output help page

`shaber -h` or `shaber -h [MODE]`

###### Download mods

`shaber mod download [MODS...]`

###### Enable mods

`shaber mod enable [MODS...]`

###### Disable mods

`shaber mod disable [MODS...]`

###### Delete mods

`shaber mod remove [MODS...]`

###### Update mods

`shaber mod update [MODS...]`

###### Patch with BSIPA

`shaber ipa download`\
`shaber ipa patch`

## Uninstallation

To uninstall ShellSaber, all mods need to be disabled or removed beforehand. To
do this, run the command `shaber mod remove all`. Afterwards, run the command
`shaber-uninstall` in your shell. Your custom config file will be left where you 
made it.

## Credit

**[geefr](https://github.com/geefr)** — I was inspired by his *QBeat* mod
manager, and wanted to take the idea further. He has helped me greatly with
development of *ShellSaber*.
