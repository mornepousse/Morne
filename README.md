# Jorne

Corne with an extra key

## Downloads

Version 2.0 has been already assembled and checked, everything works fine.

* [jorne-classic-2.0-gerbers.zip](https://github.com/joric/crkbd/raw/jorne/corne-classic/pcb/jorne-classic-2.0-gerbers.zip)

![](images/jorne-classic-2.0.png)

**WARNING** no mounting holes and ground zones in this revision (lost in conversion)!

There are also two **UNTESTED** revisions with an extra key, use at your own risk:

* [jorne-classic-2.1-gerbers.zip](https://github.com/joric/crkbd/raw/jorne/corne-classic/pcb/jorne-classic-2.1-gerbers.zip) (classic version, with mounting holes and ground planes)

![](images/jorne-classic-2.1.png)

* [jorne-cherry-2.1-gerbers.zip](https://github.com/joric/crkbd/raw/jorne-cherry/corne-cherry/pcb/jorne-cherry-2.1-gerbers.zip) (hotswap version, see [jorne-cherry](https://github.com/joric/crkbd/tree/jorne-cherry) branch)

![](images/jorne-cherry-2.1.png)

## Firmware

Compatible with [stock Corne firmware](https://github.com/qmk/qmk_firmware/tree/master/keyboards/crkbd). The extra key can be snapped off. [Bluetooth firmware version](https://github.com/joric/nrfmicro/wiki/Corne-BLE) is in progress.

## PCB manufacturers

I recommend [JLCPCB.com](https://jlcpcb.com). New users gets $8 discount, so 5 black matte PCBs cost $9.88 total, including shipping.

## Modification

In order to make your own Corne clone, you need to do the following:

* Fix "find segment with an endpoint" error messages on Alt+3 (see https://github.com/foostan/crkbd/pull/21)
* Fix the schematic to your taste (add an extra key to the free row, add an extra LED to the end of the strip)
* Press Ctrl+Q to update the PCB (uncheck the "Delete extra footprints" setting)
* Fix the 1.75u footprint for the autorouting (I moved bottom pads a little bit apart)
* Export "Specctra DSN" file, run Freerouting and autoroute the board, import Specctra session file
* Use "Create Corner" for the Zone Outlines, move corners to match the new outline (they autoupdate)
* Plot with "Use Protel filename extensions", generate drill files with "PTH and NPTH in a single file"

Note I did not reroute the whole board, just autorouted a few new traces and it worked.

## Pictures

![](corne-classic/pcb/front.png)

More pictures: https://imgur.com/a/T2GXaLw

## Video

[![](http://img.youtube.com/vi/JKPftgYVeUQ/0.jpg)](https://youtu.be/JKPftgYVeUQ)

## References

* https://github.com/foostan/crkbd
* https://github.com/joric/nrfmicro/wiki/Corne-BLE
