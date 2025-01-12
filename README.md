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
### Setup
- ``./ubuntu-buildscript setup [Name] [Version]``
Create a new environment to current folder, and install packages.

- ``./ubuntu-buildscript debootstrap [Path] [Suite] [URL]``
Setup the new Ubuntu minimal installation to the specified environment. You can choose suites (e.g. jammy, focal) and distribution's mirror's URL.
NOTE: This command will execute ``debootstrap`` with *minimal* option.

### Maintenance
- ``./ubuntu-buildscript update [Path] [New Version]``
Update the version information of the environment specified with Path.

- ``./ubuntu-buildscript change-name [Path] [New Name]``
Update the name of specified environment. This command will change the name of distribution too.

- ``./ubuntu-buildscript install-packages [Path]``
Install the packages, specified in the profile, or contained in the 'custom-dpkgs' directory of each profile. Requires the environment to have already executed debootstrap.

### Build
- ``./ubuntu-buildscript build [Path]``
Create the ISO of the specified environment.

## ToDo
- [ ] Separate commands to individual modules
- [ ] Change the folder structure of ISO
- [ ] Create a package for Ubuntu
