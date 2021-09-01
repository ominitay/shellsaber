# ShellSaber

ShellSaber is a mod manager written in POSIX-compliant shell script to support
Beat Saber modding on Linux.

## Why?

Linux has no other native mod managers besides
[QBeat and Beataroni](https://github.com/geefr/beatsaber-linux-goodies)
(written and maintained by [geefr](https://github.com/geefr)). While these are
great tools in their own right, QBeat (which is now discontinued) cannot keep
track of currently installed mods, and Beataroni is GUI-only and uses dotnet. 
ShellSaber takes a different approach. By keeping track of dependencies, 
ShellSaber is able to remove orphaned dependencies quickly and easily. The use
of symlinks means that no files have to be moved, and that all mod files remain
separate from the Beat Saber installation.

## Installation

### Arch

```sh
git clone https://github.com/ominitay/shellsaber
cd shellsaber
makepkg -si # Generate and install the package
```

### Other Distros (local installation)

Download `installshaber` from the latest release, run `chmod +x installshaber`,
then execute it. Contributions for packages for unsupported distros would be much
appreciated!

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
