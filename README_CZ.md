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

**⛔  Pozor, swifitch přesto, že umožňuje aktivaci výstupu 5V neumožňuje vstup 5V na žádném dostupném pinu, pokud byste připojili 5V na některý pin, zničíte modul ESP8266.**

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
|<img src="Images/Parts/Capacitors_4.7uF.png" width="70">|4.7μF 0805|[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/capacitors_4.7uf_0805)|
|<img src="Images/Parts/Gray_BG_Parts/Capacitors_100nF.png" width="70">|100nF 0805|[<img src="Images/Shops/gray_ali.png" width="30">](http://swifitch.cz/capacitors_100nf_0805)|
|<img src="Images/Parts/Capacitors_10nF.png" width="70">|10nF 0805|[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/capacitors_10nf_0805)|
|<img src="Images/Parts/Gray_BG_Parts/Capacitors_47uF.png" width="70">|47μF ⌀6.3x5mm|[<img src="Images/Shops/gray_farnell.png" width="35">](http://swifitch.cz/cz/capacitors_47uf_6.3x5_farnell) [<img src="Images/Shops/gray_tme.png" width="30">](http://swifitch.cz/cz/capacitors_47uf_6.3x5_tme)|
|<img src="Images/Parts/Capacitors_47nF.png" width="70">|47nF X2|[<img src="Images/Shops/farnell.png" width="35">](http://swifitch.cz/cz/capacitors_47nf_farnell) [<img src="Images/Shops/tme.png" width="30">](http://swifitch.cz/cz/capacitors_47nf_tme)|

**Odpory**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/Resistors_10k.png" width="80">|10kΩ 0805|[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/resistors_10k_0805)|
|<img src="Images/Parts/Gray_BG_Parts/Resistors_one_0805.png" width="80">|1.5kΩ 0805|[<img src="Images/Shops/gray_ali.png" width="30">](http://swifitch.cz/resistors_1.5k_0805)|
|<img src="Images/Parts/Resistors_one_0805.png" width="80">|2.2kΩ 0805|[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/resistors_2.2k_0805)|
|<img src="Images/Parts/Gray_BG_Parts/Resistors_one_0805.png" width="80">|47kΩ 0805|[<img src="Images/Shops/gray_ali.png" width="30">](http://swifitch.cz/resistors_47k_0805)|
|<img src="Images/Parts/Resistors_160R_1206.png" width="80">|160Ω 1206|[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/resistors_160R_1206)|
|<img src="Images/Parts/Gray_BG_Parts/S10K275.png" width="80">|S10K275|[<img src="Images/Shops/gray_farnell.png" width="35">](http://swifitch.cz/cz/resistors_S10K275_farnell) [<img src="Images/Shops/gray_tme.png" width="30">](http://swifitch.cz/cz/resistors_S10K275_tme)|

**Napájení a ovládací prvky**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/Fuse_Schurter.png" width="40">|SCHURTER MSF 250VAC 500mA|[<img src="Images/Shops/farnell.png" width="35">](http://swifitch.cz/cz/power_schurter_fuse_farnell) [<img src="Images/Shops/tme.png" width="30">](http://swifitch.cz/cz/power_schurter_fuse_tme)|
|<img src="Images/Parts/Gray_BG_Parts/Fuse_Temperature.png" width="40">|PROFFUSE TZ-P100/2 100°C nebo podobná|[<img src="Images/Shops/gray_farnell.png" width="30">](http://swifitch.cz/cz/power_temperature_fuse_farnell) [<img src="Images/Shops/gray_tme.png" width="30">](http://swifitch.cz/cz/power_temperature_fuse_tme)|
|<img src="Images/Parts/HLK-PM01.png" width="80">|Hi-Link HLK-PM01 AC-DC 5V/3W|[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/power_AC_DC)|
|<img src="Images/Parts/Gray_BG_Parts/Relay.png" width="50">|SRD-05VDC-SL-C relé<br>FINDER  36.11.9.005.4011|[<img src="Images/Shops/gray_ali.png" width="30">](http://swifitch.cz/power_relay_ali) [<img src="Images/Shops/gray_farnell.png" width="30">](http://swifitch.cz/cz/power_relay_farnell) [<img src="Images/Shops/gray_tme.png" width="30">](http://swifitch.cz/cz/power_relay_tme)|

**Další SMD součástky**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/BC817-16.215.png" width="20">|BC817-16.215|[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/smd_bc817_ali) [<img src="Images/Shops/farnell.png" width="35">](http://swifitch.cz/cz/smd_bc817_farnell) [<img src="Images/Shops/tme.png" width="30">](http://swifitch.cz/cz/smd_bc817_tme)|
|<img src="Images/Parts/Gray_BG_Parts/BAS86.png" width="22">|BAS86|[<img src="Images/Shops/gray_farnell.png" width="35">](http://swifitch.cz/cz/smd_bas86_farnell) [<img src="Images/Shops/gray_tme.png" width="30">](http://swifitch.cz/cz/smd_bas86_tme)|
|<img src="Images/Parts/MCP1825T-3302E-DC.png" width="30">|MCP1825T-3302E/DC Regulátor Napětí|[<img src="Images/Shops/farnell.png" width="35">](http://swifitch.cz/cz/smd_MCP1825T_farnell) [<img src="Images/Shops/tme.png" width="30">](http://swifitch.cz/cz/smd_MCP1825T_tme)|
|<img src="Images/Parts/Gray_BG_Parts/FB1.png" width="18">|Feritová perla 600Ω 100MHz 0805|[<img src="Images/Shops/gray_ali.png" width="30">](http://swifitch.cz/smd_ferritebead_ali) [<img src="Images/Shops/gray_farnell.png" width="30">](http://swifitch.cz/cz/smd_ferritebead_farnell) [<img src="Images/Shops/gray_tme.png" width="30">](http://swifitch.cz/cz/smd_ferritebead_tme)|
|<img src="Images/Parts/LED1.png" width="18">|Libovolná 0805 LED dioda|[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/smd_led_diode)|

**Konektory**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/Header_1x2.png" width="30">|Oboustranný kolík 1x2 s roztečí 2.54mm |[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/connector_headers_1x2)|
|<img src="Images/Parts/Gray_BG_Parts/Header_2x5.png" width="26">|Oboustranný kolík 2x5 s roztečí 2.54mm|[<img src="Images/Shops/gray_ali.png" width="30">](http://swifitch.cz/connector_headers_2x5)|
|<img src="Images/Parts/Terminal_2P_and_3P.png" width="100">|Svorkovnice 2P a 3P, s roztečí 5.08mm a kulatým vývodem|[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/connector_terminal)|

**Zbytek**

|Náhled|Součástka|Koupit|
|---|---|---|
|<img src="Images/Parts/ESP8266_12.png" width="75">|ESP8266-12(E/F/S)|[<img src="Images/Shops/ali.png" width="30">](http://swifitch.cz/therest_esp8266)|
|<img src="Images/Parts/Gray_BG_Parts/PCB.png" width="300">|Plošné spoje|[<img src="Images/Shops/gray_seeedstudio.png" width="30">](http://swifitch.cz/therest_pcb)|

Většinu lze zakoupit na AliExpressu nebo eBay a to za ceny, že ani není třeba to komentovat. Některé součástky je lepší nebo i výhodnější zakoupit od místních prodejců elektroniky.

Většina odkazů na jednotlivé díly v tabulkách výše je prověřená, nicméně neposkytujeme žádné záruky.

Pro nás Čechy a popř. Slováky, bude dobrým zdrojem většiny dílů, které nelze zakoupit přes Alíka obchod TME.eu, poštovné je také za hubičku.

Pro ty ostatní je zde ještě Farnell

# SeeedStudio Fusion PCB

### Jak objednat plošné spoje

Stáhněte si ZIP soubor obsahující soubory "Gerber" a celý jej nahrajte do objednávacího procesu na [SeeedStudio Fusion PCB webu](http://swifitch.cz/therest_pcb) a postupujte podle instrukcí na webu a níže.

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

Připravili jsme pro vás náš software aby byl začátek co nejsnazší, pokračujte do jeho [repozitáře](http://swifitch.cz/software).

<img src="Images/Swifitch_NodeMCU.png" width="700">

**⚡ PŘI FLASHOVÁNÍ SOFTWARU NEPŘIPOJUJTE SWIFITCH K ROZVODNÉ SÍTI ⚡**

Mělo by to být bezpečné, přesto to nedoporučujeme.

# Software

### Náš základní software 

Pokud jste se rozhodli pro náš software tak postupujte dle README v jeho [repozitáři](http://swifitch.cz/software).

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

Swifitch byl navržen primárně pro umístění do krabičky běžně [dostupné](http://swifitch.cz/cz/enclosure), je však nutné jí drobně upravit, postačí vrtačka a vrtáky na kov.

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
<img src="Images/Photo_Bottom_5pcs.jpg">