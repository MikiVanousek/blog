---
layout: post
title: Root With Magdisk And TWRP Without Reinstalling System And Fix Safetynet
date: 210908 
---
This tutorial is meant for Arrow os on alioth (Poco F3)! On other devices the steps might be different!

Follow this on your own risk!

You need adb and fastboot installed to follow.

Edit 2: Location is now working as well. Everything is working.

# Root your system with magisk
 - Connect your phone to your PC
 - Download the [Magisk apk](https://github.com/topjohnwu/Magisk/releases/tag/v23.0)
 - Make a copy of the Magisk-v##.#.apk file with .zip extension. You should now have 2 files (.apk, .zip) 
 - Download and flash [TWRP](https://forum.xda-developers.com/t/recovery-unofficial-twrp-3-5-1-20210702.4300189/) - your system is going to stay intact
 - Boot to TWRP (adb reboot bootloader)
 - Upload the magisk.zip file
	adb push <path to your magisk.zip file> /sdcard/Download/
 - In TWRP press first big button 'Install', go to Download and select 
magisk.zip
 - In the next menu check 'Skip Digest check before installing zip' only! UNCHECK 'Inject TWRP after install'
- After the install, reboot to system. Install magisk.apk
	adb install Magisk-v##.#.apk
- When you open the Magisk app, it should say 'Installed: <your version>'

# Fixing Safetynet with Magdisk

 - Download the latest [fdroid apk](https://f-droid.org/en/packages/org.fdroid.fdroid/)
 - Install it with adb
 - In the F-Droid app find XPrivacyLua and install it
 - Download the latest [safetynet-fix-v#.#.#.zip](https://github.com/kdrag0n/safetynet-fix/releases).
 - In the settings of Magisk app check MagiskHide
 - In the Magisk app navigate to modules, 'Install from storage' and install the safetynet fix 
 - In the Magisk module search find 'Riru', install it **without rebooting**
 - In the same way install 'Lsposed', then reboot
 - Open Lsposed app, click 'Modules' -> 'XPrivacyLua' -> 3 dots in top right -> 'Hide' -> uncheck System apps
 - Now select:
   - System Framework
   - Settings Storage
   - Google Play Services
 - Reboot your device
 - Open XPrivacyLua app and check Google Play Services, expand the item and uncheck 'Get Location'
   and 'Get Sensors'
 - Clear storage for Google Play Services and Google Play in Settings -> Apps

Congratulations, you should now be able to pass the Safetynet.
Please, let me know [on XDA](https://forum.xda-developers.com/t/rom-11-0-0-alioth-aliothin-arrowos-11-0-official-weekly.4279481/post-85599629) if it worked for you!
This is my first contribution to this community, and I am generally curious as to how many people it might help. 

If it did not work or, you do not understand something, also let me know and I will try to fix it... 
