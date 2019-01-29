# tm1637-fpga
4-Stellen 7-Segment Anzeige für FPGA

Modul setzt "kastrierte" Version von I2C ein (Kommunikation erfolgt ohne I2C-Busteilnehmeradresse).

Diese "Bit-Banging-Lösung" ist entstanden durch Mitschneiden einer Arduino Beispielkommunikation (nachgehalten mit [Logic-Analyser](https://www.saleae.com/de) und Stift & Zettel) und Vergleich mit dem Datenblatt.

Die VHDL-Funktion "int_to_seg7" bei **tm1637_standalone.vhd** hat die Zahl **2017** hartkodiert und ist somit nicht als Parameter "nach außen" verfügbar. 

<!--Todo (... dahingehende Änderungsversuche machen Probleme mit wertwillkürlicher Anzeige !!! Problem: voneinander (un)abhängige Clocks ... Hardwarequarz hierbei: **25 MHz**)-->

---

1. Version: **tm1637_standalone.vhd**

2. Version: **tm1637_external_connect.vhd** - Verbindug "nach außen" implementiert. Dank an Igor K. !!! 
TODO: Ungetestet!

---

![alt text](https://i.ebayimg.com/images/g/qf8AAOSw301aUlaS/s-l400.jpg "TM1637")
