# tm1637-fpga
4-Digit 7-Segment Display for FPGAs

Modul setzt funktionsreduzierte Version von I2C ein (Kommunikation erfolgt ohne I2C-Busteilnehmeradresse).

Diese "Bit-Banging-Lösung" ist entstanden durch Mitschneiden einer Arduino Beispielkommunikation (nachgehalten mit [Logic-Analyser](https://www.saleae.com/de) und Stift & Zettel) und Vergleich mit dem Datenblatt.

<!--Todo (... dahingehende Änderungsversuche machen Probleme mit wertwillkürlicher Anzeige !!! Problem: voneinander (un)abhängige Clocks ... Hardwarequarz hierbei: **25 MHz**)-->

---

1. Version: **tm1637_standalone.vhd** - Display of **2017** hard coded

2. Version: **tm1637_external_connect.vhd** - Connection to "outside world" implemented ... thanks go to Igor K. !!! 

---

![alt text](https://i.ebayimg.com/images/g/qf8AAOSw301aUlaS/s-l400.jpg "TM1637")
