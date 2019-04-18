# minimosd-extra

Quickstart Guide (c) Johnex
----------------------
1. Download the latest MinimOSD-Extra build here: https://github.com/night-ghost/minimosd-extra/blob/master/osd_latest.zip?raw=true
2. Run the OSD_Config.exe
3. Connect your MinimOSD to your pc making sure you are using an FTDI that has 5V and not 3.3V.
4. After the usb driver is installed, select your COM port in OSD_Config.
5. Click Options -> Update Firmware. Select the Character_Updater_FW.hex file from the "FW_+_Char" folder.
6. This is a character set uploader, so just click Options -> Update CharSet. Select the latest character set MinimOSD_2.4.1.X.mcm from the "FW_+_Char" folder. Notice that this MimimOSD-Extra has a custom character set and must be updated if coming from another fork or the original, and some newer versions might require a new version, always check the "FW_+_Char" folder.
7. Click Options -> Update Firmware again. Select the latest MinimOsd_Extra_Uni.9XXDV-release.hex file from the "FW_+_Char" folder.
8. Set your video mode to Auto if you have different cam types, or select NTSC or PAL if you have just 1 cam and you know it's type or had issues with Auto.
9. Connect your OSD directly to a monitor or to a video transmitter so you can see the OSD output, making sure you don't forget to connect the antenna to the video transmitter before powering it on if you are using that. Click Options -> Load TLog. Select 2015-09-06 18-40-55.tlog from the "FW_+_Char" folder.
10. Set up the screens as you want. Click "Save Tab to OSD" and then click "Start" to run a simulation so you can see how everything looks without having to set up a copter. If something is not right, click "Stop", do the changes, save the config again and click "Start" again to see the new changes.
11. If you encounter that your screen is not centered, change the "Offsets", Left and Top from the config page. You can also move panels away from the edge if your screen gets cropped.



Description


* refactored a bit - now uses much less memory and can use less EEPROM

* also MAX7456 renew doing in VSYNC to get rid of "snow" on screen - like 
in http://forum.rcdesign.ru/f90/thread132831-195.html#post5602416 but on interrupt instead of polling via SPI.

* Also PSTR to all strings

* NEW FEATURES:

* 4 screens instead of 2

* individual control of sign icon of each panel per screen

* voltage, current & RSSI can be used from external pins

* TLOG player in configurator - now settings can be checked without working plane/copter!

* RADAR (like in MiniNAZAosd) and ILS in Horizon, can be enabled individually

* horizon angles can be adjusted, indepentently in PAL and NTSC

* PAL/NTSC detected dynamically - now can use different cameras!

* screen offsets via configurator

* can use additional pins (that can be found on some boards) for measuring 2nd battery current and voltage

* new GPS coords - in one line

* fixed a lot of old bugs of CT

* Any RC channel can be translated to output pin (eg. for cameras switch)

* Setup screen! Some parameters can be adjusted without computer - by RC 

* Panel in CT can be dragged over any point, not only for the upper left corner

* and much more! See [CHANGELOG.md](https://github.com/night-ghost/minimosd-extra/blob/master/CHANGELOG.md)

If you like this project and want to support further development - you can do it! [![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=SLUC8B3U7E7PS)USD
  [![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=HXRA6EXZJ489C) EUR


changelog in [CHANGELOG.md](https://github.com/night-ghost/minimosd-extra/blob/master/CHANGELOG.md)
some descriptions are in [wiki](https://github.com/night-ghost/minimosd-extra/tree/master/wiki)

fonts:

MinimOSD_2.4.1.x.mcm         - base font
MinimOSD_2.4.1.x-digital.mcm - styled for 7-segment and dotted horizon



Attention! This version is incompatible with the tools from the ArduCam and original MinimOSD-extra!

Discussion forum - http://www.rcgroups.com/forums/showthread.php?t=2591835 (abandoned) http://www.ykoctpa.ru/groups/eye-in-a-sky/forum/topic/minimosd-english-support-thread/#post-9147
