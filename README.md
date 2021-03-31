# tm1637-fpga

4-Digit 7-Segment Display for FPGAs

Module uses functionally reduced Version of I2C (no bus identifier number)

This "bit-banging solution" was developed by sniffing on example communication with an Arduino board with a [Logic-Analyser](https://www.saleae.com/de), a pen and a piece of paper.

**For the most recent version have a look at: https://opencores.org/projects/tm1637**

<!--Modul setzt funktionsreduzierte Version von I2C ein (Kommunikation erfolgt ohne I2C-Busteilnehmeradresse).-->


<!-- Diese "Bit-Banging-Lösung" ist entstanden durch Mitschneiden einer Arduino Beispielkommunikation (nachgehalten mit [Logic-Analyser](https://www.saleae.com/de) und Stift & Zettel) und Vergleich mit dem Datenblatt.
-->

<!--Todo (... dahingehende Änderungsversuche machen Probleme mit wertwillkürlicher Anzeige !!! Problem: voneinander (un)abhängige Clocks ... Hardwarequarz hierbei: **25 MHz**)-->

---

![alt text](https://wiki.das-labor.org/images/thumb/b/b3/Workshop_ArduinoGR20.png/120px-Workshop_ArduinoGR20.png "Arduino Gruppe Ruhrgebiet")

Talk: [Arduino Nano RTC Clock (TM1637 & DS1307)](https://github.com/mongoq/tm1637-fpga/raw/master/Vortrag_-_Arduino_Real_Time_Clock_mit_7-Segment_Anzeige.pdf)

---

1. Version: **tm1637_standalone.vhd** - Display of **2017** hard coded

2. Version: **tm1637_external_connect.vhd** - Connection to "outside world" implemented ... thanks go to Igor K. !!! 

3. Version: **TODO: Add missing ":" segment** (see [Example Arduino Code](https://draeger-it.blog/arduino-lektion-26-4-digit-7-segment-display/?cn-reloaded=1#Quellcode-3))

---

![alt text](https://i.ebayimg.com/images/g/qf8AAOSw301aUlaS/s-l400.jpg "TM1637")
