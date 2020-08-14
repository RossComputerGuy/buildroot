Intro
=====

This default configuration will allow you to start experimenting with the
buildroot environment for the Braveheart Edition of PinePhone. With the current configuration
it will bring-up the board, and allow access through the serial console.

PinePhone link:
https://www.pine64.org/pinephone/

Wiki link:
https://wiki.pine64.org/index.php/PinePhone

This configuration uses PINE64 U-Boot and megi's Linux kernel.

How to build
============

    $ make pine64_braveheart_defconfig

    $ make

Note: you will need access to the internet to download the required
sources.

How to write the SD card
========================

Once the build process is finished you will have an image called "sdcard.img"
in the output/images/ directory.

Copy the bootable "sdcard.img" onto an SD card with "dd":

  $ sudo dd if=output/images/sdcard.img of=/dev/sdX
  $ sudo sync

Insert the micro SDcard in your PinePhone Braveheart Edition and power it up. The console
is on the serial line, 115200 8N1.
