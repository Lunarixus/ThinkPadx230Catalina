# ThinkPadx230Catalina
Fully working Clover EFI setup for Catalina 10.15.4 on the ThinkPad x230

# What's working
- WiFi (with swapped card)
- Bluetooth
- Native power management
- Battery status
- Brightness control
- Audio
- Ethernet
- iMessage and FaceTime
- Laptop sleep/idle

# Any bugs
- VGA since no real Mac's have it

# Setup
Setup is easy, just replace the stock EFI folder with this one

# My specs
- i5 3320M
- 8GB of RAM
- 80GB Intel SSD
- Dell DW1510 (BCM4322)

# WiFi Card swap
The ThinkPad x230 now has an exploit named 1vyRa1n which installs a custom BIOS with the WiFi whitelist removed.  
Thus it is much easier to now get macOS supported WiFi cards. I use the DW1510 because it works well.  

1vyRa1n instructions can be found here: https://github.com/n4ru/1vyrain  

You can get the Dell DW1510 for cheap on AliExpress or eBay.  

Instructions to make the Dell DW1510 work again in Catalina:  

Run these commands to remove the old kexts:  
```sudo mount -uw /```  
```sudo rm -rf /System/Library/Extensions/IO80211Family.kext && sudo rm -rf /System/Library/Extensions/IO80211FamilyV2.kext```  

Then download the new kexts from here: https://drive.google.com/file/d/1rRq4auOy6dN9wf6T0zPRbUXPmgX_JXX-/view?usp=sharing  
This will also be required for the Atheros cards along with Atheros injector kexts (and fake PCI ID's if required).  

# Trackpoint workaround
For scrolling with the middle button on the trackpoint you can use smart scroll for macOS.  
Link: https://www.marcmoini.com/sx_en.html

# Credits
- Lunarixus for creating new DSDT and SSDT models.
- Bizarro for the LED and brightness control workarounds.
- RehabMan for the USB and battery patches.

> Bring on Big Sur!
