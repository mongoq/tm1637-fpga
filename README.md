# tm1637-fpga
4-Digit 7-Segment Display for FPGAs

Modul setzt funktionsreduzierte Version von I2C ein (Kommunikation erfolgt ohne I2C-Busteilnehmeradresse).

Diese "Bit-Banging-Lösung" ist entstanden durch Mitschneiden einer Arduino Beispielkommunikation (nachgehalten mit [Logic-Analyser](https://www.saleae.com/de [Aliexpress]https://de.aliexpress.com/item/4000100256046.html?src=google&src=google&albch=shopping&acnt=494-037-6276&isdl=y&slnk=&plac=&mtctp=&albbt=Google_7_shopping&aff_platform=google&aff_short_key=UneMJZVf&&albagn=888888&albcp=9317151805&albag=93621837065&trgt=299423776478&crea=de4000100256046&netw=u&device=c&gclid=Cj0KCQiAv8PyBRDMARIsAFo4wK0ykRDvqmds9vIVbDNbugpxAgwLh0YYmbvtvSm6NlQfMS7bdW5ojFUaAuz0EALw_wcB&gclsrc=aw.ds) und Stift & Zettel) und Vergleich mit dem Datenblatt.

<!--Todo (... dahingehende Änderungsversuche machen Probleme mit wertwillkürlicher Anzeige !!! Problem: voneinander (un)abhängige Clocks ... Hardwarequarz hierbei: **25 MHz**)-->

---

1. Version: **tm1637_standalone.vhd** - Display of **2017** hard coded

2. Version: **tm1637_external_connect.vhd** - Connection to "outside world" implemented ... thanks go to Igor K. !!! 

---

![alt text](https://i.ebayimg.com/images/g/qf8AAOSw301aUlaS/s-l400.jpg "TM1637")
