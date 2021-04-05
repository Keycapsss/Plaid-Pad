# Build guide for the Plaid-Pad

### Diodes 1N4148 (D1-D16)

Diodes are __polarized__. The black line on the diode (cathode) must face the squared solder pad.
The 1N4148 diodes look similar as Zener diodes - so make sure that you do not confuse both diodes.

You can use some tape, as show in the image, to hold the diodes in place and solder all in one pass.

<img src="img/plaid-pad-1N4148-diodes-1.jpg" width=600>

### Zener diodes (D49, D50)

The diodes are __polarized__ where the black line on the diode (cathode) must face the squared solder pad.
The 1N4148 diodes look similar as Zener diodes - so make sure that you do not confuse both diodes.

<img src="img/plaid-pad-zener-diodes-1.jpg" width=600>

### Resettable fuse (F1)

Attach and solder the fuse to `F1`. After soldering, bend the fuse like in the image.

<img src="img/plaid-pad-resettable-fuse-1.jpg" width=600>

### Electrolytic capacitor (C3)

The Electrolytic capacitor is __polarized__. The short leg is cathode which needs to be attached to the square pad on the PCB.

<img src="img/plaid-pad-electrolytic-capacitor-1.jpg" width=600>

### Resistors 1.5k Ohm (R1, R7)

Attach the resistors with following colors from left to right:

- brown, green, black, brown, brown

<img src="img/plaid-pad-resistors-1.5k-1.jpg" width=600> <img src="img/plaid-pad-resistors-1.5k-2.jpg" width=600>

### Resistors 75 Ohm (R2, R3)

Attach the resistors with following colors from left to right:

- purple, green, black, gold, brown

<img src="img/plaid-pad-resistors-75-1.jpg" width=600>

### Resistors 10k Ohm (R4)

Attach the resistors with following colors from left to right:

- brown, black, black, red, brown

<img src="img/plaid-pad-resistors-10k-1.jpg" width=600>

### Resistors 5.1k Ohm (R8, R9)

Attach the resistors with following colors from left to right:

- green, brown, black, brown, brown

<img src="img/plaid-pad-resistors-5.1k-1.jpg" width=600>

### USB-C connector (J1)

Double check that there are no short cuts between the solder pads.
A magnifier is handy for this task.

<img src="img/plaid-pad-usb-c-connector-1.jpg" width=600>

### Optional: LED (LED1)

The LEDs are __polarized__. The short leg is the cathode which needs to be attached to the square pad on the PCB

`LED1` indicates that the Plaid-Pad is powered and constantly on.

If you don't want a constant red light on your Plaid-Pad, don't solder this LED.

<img src="img/plaid-pad-leds-1.jpg" width=600>

### Crystal (Y1)

<img src="img/plaid-pad-crystal-1.jpg" width=600>

### Capacitors 22pF (C1, C2)

They have a small pitch (2.5mm).

<img src="img/plaid-pad-capacitors-22pf-1.jpg" width=600>

### Capacitors 0.1uF (C4, C5)

These have a larger pitch of 5mm.

<img src="img/plaid-pad-capacitors-0.1uf-1.jpg" width=600>

### IC socket U1

The IC socket is __polarized__. Check the notch on the silk and the IC Socket.

<img src="img/plaid-pad-ic-socket-1.jpg" width=600>

### Tactile switch (SW50/RESET, SW51/BOOT)

<img src="img/plaid-pad-tactile-switch-1.jpg" width=600>

### ATMEGA328p chip

The ATMEGA328 has to be attached in a __specific direction__. Check the notch on the chip and IC Socket - they need to match. Here, the notch faces the crystal at `Y1`.

<img src="img/plaid-pad-atmega329p-1.jpg" width=600>

### Oled display (SSD1306)

Add isolation tape to the back of the oled, to protect the components for shorts.

<img src="img/plaid-pad-oled-ssd1306-1.jpg" width=600>

Place the oled like on the image and solder it from the bottom to the PCB.

<img src="img/plaid-pad-oled-ssd1306-2.jpg" width=600>

## Check list before connecting USB

- No short cuts on the USB-C connector pads
- Direction of polarized and directional components is correct (ATMEGA328p, diode, resettable fuse, electrolytic capacitor, LEDs)
- Resistors with correct values are attached to the target locations

## Test 
_Bootloader and Firmware (VIA keymap) are already on the ATmega328P chip.  
Everything should work after soldering._

Connect the Plaid-Pad to your computer and open the [QMK-Test-Site](https://config.qmk.fm/#/test).

Check whether all switches will work. In order to do so, short the solder pads with tweezers.

<img src="img/plaid-pad-tweezers-switch-test-1.jpg" width=600>

## Optional Mill-Max Holtites

The Plaid-Pad supports [Mill-Max 0305 Holtites](https://keycapsss.com/keyboard-parts/parts/73/mill-max-0305-holtite-for-switches-hotswap-sockets?number=KC10042_50x). If these are installed, you can Hotswap the switches (change without soldering).

Put the holtite in the related holes.


<img src="img/plaid-pad-mill-max-0305-holtite-2.jpg" width=600>

Install all switches to the top plate. Check that all switch pins are straight and press the top plate with switches on the PCB with the holtites.

Pay attention that no solder flows into the holtite.

<img src="img/plaid-pad-mill-max-0305-holtite-3.jpg" width=600>

## Case assembly

__Before you solder the switches,__ attach the 4x 5mm spacer to the pcb with the M2x4mm screws.  
__Do not solder the rotary encoder yet.__

<img src="img/plaid-pad-top-plate-1.jpg" width=600> <img src="img/plaid-pad-top-plate-2.jpg" width=600>


Attach all switches to the top plate and place __(not solder)__ the desired amount of the rotary encoder on the pcb ([more information about rotary encoder placement](https://github.com/BenRoe/Plaid-Pad#keymap)).

<img src="img/plaid-pad-top-plate-3.jpg" width=600>

This way the rotary encoder have room to move and fit perfect into the top plate cutout.

### Rotary encoder and Choc (low profile) switches (skip if you use MX switches)

If you use Choc (low profile) switches, you have to bend the 5 pins of the rotary encoder with a pliers, to fit into the top plate.

<img src="img/rotary-encoder-pin-adjustment-1.jpg" width=600>

---

Put the top plate with the switches on the front side of the pcb.  
Solder the switches and rotary encoder from the bottom side.  
__Ensure that there is no gap between the switch bottom and the pcb. Same for the encoder.__ 

<img src="img/plaid-pad-top-plate-4.jpg" width=600>

Screw the 4x 5mm spacer at the upper part of the bottom plate. Use the 12mm screws for it. 

<img src="img/plaid-pad-bottom-plate-1.jpg" width=600>

Optional: Put the dampening foam on the bottom plate.

<img src="img/plaid-pad-bottom-plate-2.jpg" width=600>

Put the assembled top plate with the switches and pcb on the bottom plate.  

Screw the 4x 10mm spacer for the guard plate on 12mm prominent screws from below.
Remove the protection film on both sides from the acrylic guard plate.
Fix the acrylic guard plate and the pcb with the 4mm screws.

<img src="img/plaid-pad-final-1.jpg" width=600>

Put the rubber feeds on the back of the Plaid-Pad.

__The assembly is done.__
  
You can change the keymap with [VIA](../README.md#qmk-with-via-support-no-rotary-encoder-support)(**no** rotary encoder support), [VIAL](https://get.vial.today)(with rotary encoder support), 
or change the [QMK keymap](https://github.com/BenRoe/Plaid-Pad#qmk-default-keymap) file and reflash the firmware.
