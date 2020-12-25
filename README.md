# ShellSaber

ShellSaber is a mod manager written in POSIX-compliant shell script to support
Beat Saber modding on Linux.

***WARNING: This script is very much a work-in-progress. Error-catching is very
sparse, and bugs will be significant and common. Please use geefr's [QBeat or
Beataroni](https://github.com/geefr/beatsaber-linux-goodies) in the meantime.***

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

Don't use this yet (unless you want to test and/or contribute). I hope to
have a prerelease which is usable by the year's end.

## Usage

*TODO*

## Credit

**[geefr](https://github.com/geefr)** — I was inspired by his *QBeat* mod
manager, and wanted to take the idea further. He has helped me greatly with
development of *ShellSaber*.
