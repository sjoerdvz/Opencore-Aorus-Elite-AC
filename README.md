# Opencore-Aorus-Elite-AC
OpenCore Gigabyte Z490 Aorus Elite AC

opencore 0.6.7 bootloader for gigabyte z490 Aorus Elite AC.
The purpose of this EFI is that anyone with the same board can run macOS BigSure without any problems without worrying about configurations.
all onboard hardware are working as normal even integreted wifi and bluetooth.

before use make sure you make some changes.if you have the onboard intel uhd 630 you ready to boot.

For RX580 remove boot-args "igfxonln=1".  
for 5600XT add boot-args "agdpmod=pikera".  

system plist is macpro 7.1
incl memory module mismatch configuration fix. you need to have 16gb ram installed.
To match your ram modules type,speed,serial use dmicode to get your Ram info.
https://dortania.github.io/OpenCore-Post-Install/universal/memory.html. 

i have romoved some unnecessary bios patches because we can disable this all in the bios settings. 
this result is faster and stable system, but you need set the bios settings cerrectly otherwise it wont boot.
if you want a dualboot system with windows,i have disable ACPI patching that prevent OC from injecting ACPI values 

To Enable Wifi use Heliport app easy way.                      
if you want wifi while installing or configuration macos on first time. you need to set your SSID and PASS in config.plist from "itlwm.kext" in Kext folder modify the file using xcode.    
Modify itlwm.kext/config.plist/IOKitPersonalities/itlwm/WiFiConfig for SSID and Pass

Fix no network cable error for Ethetnet. 
  go to network settings. choose left Ethernet choose advanced.
  go to hardware settins tab. 
  Use the following settings.  
 * configure = manually
 * Speed = 1000baseT
 * Duplex Full duplex 
 
Bios Version=F20b.  
Bios Settings (important)  
 * VT-D Disable.       
 * XMP profile Enable (if supported).    
 * Above 4G Decoding Enable.  
 * Resize-Bar Enable (only for 5600XT 5700XT).  
 * CFG Lock Disable.  
 * CSM Disable.   
 * Secureboot Disable.  
 * Windows Features set to window for Dualboot systems. if you not use windows 10 choose OtherOS.  
 * Optional you can use my bios from repo, it will boot with a blackscreen to open core.   
                https://github.com/sjoerdvz/Gigabyte-Z490-Aorus-Elite-AC-Bios.git

whats working 
* Audio
* Onboard Wifi 
* Onboard Bluetooth
* Airdrop
* incoming en outgoing calls from iphone working
* Bluetooth Accessoires working
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


