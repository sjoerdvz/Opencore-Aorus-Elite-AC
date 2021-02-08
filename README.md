# Opencore-Aorus-Elite-AC
OpenCore Gigabyte Z490 Aorus Elite AC

opencore 0.6.6 bootloader for gigabyte z490 Aorus Elite AC.
The purpose of this EFI is that anyone with the same board can run macOS BigSure without any problems without worrying about configurations.
all onboard hardware are working as normal even integreted wifi and bleutooth.

Default plist is now set to imac 20,1 
if you have a radeon 5600XT 5700XT or similar your ready to go, when using a RX590 RX580 you need to make chage to the config.plist.
for RX590 RX580 remove the line "agdpmod=pikera" in NVRam boot-args

Fix no network cable error for Ethetnet 


whats working 
* Audio
* Boot chime (When Enable)
* Onboard Wifi 
* Onboard Bleutooth
* Facetime
* iMessage
* Network
* Usb 2.0
* Usb 3.0
* FileVault
* HandOff
* Bootcamp
* NvRam
* Sleep
* Wake




Bios Version=F20b

Bios Settings *(important)

*VT-D Disable

XMP profile Enable

*Above 4G Decoding Enable

Resize-Bar Enable

*CFG Lock Disable

*CSM Disable

*Secureboot Disable
