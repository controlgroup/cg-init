CG-INIT TEMPLATE
================

	The goal of cg-init is to create a git-based project repo template. The cg-init flow is as follows:

        1) A CG github admin clones this repo via the cg-init command
        2) The initial developer edits the puppets site.pp and module init.pp files for the respective project
        3) All onboarding members of the project change directory to setup/ and run the install.sh <arch> script to bootstrap their environment.

Setup Instructions
==================

The following are prerequisites for using the install script: [Vagrant](http://www.vagrantup.com/), [Virtualbox](https://www.virtualbox.org/), [Packer](http://www.packer.io/). The versions listed below were the most up-to-date as of November 6, 2013.

Installing Vagrant:

- [Download and install 1.3.5 dmg](http://downloads.vagrantup.com/)

Virtualbox:

- [Download and install 4.3.2 dmg for OS X x386](https://www.virtualbox.org/wiki/Downloads)

Packer:

- [Download zip file for amd64 mac](https://www.packer.io/downloads.html) *Note Requires Packer 0.5+
- Unzip, rename folder to "packer", and move folder to /usr/local/bin
- Add /usr/local/bin/packer to $PATH
- Optionally you can use a package manager to install packer


To boostrap environment run, change directory to setup/ and run the install.sh script passing the host architecture as an agrument:

     $ ./install.sh mac
     
NOTE: When the  installation reaches the point shown below, it may seem as if it is "hanging". It is not. It is normal at this stage for no additional output to appear for 10-20 minutes. It is still installing; do not try to kill the process.

    ==> virtualbox: Waiting for SSH to become available...
