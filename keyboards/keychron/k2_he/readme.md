# Keychron K2 HE

![Keychron K2 HE](https://cdn.shopify.com/s/files/1/0059/0630/1017/files/K2-HE-1_d3ce1e1c-6562-4b1f-a857-ba2269478c99.jpg)

A customizable 84 keys TKL hall effect keyboard.

* Keyboard Maintainer: [Keychron](https://github.com/keychron)
* Hardware Supported: Keychron K2 HE
* Hardware Availability: [Keychron K2 HE QMK/VIA Wireless Custom Mechanical Keyboard](https://www.keychron.com/products/keychron-k2-he-wireless-magnetic-switch-keyboard)

## Option A: Build And Flash Firmware

Make example for this keyboard (after setting up your build environment):

    export PATH="$HOME/.local/share/qmk/bin:$PATH"

    # Stock keymaps
    make keychron/k2_he/ansi:keychron
    make keychron/k2_he/iso:keychron
    make keychron/k2_he/jis:keychron

    # Custom keymap implemented in this repo
    make keychron/k2_he/ansi:artylemon
    make keychron/k2_he/iso:artylemon

    # Equivalent QMK CLI commands
    qmk compile -kb keychron/k2_he/ansi -km artylemon
    qmk compile -kb keychron/k2_he/iso -km artylemon

Flashing example for this keyboard:

    make keychron/k2_he/ansi:keychron:flash
    make keychron/k2_he/iso:keychron:flash
    make keychron/k2_he/jis:keychron:flash

    # Flash custom keymap
    make keychron/k2_he/ansi:artylemon:flash
    make keychron/k2_he/iso:artylemon:flash

    # Equivalent QMK CLI commands
    qmk flash -kb keychron/k2_he/ansi -km artylemon
    qmk flash -kb keychron/k2_he/iso -km artylemon

### Custom keymap note (`artylemon`)

Implemented at:

- `keyboards/keychron/k2_he/ansi/keymaps/artylemon`
- `keyboards/keychron/k2_he/iso/keymaps/artylemon`

For ISO hardware, use the ISO target (`keychron/k2_he/iso:artylemon`) so Enter/Backslash keys map correctly.

Behavior highlights:

1. Mac/Win dual-base setup: Mac switch position uses a standard base layout, Win switch position uses a modified layout.
2. Space layer-tap on the Win base (`LT(FN2, KC_SPC)`), with a right-hand numpad cluster on `FN2` aligned to `U I O` / `J K L` / `M , .`.
3. Home row mods on the Win base (`A S D F` and `J K L ;`) with `TAPPING_TERM 200`.

**Bootloader Activation (K2 HE)**: Disconnect the USB cable, toggle mode switch to "Cable", hold down the *Esc* key, then reconnect the USB cable while still holding *Esc*. You can also use the reset button underneath the space bar.

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

## Option B: Use Keychron Launcher (no code required)

If you just want to remap keys, tune Hall Effect settings, or change lighting, you don't need to build firmware:

1. Open [Keychron Launcher](https://launcher.keychron.com/) in a Chromium-based browser such as Google Chrome, Microsoft Edge, Brave, Opera, or Vivaldi
2. Connect your Keychron keyboard via USB
3. Remap keys, configure layers, adjust lighting, and fine-tune HE sensitivity - changes apply instantly

Keychron Launcher works out of the box with no JSON import required, and supports features beyond VIA such as Hall Effect actuation point tuning and rapid trigger configuration. Safari and other non-Chromium browsers will not work with Keychron Launcher.

