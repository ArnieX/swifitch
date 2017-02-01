![](Images/swifitch_looong_header.png)

## Table of contents

- [Introduction]()
	- [What is it?]()
	- [What can it do?]()
	- [What is expected cost?]()
	- [How does it look like?]()
	- [How big is it?]()
	- [Is it safe?]()
	- [OK I'm sold! What do I need to build it?]()
- [SeeedStudio Fusion PCB]()
	- [How to order PCBs]()
-  [After you build it]()
	- [OK DONE! What's next?]()
- [Software]()
	- [Swifitch default software]()
	- [Custom software]()
- [Enclosure]()
	- [3D Printed]()
	- [Purchased ABS box]()
- [Soldering cheatsheet]()
	- [Back side]()
	- [Front side] ()
- [Credits]()
- [What's next?]()
- [Photos]()

# Introduction

### What is it?

ESP8266 based WiFi enabled relay board, that will let you easily turn any light or any plug to SMART one. Easily control using HomeKit (other HW needed) or using any MQTT based SmartHome application. Or if you are skilled developer, write any code you want.
<br><br>
### What can it do?

Main purpose is to turn things ON or OFF. But it can do lot more than that, swifitch is equiped with header to connect another 4 digital devices and 1 analog. These could be sensors etc.
<br>
If you need, by sacrificing one of the data pins, you can get 5V for your 5V sensors.
<br><br>
**⛔  Be aware that swifitch's pins are not 5V tolerant and cannot accept 5V on any of the pins provided, and it will damage the ESP.**
<br><br>
There are also two jumpers. One is for enabling deep sleep and the other is to put ESP into flash mode when you use conventional USB2UART programmer. We have reused one NodeMCU to make a lot more convenient programmer out of it, because it handles resets and flash mode boot automatically. Details will follow.
<br><br>
### What is expected cost?

We have designed swifitch to be both cheap and safe. So it is not ultra cheap but not expensive too. **Our cost calculations has stoped at $8!** Not bad, what you think?
<br><br>
### How does it look like?

Definitely beautiful!!
<br>
<img src="Images/3D_Vector_Swifitch2.png" width="700">
<br><br>
### How big is it?

Actually very small, you should be able to fit it almost anywhere without any hassle. But I know, numbers tell it all, so here it is.

|**Width**|**Height**|**Depth**|**Weight W/O BOX**|**Weight W/ BOX**|
|---|---|---|---|---|
| 42mm / 1.65" | 60.5mm / 2.36" | 19.6mm / 0.77" | ~42g / ~1.48oz | ~72g / ~2.54oz  |

### Is it safe?

We have designed few safety features in swifitch. Most important are fuses on mains input. There is one overcurrent fuse and more importantly temperature fuse that will disconnect swifitch from mains input when temperature raises above 100°C. There should be another few safeties in HLK-PM01 but we didn't want to depend on it's quality. 

### OK I'm sold! What do I need to build it?

Except the PCB and casing, here is the part's list.

![](Images/Swifitch_PCB_parts_list.png)

Most of it could be purchased on AliExpress or eBay for what we call "no money", some parts are safer to get from your local trusted electricians shop (fuse and relay if you do not want chinese). We'll post links for trusted and tested AliExpress sellers for some of the parts.

- For PCB we have good experience with guys at [SeeedStudio](https://www.seeedstudio.com)
- ESP8266-12F were always best quality from this [seller](https://www.aliexpress.com/item/1PCS-ESP-12F-ESP-12E-upgrade-ESP8266-Remote-Serial-Port-WIFI-Wireless-Module-ESP8266/32714088769.html?spm=2114.13010608.0.0.4TnTET)

- [SMD 1206 - 160R](https://www.aliexpress.com/item/Free-Shipping-100PCS-1206-160R-1206-160ohm-1-SMD-Resistor-160ohm/2043972079.html?spm=2114.13010608.0.0.iQHdt4)
- [Relay SRD-05VDC-SL-C](https://www.aliexpress.com/item/Free-shipping-SRD-5VDC-SL-C-5pins-SRD-05VDC-SL-C-Mini-Power-Relay-In-stock/1092738041.html?spm=2114.13010608.0.0.ztsIz3)
- [FB 0805 600R 100MHz](https://www.aliexpress.com/item/50pcs-SMD-bead-FB-0805-600R-100MHZ-600-600ohm-25-500mA-Ferrite/32637007661.html?spm=2114.13010608.0.0.ztsIz3)
- [0805 SMD capacitor 100nF](https://www.aliexpress.com/item/Free-shipping-0805-SMD-capacitor-100nf-0-1uf-50V-104Z-100PCS/32375582602.html?spm=2114.13010608.0.0.ztsIz3)
- [0805 SMD capacitor 10nF](https://www.aliexpress.com/item/Free-shipping-0805-SMD-capacitor-10nf-50V-103K-100PCS/32375924803.html?spm=2114.13010608.0.0.ztsIz3)
- [0805 SMD capacitor 4.7uF](https://www.aliexpress.com/item/Free-shipping-0805-SMD-capacitor-4-7uf-50V-475Z-100PCS/32376068362.html?spm=2114.13010608.0.0.ztsIz3)
- [0805 SMD resistor 1K5](https://www.aliexpress.com/item/New-100PCS-Lot-SMD-Resistance-0805-1K5-1-5K-5-1-8W-Chip-Resistors-Wholesale/32530331741.html?spm=2114.13010608.0.0.FKRHEz)
- [0805 SMD resistor 2K2](https://www.aliexpress.com/item/New-100PCS-Lot-SMD-Resistance-0805-2K2-2-2K-5-1-8W-Chip-Resistors-Wholesale/32530124753.html?spm=2114.13010608.0.0.FKRHEz)
- [0805 SMD resistor 10K](https://www.aliexpress.com/item/100pcs-lot-SMD-Chip-Resistor-0805-10K-10K-ohm-5-Free-shippng/32382494431.html?spm=2114.13010608.0.0.nza8EJ)
- [0805 SMD resistor 47K](https://www.aliexpress.com/item/100pcs-lot-SMD-Chip-Resistor-0805-47K-47K-ohm-5-Free-shippng/32381859069.html?spm=2114.13010608.0.0.nza8EJ)
- [0805 SMD LED](https://www.aliexpress.com/item/100pcs-Flashing-LEDs-SMD-0805-Red-Flashing-Diodes-Blinking-LED-Flash-0805-SMD-Diode-0805-smd/32366087497.html?spm=2114.13010608.0.0.FKRHEz)
- [HLK-PM01](https://www.aliexpress.com/item/Free-Shipping-10pcs-lot-HLK-PM01-AC-DC-220V-to-5V-mini-power-supply-module-intelligent/32688093777.html?spm=2114.13010608.0.0.T6S4Y8)
- [2.54mm header](https://www.aliexpress.com/item/10pcs-40-Pin-1x40-Single-Row-Male-2-54-Breakable-Pin-Header-Connector-Strip-for-Arduino/32641752713.html?spm=2114.13010608.0.0.U9AXxI)

Components that we haven't listed will be up to you to find and obtain.

# SeeedStudio Fusion PCB

### How to order PCBs

First grab gerber files ZIP and upload it to SeeedStudio Fusion then follow instructions below.

We have created sreenshots from ordering process so you can recreate the process in same manner. Decide how many pieces you want and get started. Keep in mind that each board are actually two swifitches ;). That makes it even cheaper.

<img src="Images/SeeedStudio_Order.png" width="900">

Gerber files preview:

<img src="Images/SeeedStudio_Order_Gerber.png" width="900">

# After you build it

### OK DONE! What's next?

Now you need to flash some software to it. Either use conventional CP2102 USB2UART programmer or build your own as we did from NodeMCU, it is definitely best option you have.

This image tell you all you need to know but basically this is the list of steps:

- Desolder ESP8266 from NodeMCU (Heatgun baby!! But carefully you can use it for swifitch then.)
- Solder colored wires to the contacts according to image below
- Insert these wires to 2x5, 2.54mm pitch connector
- Connect to swifitch and flash firmware

We have created software for you to get started quicky so go to it's own [repository](#).

<img src="Images/Swifitch_NodeMCU.png" width="700">

**⚡ DO NOT CONNECT SWIFITCH TO MAINS VOLTAGE WHEN FLASHING ⚡**

It should be safe, but we do not recommend it!

# Software

### Swifitch default software

If you went with our software you are good to go, just follow the README in the [repository](#).

### Custom software

Just few things you need to know if you develop your own software.

- Relay is controled by D1 or GPIO5 PIN
- Built in LED is controled by D6 or GPIO12 PIN

# Enclosure

### 3D Printed

If you have access to 3D printer, have a look at our original swifitch box.

**This is experimental, not printed yet. Feel free to be first one.**

<img src="Images/swifitch_box_transp.png" width="500">

Use ABS plastic filament as this device is using mains voltage and ABS is safer for such devices.

**DO NOT USE CONDUCTIVE FILAMENTS**

### Purchased ABS box

We have fitted swifitch to box that can be purchased from various electrical shops. May not be available in all countries thought.

<br>
# Soldering cheatsheet

### Back side

Start with SMD parts on the BACK side.

**Capacitors**

|Slot|Part|
|---|---|
|C1|4.7μF|
|C3|4.7μF|
|C5|4.7μF|
|C6|4.7μF|
|C4|100nF|
|C7|100nF|
|C8|10nF|

**Resistors**

|Slot|Part|
|---|---|
|R3|10kΩ|
|R4|10kΩ|
|R5|10kΩ|
|R6|10kΩ|
|R7|10kΩ|
|R8|2.2kΩ|
|R9|47kΩ|
|R10|160Ω|
|R11|160Ω|

**The rest**

|Slot|Part|
|---|---|
|FB1|FB 600Ω 100MHz|
|D1|BAS86|
|T1|BS817|
|WiFi1|ESP8266-12(E/F/S)|

### Front side

Front side contains mostly THT parts, but start with SMD parts that would be harder to solder when you finish all bigger parts.

**SMD**

|Slot|Part|
|---|---|
|R1|470Ω > 2kΩ (depends on LED1)|
|LED1|Choose color you like|
|V1|Voltage Regulator|

**THT**

|Slot|Part|
|---|---|
|DC1|HLK-PM01|
|F2|100°C fuse|
|R2|S10K275|
|F1|MSF250/0.5A|
|C10|47μF|
|C2|47μF|
|C9|47μF|
|SB1|Optionaly enable D5 or 5V|
|JP1|1x2 header|
|JP2|1x2 header|
|J3|2x5 header|
|RE1|Relay|
|J1|2P terminal|
|J2|3P terminal|

<br>
**🎉 DONE 🎉**

<br>
# Credits

- PCB design, electronics ideas, parts selection - Miroslav Batěk
- SW, Git Repo, design - Martin Doubek

<br>
# What's next?

If you liked swifitch and want to submerge deeper into IoT we will reference some other projects here.

- [tjclement's ESP8266 dimmer HW for LED Strips](https://github.com/tjclement/esp-dimmer-hardware)

<br>
# Photos

<img src="Images/Photo_Front.jpg" width="200"> <img src="Images/Photo_Back.jpg" width="200">
<img src="Images/Photo_Kaleidoscope_1.jpg" width="200"> <img src="Images/Photo_Kaleidoscope_2.jpg" width="200">

