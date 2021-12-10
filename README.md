# Plaid-Pad

<img src="https://i.imgur.com/KHPId3G.jpg" width="400">

A 4x4 numpad/macro pad with only through hole components. It supports up to 4 rotary encoder. The positions for the encoder are interchangeable with keyboard switches.  

---

- [**Build guide**](./buildguide_en.md)
- [QMK Firmware](#qmk-firmware)
- [Bootloader](#bootloader)
- [Changelog](#changelog)
- [3D printing parts](./3d-print) (simple case)
- [Laser cut drawings](./lasercut) (guard plate, dampening foam)

---

## Keymap

<img src="https://i.imgur.com/V82cMqq.png" width="400">

Below you can see the possible positions for the 4 rotary encoder (Rev1 only 2).  
*If you place a encoder in the top left corner (E1), you can't use another encoder in the lower right corner.*

```text
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

- Encoder E1 performs a tap on KC_F17 and KC_F18
- Encoder E2 performs a tap on KC_F19 and KC_F20
- Encoder E3 performs a tap on KC_F21 and KC_F22
- Encoder E4 performs a tap on KC_F23 and KC_F24

The F17-F24 keys are intended to be customized via [Karabiner-Elements](https://github.com/pqrs-org/Karabiner-Elements) (OSX), or [AutoHotkey](https://github.com/Lexikos/AutoHotkey_L) (WIN).

It's a great companion to the Plaid keyboard by [hsgw](https://github.com/hsgw/) and heavily inspired by it.

- Keyboard Maintainer: BenRoe [Github](https://github.com/BenRoe) / [Twitter](https://twitter.com/keycapsss)
- Hardware Supported: ATmega328P with VUSB ([see Bootloader section](#Bootloader))
- Hardware Availability: [Keycapsss.com](https://keycapsss.com)

## QMK Firmware

_Bootloader ([USBaspLoader](https://github.com/baerwolf/USBaspLoader)) and Firmware ([via keymap](https://github.com/qmk/qmk_firmware/tree/master/keyboards/keycapsss/plaid_pad)) are already on the ATmega328P chip._

### QMK with VIAL support (support for rotary encoder)

_Plaid-Pad Kit's Rev3 shipped with preflashed VIAL firmware._
_If you have a Rev2 Plaid-Pad, or want to re-flash the VIAL firmware again, you can find a compiled firmware file here ([Rev2]([keycapsss_plaid_pad_rev2_vial.hex](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/Keycapsss/Plaid-Pad/blob/master/keycapsss_plaid_pad_rev2_vial.hex)), [Rev3]([keycapsss_plaid_pad_rev3_vial.hex](https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/Keycapsss/Plaid-Pad/blob/master/keycapsss_plaid_pad_rev3_vial.hex)))

1. Flash pre-compiled firmware on the Plaid-Pad with [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases) ([How to enter Bootloader Mode](#enter-bootloader-mode-to-flash-a-new-firmware)).
2. Download the VIAL software from [here](https://get.vial.today)
3. Connect the Plaid-Pad to the computer with a USB cable (Reconnect after flashing the firmware)
4. Open VIAL and change the keymap to your needs (automatic save)

### QMK with VIA support (no rotary encoder support)

_Plaid-Pad Kit's shipped before 11.09.2020 are flashed with the QMK Default Keymap._
_To use VIA, compile the VIA Keymap with the following command and flash it with [QMK Toolbox](https://github.com/qmk/qmk_toolbox/releases) on the Plaid-Pad ([enter Bootloader Mode](#enter-bootloader-mode-to-flash-a-new-firmware))._

```bash
qmk compile -kb keycapsss/plaid_pad -km via
```

1. Download the VIA software from [here](https://github.com/the-via/releases/releases/latest)
2. Connect the Plaid-Pad to the computer with a USB cable
3. Open VIA, switch to the `CONFIGURE` tab and change the keymap to your needs (automatic save)

_The current VIA version can't change the rotary encoder function._

### QMK Default Keymap

Make example for this keyboard (after [setting up your build environment](https://docs.qmk.fm/#/getting_started_build_tools)):

```bash
make keycapsss/plaid_pad:default
```

or

```bash
qmk compile -kb keycapsss/plaid_pad -km default
```

Flashing example for this keyboard:

```bash
make keycapsss/plaid_pad:default:flash
```

or

```bash
qmk flash -kb keycapsss/plaid_pad -km default
```

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with the [Complete Newbees Guide](https://docs.qmk.fm/#/syllabus).

You can find the rotary encoder code [here](https://github.com/qmk/qmk_firmware/blob/95bbd799a4f86dac37fdf2354e008d2fed7f6660/keyboards/keycapsss/plaid_pad/keymaps/via/keymap.c#L71).

## Bootloader

- same `usbasploader` as used for Plaid ([Instructions](https://github.com/hsgw/plaid/blob/master/doc/en/bootloader.md), [Repository](https://github.com/hsgw/USBaspLoader/tree/plaid))

### Enter Bootloader Mode (to flash a new firmware)

- Plug in the USB cable
- Push and hold RESET switch
- Push and hold BOOT switch
- Release RESET switch
- Release BOOT switch

alternative method:

- Unplug the USB cable
- Hold down the BOOT switch
- Plug in the USB cable
- Release the BOOT switch

alternative method ([Bootmagic Lite](https://docs.qmk.fm/#/feature_bootmagic?id=bootmagic-lite)):

- Unplug the USB cable
- Hold down the most top left key
- Plug in the USB cable
- Release the most top left key

If you succeed to enter bootloader mode, you can see usbasp in device manager, or `*** USBAsp device connected` in [QMK Toolbox](https://github.com/qmk/qmk_toolbox).

## CHANGELOG

### Rev1

- Initial pcb design
- Optional up to 2 Rotary Encoder

### Rev2 (Rev1.1)

- Pcb's with the label Rev1.1 are Rev2 (fixed with the second ordered batch)
- Optional: up to 4 Rotary Encoder
- Support for 3pin switches with the new top plate
- Add a small PLAID-PAD text beneath the USB-C connector

### Rev2.1

- Bigger solder pads for the USB-C connector
- Support for Choc V2 switches _(issue that the keycap touch the mounting screw, if bottoming out)_
- Changed case mounting style _(spacer go through the pcb and screwed on the top and bottom plate)_

### Rev3

- Support for a SSD1306 oled display (I2C Pins C4/C5)
- Removed the 2 indicator LEDs (Pin C4/C5)
- Added a power indicator LED
- Changed case mounting style back to the previous style (spacer mounted between mid PCB and bottom plate) - fix ChocV2 issue from REV2.1
