GM Interface Board

====

Design from the community from: [@vntarasov](https://github.com/vntarasov)

**THIS IS ALPHA QUALITY HARDWARE, NOT TESTED, NOR DESIGNED BY COMMA.AI, FOR RESEARCH PURPOSES ONLY. THIS IS NOT A PRODUCT.
YOU ARE RESPONSIBLE FOR COMPLYING WITH LOCAL LAWS AND REGULATIONS.
NO WARRANTY EXPRESSED OR IMPLIED.**

=====

Parts for case assembly (mcmaster part numbers):
- 92010A122, M3 12mm flat head
- 94180A331, M3 heat insert

PCB parts: digikey.csv

Connector pins:
- For data pins, Digikey part # SAM12735-ND
- For power & ground pins, Mouser part # 829-15304702

Assembly steps:
- Order PCB from Oshpark and populate yourself, or order a populated PCB from Macrofab
  Solder everything except for connector headers and power pins
- Flash the board with
  - Connect 5v, ground, data+, data- to USB host. Use external 5v power
  - Don't use 5v linear regulator for USB power, it will get fried
  - Pull high (to +3.3v net) BOOT testpoint, through 1k resistor, to put board into DFU
- Print case.stl and connector.stl, use ABS filament
- Install m3 heat insert into the case
- Drill holes in the connector housing for easier insertion of data pins, from 0.7mm to 0.75mm
- Cut 0.1" connector header SAM12735-ND to 12-pin and 16-pin sizes
- Cut one of the 829-15304702 short, bend the other one 90 degrees
- Insert shorter 829-15304702 (+12v) into connector housing
  - Put enough solder on the +12v testpoint of the PCB
  - Insert 0.1" headers into PCB, then solder the +12v pin to the PCB
  - Connector's plastic is going to melt, immobilizing the +12v pin is recommended
- Solder 0.1" headers to the PCB
- Insert 90-degrees bent 829-15304702 (ground) into connector housing, solder to PCB
- Bolt down connector housing to the case
