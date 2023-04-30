## Flashing RETROFIT ROM Guide

* How to Flash Using Retrofit OrangeFox/TWRP Recovery

{% include alerts/warning.html content="Follow the following guide to install PixelExperience 13 on mido.
Note: This in a RETROFIT build so follow the guide given below or you will be stucked."%}

1. Clean Flash 
• Clean flash is mandatory: you are required to backup all of your existing data to your computer or your preferred cloud service and avoid using nandroid backup.

2. Flash RETROFIT Recovery
• Flash the new RETROFIT OrangeFox/TWRP Recovery: (Mandatory) due to various changes in fstab file, you are required to flash the new RETROFIT recovery of which the link is undermentioned 

[ORANGEFOX](https://sourceforge.net/projects/nranjan-17/files/RETROFIT%20OrangeFox/OrangeFox-R11.1-A12-RETROFIT-Unofficial-mido.zip/download) 
[TWRP](https://sourceforge.net/projects/alone0316/files/recovery/twrp-3.7.0_12.0-mido-A13.img/download)

3. How to Flash Recovery
• Reboot to your existing recovery
• Wipe cache, data, system, vendor and Format Data
• Flash the RETROFIT Supported Recovery
• Reboot to Recovery (If flashing Orangefox it will be automatically rebooted to OrangeFox Recovery)

4. Wipe and format Device (Both are different)
• After you flash and boot into the new TWRP recovery, format data and reboot to the recovery again. 
Now, wipe all the partitions (i.e. cache, metadata, data, internal storage). Wiping Internal might throw an error because of missing /data/media/ which is okay, reboot to recovery again.  
This format data and wiping of other partitions is required only once every clean flash.
NB : encryption is now enabled by default and that is why a clean flash would cost you a data format.

4. Flash ROM
*To use internal storage for transferring files from PC 

From TWRP > tap Advanced > Terminal > run command:
```
mkdir -p /data/media/0/
```

• Copy the latest releases PixelExperience Android 13 rom to your internal storage/otg media/sd card etc. 
• Flash the ROM
• Format data 
• Reboot to system (it may show no os installed ignore it, if it doesn't boot then flash the ROM again and reboot to system)

6. Go Back 
If you want to go back to the previous version of Android. 
You need to flash your old recovery and Wipe and Format device ,Flash ROM again.

* How To Flash Using AOSP Recovery
1. Download the AOSP Recovery from the PE website
2. Copy the recovery to PC/laptop
3. Connect your device with PC/laptop (USB debugging should be turned on)
4. Reboot to fastboot 
5. Flash the recovery
6. Boot to recovery 
7. Format data using the recovery
8. On the device, select “Advanced”, “ADB Sideload”, then swipe to begin sideload.
9. On the PC/laptop, sideload the package using: adb sideload filename.zip
10. Format data
11. Reboot to system
