![](Images/swifitch_looong_header.png)

|<img src="Images/english_flag.png" width="30">|[Readme in English](https://github.com/ArnieX/swifitch/blob/master/README.md)|
|---|---|

## Obsah

- [Úvod](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#úvod)
	- [Co to je?](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#co-to-je)
	- [Co to umí?](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#co-to-umí)
	- [Na kolik to vyjde?](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#na-kolik-to-vyjde)
	- [Jak to vypadá?](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#jak-to-vypadá)
	- [Jak je to velké?](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#jak-je-to-velké)
	- [Co bezpečnost?](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#co-bezpečnost)
	- [Chci to! Co potřebuji koupit?](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#chci-to-co-potřebuji-koupit)
- [SeeedStudio Fusion PCB](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#seeedstudio-fusion-pcb)
	- [Jak objednat plošné spoje](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#jak-objednat-plošné-spoje)
-  [Po sestavení](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#po-sestavení)
	- [Hotovo! Co dál?](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#hotovo-co-dál)
- [Software](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#software)
	- [Náš základní software](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#náš-základní-software)
	- [Vlastní software](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#vlastní-software)
- [Krabička](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#krabička)
	- [Vytištěná na 3D tiskárně](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#vytištěná-na-3d-tiskárně)
	- [Kupovaná krabička](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#kupovaná-krabička)
- [Návod na pájení](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#návod-na-pájení)
	- [Zadní strana](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#zadní-strana)
	- [Přední strana](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#přední-strana)
- [Zásluhy](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#zásluhy)
- [Co dál?](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#co-dál)
- [Fotografie](https://github.com/ArnieX/swifitch/blob/master/README_CZ.md#fotografie)

# Úvod

### Co to je?

Swifitch je zjednodušeně WiFi spínač, založený na známém modulu ESP8266 ve verzi 12(E,F,S) a umožní vám proměnit jakékoliv světlo nebo zásuvku v dálkově ovládanou. Pak lze ovládat přes HomeKit (Potřeba dalšího zařízení - serveru) nebo přes jakoukoliv aplikaci, která umožňuje ovládání přes protokoly MQTT nebo HTTP. Velice záleží na softwaru, který si do zařízení nahrajete.

### Co to umí?

Jak už z názvu vyplývá hlavní funkcí je připojené zařízení zapínat nebo vypínat. Tím to ale nekončí, přidali jsme rozhraní pro připojení dalších 4 digitálních a jednoho analogového zařízení, tím může být prakticky cokoliv, teplotní čidlo, senzor pohybu nebo jiný senzor či modul.

Obětováním jednoho datového pinu lze získat 5V pro senzory nebo jiné moduly vyžadujících pro svou činnost 5V.

**⛔  Pozor, swifitch přesto, že umožňuje aktivaci výstupu 5V neumožňuje vstup 5V na žádném dostupném pinu, pokud by jste připojili 5V na některý pin, zničíte modul ESP8266.**

Kromě vstupně-výstupních pinů jsou k dispozici také dvě přemostění, první umožňuje využití režimu hlubokého spánku, druhé je nezbytné pokud pro nahrávání softwaru budete využívat běžný USB2UART programátor. Naše doporučení je využít pro programování upravený NodeMCU vývojový modul a to proto, že se sám stará o aktivaci flashovacího režimu a restarty modulu, víc dále.

### Na kolik to vyjde?

Navrhli jsme swifitch aby byl levný a zároveň bezpečný, takže není ani extrémně levný, ale ani drahý. **Celková konečná cena druhé verze je přibližně 215Kč!** To není zlé co myslíte?

### Jak to vypadá?

Naprosto a jednoznačně krásně!

<img src="Images/3D_Vector_Swifitch2.png" width="700">

### Jak je to velké?

Velké ani ne, spíše malé. Neměl by být problém napasovat swifitch kamkoliv jej budete chtít umístit. Je mi to jasné, čísla to poví lépe.

|**Šířka**|**Výška**|**Hloubka**|**Váha bez krabičky**|**Váha s krabičkou**|
|---|---|---|---|---|
| 42mm | 60.5mm | 19.6mm | ~42g | ~72g |

### Co bezpečnost?

Při navrhování swifitche byla bezpečnost jednou z priorit a rozhodně jsme ji nezanedbali. Hlavní bezpečnostní prvky jsou na vstupu z rozvodné sítě. Je zde pojistka proti nadměrnému odběru (zkratu), pojistka proti přepětí a teplotní pojistka, která vypne napájení při překročení teploty 100°C. Další pojistné mechanismy by měl obsahovat přímo zdroj HLK-PM01, nechtěli jsme však spoléhat na jejich kvalitu.

### Chci to! Co potřebuji koupit?

**Kondenzátory**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/Capacitors_4.7uF.png" width="70">|4.7μF 0805|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/Free-shipping-0805-SMD-capacitor-4-7uf-50V-475Z-100PCS/32376068362.html?spm=2114.13010608.0.0.ztsIz3)|
|<img src="Images/Parts/Gray_BG_Parts/Capacitors_100nF.png" width="70">|100nF 0805|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/Free-shipping-0805-SMD-capacitor-100nf-0-1uf-50V-104Z-100PCS/32375582602.html?spm=2114.13010608.0.0.ztsIz3)|
|<img src="Images/Parts/Capacitors_10nF.png" width="70">|10nF 0805|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/Free-shipping-0805-SMD-capacitor-10nf-50V-103K-100PCS/32375924803.html?spm=2114.13010608.0.0.ztsIz3)|
|<img src="Images/Parts/Gray_BG_Parts/Capacitors_47uF.png" width="70">|47μF ⌀6.3x5mm|[<img src="Images/Shops/gray_farnell.png" width="35">](http://cz.farnell.com/multicomp/mcumr16v476m6-3x5/cap-alu-elec-47uf-16v-rad/dp/9452214?iscrfnonsku=true) [<img src="Images/Shops/gray_tme.png" width="30">](http://www.tme.eu/cz/details/umt1c470mdd/105c-tht-electrolytic-capacitors/nichicon/)|
|<img src="Images/Parts/Capacitors_47nF.png" width="70">|47nF X2|[<img src="Images/Shops/farnell.png" width="35">](http://cz.farnell.com/kemet/r463i24705001k/cap-film-pp-0-047uf-300vac-rad/dp/2446240?ost=R463I24705001K&searchView=table&iscrfnonsku=false) [<img src="Images/Shops/tme.png" width="30">](http://www.tme.eu/cz/details/r463i24705001k/x2y2-foil-polypropylene-capacitors/kemet/)|

**Odpory**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/Resistors_10k.png" width="80">|10kΩ 0805|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/100pcs-lot-SMD-Chip-Resistor-0805-10K-10K-ohm-5-Free-shippng/32382494431.html?spm=2114.13010608.0.0.nza8EJ)|
|<img src="Images/Parts/Gray_BG_Parts/Resistors_one_0805.png" width="80">|1.5kΩ 0805|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/New-100PCS-Lot-SMD-Resistance-0805-1K5-1-5K-5-1-8W-Chip-Resistors-Wholesale/32530331741.html?spm=2114.13010608.0.0.FKRHEz)|
|<img src="Images/Parts/Resistors_one_0805.png" width="80">|2.2kΩ 0805|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/New-100PCS-Lot-SMD-Resistance-0805-2K2-2-2K-5-1-8W-Chip-Resistors-Wholesale/32530124753.html?spm=2114.13010608.0.0.FKRHEz)|
|<img src="Images/Parts/Gray_BG_Parts/Resistors_one_0805.png" width="80">|47kΩ 0805|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/100pcs-lot-SMD-Chip-Resistor-0805-47K-47K-ohm-5-Free-shippng/32381859069.html?spm=2114.13010608.0.0.nza8EJ)|
|<img src="Images/Parts/Resistors_160R_1206.png" width="80">|160Ω 1206|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/Free-Shipping-100PCS-1206-160R-1206-160ohm-1-SMD-Resistor-160ohm/2043972079.html?spm=2114.13010608.0.0.iQHdt4)|
|<img src="Images/Parts/Gray_BG_Parts/S10K275.png" width="80">|S10K275|[<img src="Images/Shops/gray_farnell.png" width="35">](http://cz.farnell.com/epcos/b72210s0271k101/varistor-43-0j-275vac/dp/1004390?ost=B72210S0271K101&selectedCategoryId=&categoryNameResp=All%2BCategories&searchView=table&iscrfnonsku=false) [<img src="Images/Shops/gray_tme.png" width="30">](http://www.tme.eu/cz/details/siov-s10k275/tht-varistors/epcos/b72210s0271k101/)|

**Napájení a ovládací prvky**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/Fuse_Schurter.png" width="40">|SCHURTER MSF 250VAC 500mA|[<img src="Images/Shops/farnell.png" width="35">](http://cz.farnell.com/schurter/0034-6011/fuse-pcb-quick-blow-500ma/dp/1214681) [<img src="Images/Shops/tme.png" width="30">](http://www.tme.eu/cz/details/0034.6011/fuses-tr5-fast/schurter/)|
|<img src="Images/Parts/Gray_BG_Parts/Fuse_Temperature.png" width="40">|PROFFUSE TZ-P100/2 100°C či podobná|[<img src="Images/Shops/gray_farnell.png" width="30">](http://cz.farnell.com/thermodisc/g4a01098c/fuse-thermal-98-c/dp/476584) [<img src="Images/Shops/gray_tme.png" width="30">](http://www.tme.eu/cz/details/tz-p100_2/thermal-fuses/proffuse/)|
|<img src="Images/Parts/HLK-PM01.png" width="80">|Hi-Link HLK-PM01 AC-DC 5V/3W|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/Free-Shipping-10pcs-lot-HLK-PM01-AC-DC-220V-to-5V-mini-power-supply-module-intelligent/32688093777.html?spm=2114.13010608.0.0.T6S4Y8)|
|<img src="Images/Parts/Gray_BG_Parts/Relay.png" width="50">|SRD-05VDC-SL-C relé<br>FINDER  36.11.9.005.4011|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/Free-shipping-SRD-5VDC-SL-C-5pins-SRD-05VDC-SL-C-Mini-Power-Relay-In-stock/1092738041.html?spm=2114.13010608.0.0.ztsIz3) [<img src="Images/Shops/gray_farnell.png" width="30">](http://cz.farnell.com/finder/36-11-9-005-4011/relay-spdt-250vac-10a/dp/2311438?ost=36.11.9.005.4011&selectedCategoryId=&categoryNameResp=All%2BCategories&searchView=table&iscrfnonsku=false) [<img src="Images/Shops/gray_tme.png" width="30">](http://www.tme.eu/cz/details/36.11.9.005.4001/miniature-electromagnetic-relays/finder/361190054011/)|

**Další SMD součástky**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/BC817-16.215.png" width="20">|BC817-16.215|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/100PCS-Lot-BC817-BC817-16-SOT-23-NPN-6C-0-1A-45V-general-purpose-transistor-NEW/32624683542.html?spm=2114.13010208.99999999.264.BYhv5u) [<img src="Images/Shops/farnell.png" width="35">](http://cz.farnell.com/nxp/bc817-16-215/transistor-npn-45v-0-5a-sot-23/dp/8734739) [<img src="Images/Shops/tme.png" width="30">](http://www.tme.eu/cz/details/bc817-16.215/npn-smd-transistors/nxp/)|
|<img src="Images/Parts/Gray_BG_Parts/BAS86.png" width="22">|BAS86|[<img src="Images/Shops/gray_farnell.png" width="35">](http://cz.farnell.com/nxp/bas86/diode-schottky-sod-80/dp/8734542) [<img src="Images/Shops/gray_tme.png" width="30">](http://www.tme.eu/cz/details/bas86.115/smd-schottky-diodes/nxp/)|
|<img src="Images/Parts/MCP1825T-3302E-DC.png" width="30">|MCP1825T-3302E/DC Regulátor Napětí|[<img src="Images/Shops/farnell.png" width="35">](http://cz.farnell.com/microchip/mcp1825t-3302e-dc/ic-ldo-3-3v-500ma-sot-223-5/dp/1578410) [<img src="Images/Shops/tme.png" width="30">](http://www.tme.eu/cz/details/mcp1825t-3302ed/ldo-unregulated-voltage-regulators/microchip-technology/mcp1825t-3302edc/)|
|<img src="Images/Parts/Gray_BG_Parts/FB1.png" width="18">|Feritová perla 600Ω 100MHz 0805|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/50pcs-SMD-bead-FB-0805-600R-100MHZ-600-600ohm-25-500mA-Ferrite/32637007661.html?spm=2114.13010608.0.0.ztsIz3) [<img src="Images/Shops/gray_farnell.png" width="30">](http://cz.farnell.com/murata/blm21ag601sn1d/ferrite-bead-0805-0-21ohm-0-6a/dp/1515622?MER=sy-me-pd-mi-alte) [<img src="Images/Shops/gray_tme.png" width="30">](http://www.tme.eu/cz/details/mmz2012r601a/ferrite-beads/tdk/)|
|<img src="Images/Parts/LED1.png" width="18">|Jakákoliv 0805 LED dioda|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/100pcs-Flashing-LEDs-SMD-0805-Red-Flashing-Diodes-Blinking-LED-Flash-0805-SMD-Diode-0805-smd/32366087497.html?spm=2114.13010608.0.0.FKRHEz)|

**Konektory**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/Header_1x2.png" width="30">|Oboustranný kolík 1x2 s roztečí 2.54mm |[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/10pcs-40-Pin-1x40-Single-Row-Male-2-54-Breakable-Pin-Header-Connector-Strip-for-Arduino/32641752713.html?spm=2114.13010608.0.0.U9AXxI)|
|<img src="Images/Parts/Gray_BG_Parts/Header_2x5.png" width="26">|Oboustranný kolík 2x5 s roztečí 2.54mm|[<img src="Images/Shops/gray_ali.png" width="30">](https://www.aliexpress.com/item/5-PCS-2-54mm-2-x-40-Pin-Male-Double-Row-Pin-Header-Strip/32216818428.html?spm=2114.01010208.3.2.5nQ4Vd)|
|<img src="Images/Parts/Terminal_2P_and_3P.png" width="100">|Svorkovnice 2P a 3P, s roztečí 5.08mm a kulatým vývodem|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/wholesale?catId=0&initiative_id=SB_20170202034250&SearchText=terminal+5.08mm)|

**Zbytek**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/ESP8266_12.png" width="75">|ESP8266-12(E/F/S)|[<img src="Images/Shops/ali.png" width="30">](https://www.aliexpress.com/item/1PCS-ESP-12F-ESP-12E-upgrade-ESP8266-Remote-Serial-Port-WIFI-Wireless-Module-ESP8266/32714088769.html?spm=2114.13010608.0.0.4TnTET)|
|<img src="Images/Parts/Gray_BG_Parts/PCB.png" width="300">|Plošné spoje|[<img src="Images/Shops/gray_seeedstudio.png" width="30">](https://www.seeedstudio.com/fusion_pcb.html)|

Většinu lze zakoupit na AliExpressu nebo eBay a to za ceny, že ani není třeba to komentovat. Některé součástky je lepší nebo i výhodnější zakoupit od místních prodejců elektroniky.

Většina odkazů na jednotlivé díly v tabulkách výše je prověřená, nicméně neposkytujeme žádné záruky.

Pro nás Čechy a popř. Slováky, bude dobrým zdrojem většiny dílů, které nelze zakoupit přes Alíka obchod TME.eu, poštovné je také za hubičku.

Pro ty ostatní je zde ještě Farnell

# SeeedStudio Fusion PCB

### Jak objednat plošné spoje

Stáhněte si ZIP soubor obsahující soubory "Gerber" a celý jej nahrajte do objednávacího procesu na SeeedStudio Fusion PCB webu a postupujte podle instrukcí na webu a níže.

Připravili jsme pro vás snímky obrazovky z objednávkového procesu, když jsme plošné spoje objednávali naposledy a tak můžete snadno vyplnit stejné hodnoty. Vyberte si počet plošných spojů a mějte na paměti, že 1ks jsou dva. Za stejnou cenu se nám podařilo na jednu desku dostat dvě.

<img src="Images/SeeedStudio_Order.png" width="900">

Náhled na obsah Gerber souborů:

<img src="Images/SeeedStudio_Order_Gerber.png" width="900">

# Po sestavení

### Hotovo! Co dál?

Po sestavení přichází na řadu nahrání softwaru. Můžete buďto použít běžný USB2UART programátor nebo vyrobit vlastní úpravou NodeMCU. Je to levná varianta, efektivní a ještě získáte jeden modul ESP8266 na výrobu swifitche.

Obrázek níže přesně ukazuje čeho potřebujete dosáhnout, přesto pár kroků jak na to.

- Pomocí horkovzdušné pistole odpájejte modul ESP8266. Opatrně ať si nepoškodíte ani ESPčko ani NodeMCU.
- Připájejte barevné vodiče dle obrázku
- Vložte vodiče do konektoru 2x5 s roztečí 2.54mm
- Připojte swifitch a nahrajte software.

Připravili jsme pro vás náš software aby byl začátek co nejsnazší, pokračujte do jeho [repozitáře](https://github.com/ArnieX/swifitch-software).

<img src="Images/Swifitch_NodeMCU.png" width="700">

**⚡ PŘI FLASHOVÁNÍ SOFTWARU NEPŘIPOJUJTE SWIFITCH K ROZVODNÉ SÍTI ⚡**

Mělo by to být bezpečné, přesto to nedoporučujeme.

# Software

### Náš základní software 

Pokud jste se rozhodli pro náš software tak postupujte dle README v jeho [repozitáři](https://github.com/ArnieX/swifitch-software).

### Vlastní software

Pokud se rozhodnete napsat vlastní software, jen do toho, zde jen pár faktů, které potřebujete znát.

- Relé je ovládané přes pin D1 nebo GPIO5
- Vestavěná LED dioda se spíná přes pin D6 nebo GPIO12

# Krabička

### Vytištěná na 3D tiskárně

Pokud máte přístup ke 3D tiskárně, můžete si vytisknout naší 3D krabičku.

**Nevyzkoušeno, klidně můžete být první.**

<img src="Images/swifitch_box_transp.png" width="500">

Doporučujeme tisk z ABS, neboť je to bezpečnější materiál pro zařízení napajené z rozvodné sítě.

**NEPOUŽÍVEJTE K TISKU VODIVÉ MATERIÁLY NEBO TY S PŘÍMĚSÍ KOVŮ**

### Kupovaná krabička

Swifitch byl navržen primárně pro umístění do krabičky běžně [dostupné](http://www.tme.eu/cz/details/cp-z-24_tr/univerzalni-krabicky/combiplast/), je však nutné jí drobně upravit, postačí vrtačka a vrtáky na kov.

# Návod na pájení

### Zadní strana

Začněte na zadní straně postupně s SMD součástkami.

**Kondenzátory**

|Pozice|Součástka|
|---|---|
|C1|4.7μF|
|C3|4.7μF|
|C5|4.7μF|
|C6|4.7μF|
|C4|100nF|
|C7|100nF|
|C8|10nF|

**Odpory**

|Pozice|Součástka|
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

**Zbytek**

|Pozice|Součástka|
|---|---|
|FB1|Feritová perla 600Ω 100MHz|
|D1|BAS86|
|T1|BC817|
|WiFi1|ESP8266-12(E/F/S)|

### Přední strana

Přední strana obsahuje většinově THT součástky, proto začněte s SMD součástkami, které by bylo obtížné pájet později.

**SMD**

|Pozice|Součástka|
|---|---|
|R1|470Ω < Rled < 2kΩ (záleží na LED1)|
|LED1|Barva dle výběru|
|V1|Regulátor Napětí|

**THT**

|Pozice|Součástka|
|---|---|
|DC1|HLK-PM01|
|F2|100°C tepelná pojistka|
|R2|S10K275|
|F1|MSF250/0.5A|
|C10|47nF|
|C2|47μF|
|C9|47μF|
|SB1|Pájecí propojka pro volbu D5 nebo výstupu 5V|
|JP1|1x2 kolík|
|JP2|1x2 kolík|
|J3|2x5 kolík|
|RE1|Relé|
|J1|2P svorkovnice|
|J2|3P svorkovnice|

**🎉 HOTOVO 🎉**

# Zásluhy

- návrhy plošných spojů, nápady ohledně elektroniky, výběr vhodných součástek - Miroslav Batěk
- SW, Git Repo, grafika, 3D krabička - Martin Doubek

# Co dál?

Pokud se vám swifitch zalíbil a chcete ve výbavě chytré domácnosti pokračovat, doporučujeme tyto další projekty.

- [ESP8266 stmívací modul pro LED pásky od uživatele tjclement](https://github.com/tjclement/esp-dimmer-hardware)

Popřípadě tyto IoT platformy, nebo enablery.

- [Homebridge - vlastní HomeKit server](https://github.com/nfarina/homebridge)
	- [Homebridge MQTT plugin](https://github.com/cflurin/homebridge-mqtt)
- [Blynk - plaforma a aplikace pro IoT - lze použít se Swifitchem](https://github.com/blynkkk/blynk-server)

# Fotografie

<img src="Images/Photo_Front.jpg" width="400"> <img src="Images/Photo_Back.jpg" width="400">
<img src="Images/Photo_Kaleidoscope_1.jpg" width="400"> <img src="Images/Photo_Kaleidoscope_2.jpg" width="400">

