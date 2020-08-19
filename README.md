# NanoPi NEO3

A tiny Rockchip RK3328 SoC, less power consumption.
Works perfectly in my music system as a network audio interface (HQPlayer NAA and ROON Bridge).

The company FriendlyELECI they do only offer Ubuntu with 5.4 kernel, therefore, I decided to compile NanoPi NEO3 bootloader images (official u-boot v2020.07 release), and finally get ArchLinux with customized mainline realtime kernel installed on this board.
 
# Install to a micro SD card:
(replace sdx with the device name for the SD card on your computer)

dd if=idbloader.img of=/dev/sdx seek=64 conv=notrunc
dd if=uboot.img of=/dev/sdx seek=16384 conv=notrunc
dd if=trust.img of=/dev/sdx seek=24576 conv=notrunc
