![](Images/swifitch_looong_header.png)

## Table of contents

- [Introduction](https://github.com/ArnieX/swifitch#introduction)
	- [What is it?](https://github.com/ArnieX/swifitch#what-is-it)
	- [What can it do?](https://github.com/ArnieX/swifitch#what-can-it-do)
	- [What is expected cost?](https://github.com/ArnieX/swifitch#what-is-expected-cost)
	- [How does it look like?](https://github.com/ArnieX/swifitch#how-does-it-look-like)
	- [How big is it?](https://github.com/ArnieX/swifitch#how-big-is-it)
	- [Is it safe?](https://github.com/ArnieX/swifitch#is-it-safe)
	- [OK I'm sold! What do I need to build it?](https://github.com/ArnieX/swifitch#ok-im-sold-what-do-i-need-to-build-it)
- [SeeedStudio Fusion PCB](https://github.com/ArnieX/swifitch#seeedstudio-fusion-pcb)
	- [How to order PCBs](https://github.com/ArnieX/swifitch#how-to-order-pcbs)
-  [After you build it](https://github.com/ArnieX/swifitch#after-you-build-it)
	- [OK DONE! What's next?](https://github.com/ArnieX/swifitch#ok-done-whats-next)
- [Software](https://github.com/ArnieX/swifitch#software)
	- [Swifitch default software](https://github.com/ArnieX/swifitch#swifitch-default-software)
	- [Custom software](https://github.com/ArnieX/swifitch#custom-software)
- [Enclosure](https://github.com/ArnieX/swifitch#enclosure)
	- [3D Printed](https://github.com/ArnieX/swifitch#3d-printed)
	- [Purchased ABS box](https://github.com/ArnieX/swifitch#purchased-abs-box)
- [Soldering cheatsheet](https://github.com/ArnieX/swifitch#soldering-cheatsheet)
	- [Back side](https://github.com/ArnieX/swifitch#back-side)
	- [Front side](https://github.com/ArnieX/swifitch#front-side)
- [Credits](https://github.com/ArnieX/swifitch#credits)
- [What's next?](https://github.com/ArnieX/swifitch#whats-next)
- [Photos](https://github.com/ArnieX/swifitch#photos)

# Introduction

### What is it?

ESP8266 based WiFi enabled relay board, that will let you easily turn any light or any plug to SMART one. Easily control using HomeKit (other HW needed) or using any MQTT based SmartHome application. Or if you are skilled developer, write any code you want.

### What can it do?

Main purpose is to turn things ON or OFF. But it can do lot more than that, swifitch is equiped with header to connect another 4 digital devices and 1 analog. These could be sensors etc.

If you need, by sacrificing one of the data pins, you can get 5V for your 5V sensors.

**⛔  Be aware that swifitch's pins are not 5V tolerant and cannot accept 5V on any of the pins provided, and it will damage the ESP.**

There are also two jumpers. One is for enabling deep sleep and the other is to put ESP into flash mode when you use conventional USB2UART programmer. We have reused one NodeMCU to make a lot more convenient programmer out of it, because it handles resets and flash mode boot automatically. Details will follow.

### What is expected cost?

We have designed swifitch to be both cheap and safe. So it is not ultra cheap but not expensive too. **Our cost calculations has stoped at $8!** Not bad, what you think?

### How does it look like?

Definitely beautiful!!

<img src="Images/3D_Vector_Swifitch2.png" width="700">

### How big is it?

Actually very small, you should be able to fit it almost anywhere without any hassle. But I know, numbers tell it all, so here it is.

|**Width**|**Height**|**Depth**|**Weight W/O BOX**|**Weight W/ BOX**|
|---|---|---|---|---|
| 42mm / 1.65" | 60.5mm / 2.36" | 19.6mm / 0.77" | ~42g / ~1.48oz | ~72g / ~2.54oz  |

### Is it safe?

We have designed few safety features in swifitch. Most important are fuses on mains input. There is one overcurrent fuse and one overvoltage fuse (surge protection), and more importantly temperature fuse that will disconnect swifitch from mains input when temperature raises above 100°C. There should be another few safeties in HLK-PM01 but we didn't want to depend on it's quality. 

### OK I'm sold! What do I need to build it?

**Capacitors**

|Preview|Part|Buy|
|---|---|---|
|<img src="Images/Parts/Capacitors_4.7uF.png" width="70">|4.7μF 0805|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/Free-shipping-0805-SMD-capacitor-4-7uf-50V-475Z-100PCS/32376068362.html?spm=2114.13010608.0.0.ztsIz3)|
|<img src="Images/Parts/Gray_BG_Parts/Capacitors_100nF.png" width="70">|100nF 0805|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/Free-shipping-0805-SMD-capacitor-100nf-0-1uf-50V-104Z-100PCS/32375582602.html?spm=2114.13010608.0.0.ztsIz3)|
|<img src="Images/Parts/Capacitors_10nF.png" width="70">|10nF 0805|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/Free-shipping-0805-SMD-capacitor-10nf-50V-103K-100PCS/32375924803.html?spm=2114.13010608.0.0.ztsIz3)|
|<img src="Images/Parts/Gray_BG_Parts/Capacitors_47uF.png" width="70">|47μF ⌀6.3x5mm|[<img src="Images/Shops/gray_farnell.png" width="35">](http://uk.farnell.com/multicomp/mcumr16v476m6-3x5/cap-alu-elec-47uf-16v-rad/dp/9452214?iscrfnonsku=true) [<img src="Images/Shops/gray_tme.png" width="30">](http://www.tme.eu/gb/details/umt1c470mdd/105c-tht-electrolytic-capacitors/nichicon/)|
|<img src="Images/Parts/Capacitors_47nF.png" width="70">|47nF X2|[<img src="Images/Shops/farnell.png" width="35">](http://uk.farnell.com/kemet/r463i24705001k/cap-film-pp-0-047uf-300vac-rad/dp/2446240?ost=R463I24705001K&searchView=table&iscrfnonsku=false) [<img src="Images/Shops/tme.png" width="30">](http://www.tme.eu/gb/details/r463i24705001k/x2y2-foil-polypropylene-capacitors/kemet/)|

**Resistors**

|Preview|Part|Buy|
|---|---|---|
|<img src="Images/Parts/Resistors_10k.png" width="80">|10kΩ 0805|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/100pcs-lot-SMD-Chip-Resistor-0805-10K-10K-ohm-5-Free-shippng/32382494431.html?spm=2114.13010608.0.0.nza8EJ)|
|<img src="Images/Parts/Gray_BG_Parts/Resistors_one_0805.png" width="80">|1.5kΩ 0805|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/New-100PCS-Lot-SMD-Resistance-0805-1K5-1-5K-5-1-8W-Chip-Resistors-Wholesale/32530331741.html?spm=2114.13010608.0.0.FKRHEz)|
|<img src="Images/Parts/Resistors_one_0805.png" width="80">|2.2kΩ 0805|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/New-100PCS-Lot-SMD-Resistance-0805-2K2-2-2K-5-1-8W-Chip-Resistors-Wholesale/32530124753.html?spm=2114.13010608.0.0.FKRHEz)|
|<img src="Images/Parts/Gray_BG_Parts/Resistors_one_0805.png" width="80">|47kΩ 0805|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/100pcs-lot-SMD-Chip-Resistor-0805-47K-47K-ohm-5-Free-shippng/32381859069.html?spm=2114.13010608.0.0.nza8EJ)|
|<img src="Images/Parts/Resistors_160R_1206.png" width="80">|160Ω 1206|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/Free-Shipping-100PCS-1206-160R-1206-160ohm-1-SMD-Resistor-160ohm/2043972079.html?spm=2114.13010608.0.0.iQHdt4)|
|<img src="Images/Parts/Gray_BG_Parts/S10K275.png" width="80">|S10K275|[<img src="Images/Shops/gray_farnell.png" width="35">](http://uk.farnell.com/epcos/b72210s0271k101/varistor-43-0j-275vac/dp/1004390?ost=B72210S0271K101&selectedCategoryId=&categoryNameResp=All%2BCategories&searchView=table&iscrfnonsku=false) [<img src="Images/Shops/gray_tme.png" width="30">](http://www.tme.eu/gb/details/siov-s10k275/tht-varistors/epcos/b72210s0271k101/)|

**Power and Controls**

|Preview|Part|Buy|
|---|---|---|
|<img src="Images/Parts/Fuse_Schurter.png" width="40">|SCHURTER MSF 250VAC 500mA Fuse|[<img src="Images/Shops/farnell.png" width="35">](http://uk.farnell.com/schurter/0034-6011/fuse-pcb-quick-blow-500ma/dp/1214681) [<img src="Images/Shops/tme.png" width="30">](http://www.tme.eu/gb/details/0034.6011/fuses-tr5-fast/schurter/)|
|<img src="Images/Parts/Gray_BG_Parts/Fuse_Temperature.png" width="40">|PROFFUSE TZ-P100/2 100°C Fuse|[<img src="Images/Shops/gray_tme.png" width="30">](http://www.tme.eu/gb/details/tz-p100_2/thermal-fuses/proffuse/)|
|<img src="Images/Parts/HLK-PM01.png" width="80">|Hi-Link HLK-PM01 AC-DC 5V/3W|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/Free-Shipping-10pcs-lot-HLK-PM01-AC-DC-220V-to-5V-mini-power-supply-module-intelligent/32688093777.html?spm=2114.13010608.0.0.T6S4Y8)|
|<img src="Images/Parts/Gray_BG_Parts/Relay.png" width="50">|SRD-05VDC-SL-C Relay|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/Free-shipping-SRD-5VDC-SL-C-5pins-SRD-05VDC-SL-C-Mini-Power-Relay-In-stock/1092738041.html?spm=2114.13010608.0.0.ztsIz3)|

**Other SMD Parts**

|Preview|Part|Buy|
|---|---|---|
|<img src="Images/Parts/BC817-16.215.png" width="20">|BC817-16.215|[<img src="Images/Shops/farnell.png" width="35">](http://uk.farnell.com/nxp/bc817-16-215/transistor-npn-45v-0-5a-sot-23/dp/8734739) [<img src="Images/Shops/tme.png" width="30">](http://www.tme.eu/gb/details/bc817-16.215/npn-smd-transistors/nxp/) [<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/100PCS-Lot-BC817-BC817-16-SOT-23-NPN-6C-0-1A-45V-general-purpose-transistor-NEW/32624683542.html?spm=2114.13010208.99999999.264.BYhv5u)|
|<img src="Images/Parts/Gray_BG_Parts/BAS86.png" width="22">|BAS86|[<img src="Images/Shops/gray_farnell.png" width="35">](http://uk.farnell.com/nxp/bas86/diode-schottky-sod-80/dp/8734542) [<img src="Images/Shops/gray_tme.png" width="30">](http://www.tme.eu/gb/details/bas86.115/smd-schottky-diodes/nxp/)|
|<img src="Images/Parts/MCP1825T-3302E-DC.png" width="30">|MCP1825T-3302E/DC Voltage Regulator|[<img src="Images/Shops/farnell.png" width="35">](http://uk.farnell.com/microchip/mcp1825t-3302e-dc/ic-ldo-3-3v-500ma-sot-223-5/dp/1578410) [<img src="Images/Shops/tme.png" width="30">](http://www.tme.eu/gb/details/mcp1825t-3302ed/ldo-unregulated-voltage-regulators/microchip-technology/mcp1825t-3302edc/)|
|<img src="Images/Parts/Gray_BG_Parts/FB1.png" width="18">|Ferrite Bead 600Ω 100MHz 0805|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/50pcs-SMD-bead-FB-0805-600R-100MHZ-600-600ohm-25-500mA-Ferrite/32637007661.html?spm=2114.13010608.0.0.ztsIz3)|
|<img src="Images/Parts/LED1.png" width="18">|Any 0805 LED diode|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/100pcs-Flashing-LEDs-SMD-0805-Red-Flashing-Diodes-Blinking-LED-Flash-0805-SMD-Diode-0805-smd/32366087497.html?spm=2114.13010608.0.0.FKRHEz)|

**Connectors**

|Preview|Part|Buy|
|---|---|---|
|<img src="Images/Parts/Header_1x2.png" width="30">|Headers 1x2 2.54mm pitch|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/10pcs-40-Pin-1x40-Single-Row-Male-2-54-Breakable-Pin-Header-Connector-Strip-for-Arduino/32641752713.html?spm=2114.13010608.0.0.U9AXxI)|
|<img src="Images/Parts/Gray_BG_Parts/Header_2x5.png" width="26">|Headers 2x5 2.54mm pitch|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/5-PCS-2-54mm-2-x-40-Pin-Male-Double-Row-Pin-Header-Strip/32216818428.html?spm=2114.01010208.3.2.5nQ4Vd)|
|<img src="Images/Parts/Terminal_2P_and_3P.png" width="100">|Terminal 2P and 3P, 5.08mm pitch rounded lead|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/wholesale?catId=0&initiative_id=SB_20170202034250&SearchText=terminal+5.08mm)|

**The rest**

|Preview|Part|Buy|
|---|---|---|
|<img src="Images/Parts/ESP8266_12.png" width="75">|ESP8266-12(E/F/S)|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/1PCS-ESP-12F-ESP-12E-upgrade-ESP8266-Remote-Serial-Port-WIFI-Wireless-Module-ESP8266/32714088769.html?spm=2114.13010608.0.0.4TnTET)|
|<img src="Images/Parts/Gray_BG_Parts/PCB.png" width="300">|PCB|[<img src="Images/Shops/gray_seeedstudio.png" width="30">](https://www.seeedstudio.com/fusion_pcb.html)|

Most of it could be purchased on AliExpress or eBay for what we call "no money", some parts are safer to get from your local trusted electricians shop (fuse and relay if you do not want chinese).

Most AliExpress links in table above are tested and trusted sellers, but we do not give any guarantees.

TME.eu is good source for EU citizens and especially guys in Czech Republic.

Farnell should be OK for all over world.

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

We have created software for you to get started quicky so go to it's own [repository](https://github.com/ArnieX/swifitch-software).

<img src="Images/Swifitch_NodeMCU.png" width="700">

**⚡ DO NOT CONNECT SWIFITCH TO MAINS VOLTAGE WHEN FLASHING ⚡**

It should be safe, but we do not recommend it!

# Software

### Swifitch default software

If you went with our software you are good to go, just follow the README in the [repository](https://github.com/ArnieX/swifitch-software).

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
|C10|47nF|
|C2|47μF|
|C9|47μF|
|SB1|Optionaly enable D5 or 5V|
|JP1|1x2 header|
|JP2|1x2 header|
|J3|2x5 header|
|RE1|Relay|
|J1|2P terminal|
|J2|3P terminal|

**🎉 DONE 🎉**

# Credits

- PCB design, electronics ideas, parts selection - Miroslav Batěk
- SW, Git Repo, design - Martin Doubek

# What's next?

If you liked swifitch and want to submerge deeper into IoT we will reference some other projects here.

- [tjclement's ESP8266 dimmer HW for LED Strips](https://github.com/tjclement/esp-dimmer-hardware)

# Photos

<img src="Images/Photo_Front.jpg" width="400"> <img src="Images/Photo_Back.jpg" width="400">
<img src="Images/Photo_Kaleidoscope_1.jpg" width="400"> <img src="Images/Photo_Kaleidoscope_2.jpg" width="400">

