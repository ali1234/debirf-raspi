Build a Raspbian ramdisk image using Debirf.

Usage:

You have to run this on Raspbian, or at least an ARM system.

* Install dependencies.
  - sudo apt-get install debirf
* Run ./build
* Format an SD card with just a FAT partition.
* Copy boot/* to SD card.
* Put SD card into Raspberry Pi and boot.

Hacking:

* Write modules to install whatever software you need. 
* Check modules-available and /usr/share/debirf/modules for examples.
* Link your modules in modules/ directory in the build tree.
* If rebuilding a lot, use apt-cacher-ng (maybe on another computer):
  - sudo apt-get install apt-cacher-ng
  - export http_proxy=http://address:3142
  - ./build
