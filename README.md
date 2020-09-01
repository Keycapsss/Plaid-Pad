# Plaid-Pad

<img src="https://i.imgur.com/Jovhxpr.jpg" width="400"> <img src="https://i.imgur.com/V82cMqq.png" width="400">

- [Build guide](/docs/solder-parts.md)
- [QMK Firmware](#qmk-firmware)
- [Bootloader](#bootloader)
- [3D printing parts](/3d-print) (simple case)
- [Laser cut drawings](/lasercut) (guard plate, dampening foam)

A 4x4 numpad with only through hole components.  
It's a great companion to the Plaid keyboard by [hsgw](https://github.com/hsgw/) and heavily inspired by it.

* Keyboard Maintainer: BenRoe [Github](https://github.com/BenRoe) / [Twitter](https://twitter.com/keycapsss)
* Hardware Supported: ATmega328P with VUSB ([see Bootloader section](#Bootloader))
* Hardware Availability: [Keycapsss.com](https://keycapsss.com)

## [QMK Firmware](https://github.com/qmk/qmk_firmware/tree/master/keyboards/keycapsss/plaid_pad)
_Bootloader and Firmware (default keymap) are already on the ATmega328P chip._

Make example for this keyboard (after setting up your build environment):

    make keycapsss/plaid_pad:default

Flashing example for this keyboard:

    make keycapsss/plaid_pad:default:flash

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

## Bootloader
- same `usbasploader` as used for Plaid ([Instructions](https://github.com/hsgw/plaid/blob/master/doc/en/bootloader.md), [Repository](https://github.com/hsgw/USBaspLoader/tree/plaid))

### Enter bootloader mode (to flash a new firmware)
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

## 3D printing parts

