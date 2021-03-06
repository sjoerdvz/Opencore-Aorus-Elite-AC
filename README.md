# Opencore-Aorus-Elite-AC
OpenCore Gigabyte Z490 Aorus Elite AC

opencore 0.6.7 bootloader for gigabyte z490 Aorus Elite AC.
The purpose of this EFI is that anyone with the same board can run macOS BigSure without any problems without worrying about configurations.
all onboard hardware are working as normal even integreted wifi and bluetooth.

before use make sure you make some changes.
if you have the onboard intel uhd 630 you ready to boot and use

For RX580 remove boot-args "igfxonln=1"

for 5600XT add boot-args "agdpmod=pikera"

system plist is macpro 7.1
incl memory module mismatch configuration fix. you need to have 16gb ram installed or make some changes to plist
on platformInfo/memory, set to match your ram memory modules speed and size.

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
 * Windows 8/10 Features set to window 10 for dualboot systems. if not use OtherOS
 
 * Optional you can use my bios from repo, it will boot with a blackscreen to open core 
 
[https://github.com/sjoerdvz/Gigabyte-Z490-Aorus-Elite-AC-Bios.git]

whats working 
* Audio
* Boot chime (When Enable)
* Onboard Wifi 
* Onboard Bluetooth
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
