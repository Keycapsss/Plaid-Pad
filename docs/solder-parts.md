# Build guide

### Diodes 1N4148 (D1-D16)

Diodes are __polarized__. The black line on the diode (cathode) must face the squared solder pad.
The 1N4148 diodes look similar as Zener diodes - so make sure that you do not confuse both diodes.

You can use some tape, as show in the image, to hold the diodes in place and solder all in one pass.

<img src="img/plaid-pad-1N4148-diodes-1.jpg" height=400>

### Zener diodes (D49, D50)

The diodes are __polarized__ where the black line on the diode (cathode) must face the squared solder pad.
The 1N4148 diodes look similar as Zener diodes - so make sure that you do not confuse both diodes.

<img src="img/plaid-pad-zener-diodes-1.jpg" height=400>

### Resettable fuse (F1)

Attach and solder the fuse to `F1`. After soldering, bend the fuse like in the image.

<img src="img/plaid-pad-resettable-fuse-1.jpg" height=400>

### Electrolytic capacitor (C3)

The Electrolytic capacitor is __polarized__. The short leg is cathode which needs to be attached to the square pad on the PCB.

<img src="img/plaid-pad-electrolytic-capacitor-1.jpg" height=400>

### Resistors 1.5k Ohm (R1, R7, R8)

Attach the resistors with following colors from left to right:

- brown, green, black, brown, brown

<img src="img/plaid-pad-resistors-1.5k-1.jpg" height=400>

### Resistors 75 Ohm (R2, R3)

Attach the resistors with following colors from left to right:

- purple, green, black, gold, brown

<img src="img/plaid-pad-resistors-75-1.jpg" height=400>

### Resistors 10k Ohm (R4)

Attach the resistors with following colors from left to right:

- brown, black, black, red, brown

<img src="img/plaid-pad-resistors-10k-1.jpg" height=400>

### Resistors 5.1k Ohm (R9, R10)

Attach the resistors with following colors from left to right:

- green, brown, black, brown, brown

<img src="img/plaid-pad-resistors-5.1k-1.jpg" height=400>

### USB-C connector (J1)

Double check that there are no short cuts between the solder pads.
A magnifier is handy for this task.

<img src="img/plaid-pad-usb-c-connector-1.jpg" height=400>

### LEDs (LED1, LED2)

The LEDs are __polarized__. The short leg is the cathode which needs to be attached to the square pad on the PCB

`LED1` indicates that the Plaid-Pad is powered and constantly on.
I prefer to solder the red LED on `LED1`, because the LED is less bright.

<img src="img/plaid-pad-leds-1.jpg" height=400>

### Crystal (Y1)

<img src="img/plaid-pad-crystal-1.jpg" height=400>

### Capacitors 22pF (C1, C2)

They have a small pitch (2.5mm).

<img src="img/plaid-pad-capacitors-22pf-1.jpg" height=400>

### Capacitors 0.1uF (C4, C5)

These have a larger pitch of 5mm.

<img src="img/plaid-pad-capacitors-0.1uf-1.jpg" height=400>

### IC socket U1

The IC socket is __polarized__. Check the notch on the silk and the IC Socket.

<img src="img/plaid-pad-ic-socket-1.jpg" height=400>

### Tactile switch (SW50/RESET, SW51/BOOT)

<img src="img/plaid-pad-tactile-switch-1.jpg" height=400>

### ATMEGA328p chip

The ATMEGA328 has to be attached in a __specific direction__. Check the notch on the chip and IC Socket - they need to match. Here, the notch faces the crystal at `Y1`.

<img src="img/plaid-pad-atmega329p-1.jpg" height=400>

## Check list before connecting USB

- No short cuts on the USB-C connector pads
- Direction of polarized and directional components is correct (ATMEGA328p, diode, resettable fuse, electrolytic capacitor, LEDs)
- Resistors with correct values are attached to the target locations
