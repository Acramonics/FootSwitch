FootSwitch
==========

![Board image](https://github.com/Acramonics/FootSwitch/blob/main/images/2d.png?raw=true)


This is a very small board to accommodate a standard 3PDT guitar pedal
footswitch and provide all wiring for true bypass:

- input (a stereo jack being used as a switch to short the ring to the
  sleeve when a mono plug is inserted)
- output (a mono jack)
- to/from the effects unit
- an (optional) LED
- power in
- power out
- an (optional) battery as an alternative power source.

It has been designed to have everything power-related on one side and
audio-related on the other.

The board has a solder jumper where the middle pad is shorted to `J`
(GND) or to `J/FS`. When shorted to `J`, only the jack switches the
power to the effects board on or off; when shorted to `J/FS`, both the
jack and the footswitch will switch off the power. (In other words,
the input jack plug must be inserted and the footswitch switched on in
order to power the effects.) If the effects take some time to become
active after powering on, then select `J`).

Molex KK254 style connectors are indicated, but not needed - you can
simpy solder wires to the holes in the board instead.

I prefer to mount the footswitch on the opposite side of the board
from the other components, but you can do whatever works for you!

KiCad
-----

To view/edit the KiCad files, you will need my ACRM symbol and
footprint libraries.

LED
---

If using the LED, you also need to add the `LED Res` resistor. The
value of this depends on the voltage drop of your LED (which will vary
with colour) and how bright you want it to be. 1K is a good starting
point for most LEDs.

Battery
-------

If you choose to use the optional battery power, then you need to add
`D2` - the anode location is indicated on the board rather than the
conventional indication of cathode although the `K` for the LED is
also the side where the `D2` cathode should be! This should be a
Schottky diode with at least a 9v rating and sufficient current to
power your effects board. Something like a 1N5819 or BAT86S will be
fine.

![Populated Board image](https://github.com/Acramonics/FootSwitch/blob/main/images/3D.png?raw=true)

