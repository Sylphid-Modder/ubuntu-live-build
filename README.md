# ubuntu-live-build
The unofficial Live ISO builder for Ubuntu, for Ubuntu 22.04 LTS (jammy) or earlier. (**No support for Ubuntu 24.04 LTS (noble) now.**)

## Dependencies
- Ubuntu 22.04 or earlier
- debootstrap
- xorriso
- squashfs-tools
- curl
NOTE: This dependencies will be satisfied after executing "ubuntu-buildscript setup".

## Usage
- ``./ubuntu-buildscript setup [Name] [Version]``
Create a new environment to current folder, and install packages.

- ``./ubuntu-buildscript update [Path] [New Version]``
Update the version information of the environment specified with Path.

- ``./ubuntu-buildscript debootstrap [Path] [Suite] [URL]``
Setup the new Ubuntu minimal installation to the specified environment. You can choose suites (e.g. jammy, focal) and distribution's mirror's URL.
NOTE: This command will execute ``debootstrap`` with *minimal* option.

- ``./ubuntu-buildscript build [Path]``
Create the ISO of the specified environment.

## ToDo
- [ ] Separate commands to individual modules
- [ ] Change the folder structure of ISO
- [ ] Create a package for Ubuntu