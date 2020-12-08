# Opencore-Aorus-Elite-AC
OpenCore Gigabyte Z490 Aorus Elite AC

opencore 0.6.4 bootloader for gigabyte z490 Aorus Elite AC.
The purpose of this EFI is that anyone with the same board can run macOS BigSure without any problems without worrying about configurations.
all onboard hardware are working as normal even integreted wifi and bleutooth.

if you wanna change de configuration plist only use MacPro 7.1 if you want bleutooth keeps working
you get a one message about Memory mismatch configuration, deal with. you can patch the plist to match all 12 slots but your audio will stop working and the OS will be verry slow because we dont have 12 slots on our mothetboard 

whats working 
* Audio
* Boot chime (When Enable)
* Boot Screen 
* Wifi 
* Bleutooth
* Facetime
* iMessage
* Network
* Usb 2.0
* Usb 3.0
* FileVault
* HandOff
* NvRam
* Shutdown
* Sleep
* Wake
