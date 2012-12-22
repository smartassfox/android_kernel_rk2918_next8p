RK2918 Kernel optimized for Nextbook 8 Premium 
=====================

Kernel based on crewtablet's NEOX kernel. Thanks guys!

###Prerequisites
* CodeSourcery's [ARM-2010.09.50 gnueabi toolchain](http://www.codesourcery.com/sgpp/lite/arm/portal/package7851/public/arm-none-linux-gnueabi/arm-2010.09-50-arm-none-linux-gnueabi-i686-pc-linux-gnu.tar.bz2)

###Building

Use Ubuntu 10.04 or 10.10, not tested on newer versions

> export CROSS_COMPILE=/path/to/the/toolchain/arm-none-linux-gnueabi-

> make clean && make mrproper

> make NEXT8P_defconfig (for Nextbook 8 Premium build)

> make menuconfig (for modules and overclock)

> make ARCH=arm

> ./mkkrnlimg arch/arm/boot/Image nameofyourkernel.img

You'll now have a RK2918 compatible kernel.img!

###Special stuff
Inside menuconfig you'll find Overclock settings, not set in NEXT8P_defconfig because a minor number tablets have issues with OC.
