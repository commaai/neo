Honda giraffe (Bosch ADAS)
====

Get your panda deeper into your:

- 2017+ Honda CR-V
- 2017+ Civic Hatchback
- 2018+ Accord

May fit some Japanese civics or other Hondas with Bosch hardware.

The switches
====

The 4 DIP switches control signals to the stock ADAS system

- 1 -- ADAS F-CAN-B <-> Car/Radar F-CAN-B

- 2 -- ADAS ACC Can <-> Radar's ACC Can

- 3 -- ADAS ACC Can <-> Car ACC Can (disconnect for proxy via panda)

- 4 -- IGN + 12V Merge (Use when constant 12v is unavailable via the DC jack or fake ethernet port)

The modes
====
The first three switches:

Stock - 111
OpenPilot w/ stock auto high-beam and stock acc/radar firmware - 110
OpenPilot w/ stock auto high-beam* and OP Longitudinal control (with modded/added radar) - 100
OpenPilot w/ stock ADAS camera completely disabled - 000

* Untested as of June 2018

The fourth switch:
Up - Use WITHOUT constant 12v power from the dc jack. DO NOT use with constant 12v connected
Down - Use with constant 12v power or to disable panda if using only ignition power. comma power makes this easy https://shop.comma.ai


Board by [@csouers](https://github.com/csouers) / Case by [@energee](https://github.com/energee)
