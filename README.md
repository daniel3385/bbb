# UNDER CONSTRUCTION!!!!!

# bbb
Beaglebone Black Hack's

## Das uboot bootloader compilation

To put the bootloader in a SD card, we need to compile it, here the steps:

* git clone git://git.denx.de/u-boot.git
* checkout some version ex: git checkout v2016.01-rc4 -b v2016.01-rc4
* cd u-boot
* export ARCH=arm
* export CROSS_COMPILE=arm-linux-gnueabi-
* make am335x_boneblack_defconfig
* make -j4

Formar a SD card to fat32(suggestion: use GParted tool), then copy MLO and u-image.img into it.

## Connect uart to Beaglebone Black throught cp2102 board

TODO: figure here
TODO: connection scheme here

After plug the cp2102 on usb computer, run "dmesg | tail" to see where is it in /dev/ (ex: /dev/ttyUSB0)
After that, start minicom and configure the device, baud rate to 115200 and disable software and hardware flow control.
Power up beaglebone Black holding S2 push button, then release it to boot from SD card.
