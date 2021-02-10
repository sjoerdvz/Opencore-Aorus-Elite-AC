# Opencore-Aorus-Elite-AC
OpenCore Gigabyte Z490 Aorus Elite AC

opencore 0.6.6 bootloader for gigabyte z490 Aorus Elite AC.
The purpose of this EFI is that anyone with the same board can run macOS BigSure without any problems without worrying about configurations.
all onboard hardware are working as normal even integreted wifi and bleutooth.

Default plist is now set to imac 20,1
i have created a serial to start. but you need to make your own and Mac Adres also
you can use latest opencore configurator tool from the web, its easy to use for this.
follow Dortania's opencore guide for this its verry easy 
[https://dortania.github.io/OpenCore-Install-Guide/config.plist/comet-lake.html#platforminfo/]


if you have a radeon 5600XT 5700XT or similar your ready to go, when using a RX590 RX580 you need to make chage to the config.plist.
for RX590 RX580 remove the line "agdpmod=pikera" in NVRam boot-args


i have romoved some unnecessary bios patches because we can disable this all in the bios settings. 
this result is faster and stable system, but you need set the bios settings cerrectly otherwise it wont boot.
if you want a dualboot system with windows,i have disable ACPI patching that prevent OC from injecting ACPI values 

Fix no network cable error for Ethetnet. 
  go to network settings. choose left Ethetnet choose advanced.
  go to hardware settins tab. 
  Use the following settings. 

 * configure = manually
 * Speed = 1000baseT
 * Duplex Full duplex 

Bios Version=F20b

Bios Settings (important)
 * VT-D Disable
 * XMP profile Enable (if supported)
 * Above 4G Decoding Enable
 * Resize-Bar Enable (only for 5600XT 5700XT)
 * CFG Lock Disable
 * CSM Disable
 * Secureboot Disable
 * Windows 8/10 Features set to window 10 for dualboot systems. if not use OthetOS


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
