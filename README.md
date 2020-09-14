# Plaid-Pad

<img src="https://i.imgur.com/Jovhxpr.jpg" width="400"> <img src="https://i.imgur.com/V82cMqq.png" width="400">

A 4x4 numpad/macro pad with only through hole components. It supports up to 4 rotary encoder. The positions for the encoder are interchangeable with keyboard switches.  

---

- [**Build guide**](/docs/solder-parts.md)
- [QMK Firmware](#qmk-firmware)
- [Bootloader](#bootloader)
- [Changelog](#changelog)
- [3D printing parts](/3d-print) (simple case)
- [Laser cut drawings](/lasercut) (guard plate, dampening foam)

---

Below you can see the possible positions for the 4 rotary encoder (Rev1 only 2).  
*If you place a encoder in the top left corner (E1), you can't use another encoder in the lower right corner.*
```
Rev2                      Rev1
,-----------------------,   ,-----------------------,
|  E1 |  E2 |  E3 |  E4 |   |  E1 |     |     |  E2 |
|-----+-----+-----+-----|   |-----+-----+-----+-----|
|     |     |     |  E3 |   |     |     |     |     |
|-----+-----+-----+-----|   |-----+-----+-----+-----|
|     |     |     |  E2 |   |     |     |     |     |
|-----+-----+-----+-----|   |-----+-----+-----+-----|
|     |     |     |  E1 |   |     |     |     |     |
`-----------------------'   `-----------------------'
```  
It's a great companion to the Plaid keyboard by [hsgw](https://github.com/hsgw/) and heavily inspired by it.

* Keyboard Maintainer: BenRoe [Github](https://github.com/BenRoe) / [Twitter](https://twitter.com/keycapsss)
* Hardware Supported: ATmega328P with VUSB ([see Bootloader section](#Bootloader))
* Hardware Availability: [Keycapsss.com](https://keycapsss.com)

## QMK Firmware
_Bootloader and Firmware ([default keymap](https://github.com/qmk/qmk_firmware/tree/master/keyboards/keycapsss/plaid_pad)) are already on the ATmega328P chip._

Make example for this keyboard (after [setting up your build environment](https://docs.qmk.fm/#/getting_started_build_tools)):

    make keycapsss/plaid_pad:default
    // or
    qmk compile -kb keycapsss/plaid_pad -km default

Flashing example for this keyboard ():

    make keycapsss/plaid_pad:default:flash
    // or
    qmk flash -kb keycapsss/plaid_pad -km default

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

## Bootloader
- same `usbasploader` as used for Plaid ([Instructions](https://github.com/hsgw/plaid/blob/master/doc/en/bootloader.md), [Repository](https://github.com/hsgw/USBaspLoader/tree/plaid))

### Enter Bootloader Mode (to flash a new firmware)
- Plug in the USB cable
- Push and hold RESET switch
- Push and hold BOOT switch
- Release RESET switch
- Release BOOT switch

or an alternative method:
- Unplug the USB cable
- Hold down the BOOT switch
- Plug in the USB cable
- Release the BOOT switch

If you succeed to enter bootloader mode, you can see usbasp in device manager, or `*** USBAsp device connected` in [QMK Toolbox](https://github.com/qmk/qmk_toolbox).

## CHANGELOG

### Rev1
* Initial pcb design
* Optional up to 2 Rotary Encoder

### Rev2 (Rev1.1)

* Pcb's with the label Rev1.1 are Rev2 (fixed with the second ordered batch)
* Optional: up to 4 Rotary Encoder
* Support for 3pin switches with the new top plate 
* Add a small PLAID-PAD text beneath the USB-C connector