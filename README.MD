# tm1637-fpga
4-Stellen 7-Segment Anzeige für FPGA

Modul setzt "kastrierte" Version von I2C ein (Kommunikation erfolgt ohne I2C-Busteilnehmeradresse).

Die "Bit-Banging-Lösung" ist entstanden durch Mitschneiden einer Arduino-Beispiel-Kommunikation (nachgehalten mit [Logic-Analyser](https://www.saleae.com/de) und Stift + Zettel) und Vergleich mit dem Datenblatt.

Die VHDL-Funktion "int_to_seg7" hat die Zahl **2017** hartkodiert und ist somit nicht als Parameter "nach außen" verfügbar. 

Todo (... dahingehende Änderungsversuche machen Probleme mit wertwillkürlicher Anzeige !!! Problem: voneinander (un)abhängige Clocks ... Hardwarequarz hierbei: **25 MHz**)

![alt text](https://i.ebayimg.com/images/g/qf8AAOSw301aUlaS/s-l400.jpg "TM1637")
