# tm1637-fpga
4-Digit 7-Segment Display an FPGA

Die "Bit-Banging-Lösung" ist entstanden durch Mitschneiden einer Arduino-Beispiel-Kommunikation (nachgehalten mit [Logic-Analyser](https://www.saleae.com/de) und Stift + Zettel).

Die VHDL-Funktion "int_to_seg7" hat die Zahl 2017 hartkodiert und ist somit nicht als Parameter "nach außen" verfügbar. 

Todo (... dahingehender Versuch macht Probleme mit wertwillkürlicher Anzeige !!! Problem: voneinander (un)abhängige Clocks)

![alt text](https://i.ebayimg.com/images/g/qf8AAOSw301aUlaS/s-l400.jpg "TM1637")
