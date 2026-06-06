# ZMK configuration for TOTEM
This is a customized keyboard layout configuration using [ZMK](https://zmk.dev).
The layout is supposed to be optimized for programming usage.
It uses the [Dvorak](https://www.kaufmann.no/roland/dvorak/) layout and is based off of [this repository](https://github.com/perryfranks/zmk_corne_prog_dvorak) by [perryfranks](https://github.com/perryfranks).
It is slightly tweaked for my own needs. 

Localizations are also available for german and (probably sometime in the future) english keyboard layouts.

## Layout
To view the layers and their layouts, take a look at the [Layout.md](./Layout.md) file.

## Building
You can use the precompiled firmware image with the german layout variant by directly downloading it from the GitHub Actions of this repo (therefore skipping steps 1-7).
Otherwise you can also build the firmware with the desired localized keyboard layout (and optional additional changes) by performing the following steps:
1. Fork this repository
2. Enable GitHub actions for the forked repository
3. Clone the forked repository
4. Copy and rename the desired keymap file to `totem.keymap` replacing the existing file (By default the english layout already has this name)
5. Optionally make additional changes to the keymap
6. Commit and push the changes
7. Wait for the action to finish building the firmware image and download it from the artifacts
8. Unzip the downloaded ZIP-file and connect the left side of the TOTEM keyboard to the PC via USB.
9. Push the Reset-button twice. Then a new USB storage device should show up.
10. Copy the unzipped `totem_left-seeeduino_xiao_ble-zmk.uf2` on the USB storage device and wait for the device to disconnect again.
11. Unplug the left side, connect the right side and repeat the steps to copy the `totem_right-seeeduino_xiao_ble-zmk.uf2` file onto the device.
12. Connect the TOTEM keyboard like you normally would and it should work with the new layout

## Credits & References
Original firmware: [iamavolk/totem-shield-module](https://github.com/iamavolk/totem-shield-module) \
TOTEM Keyboard: [GEIGEIGEIST/TOTEM](https://github.com/GEIGEIGEIST/TOTEM) \
Original Dvorak ZMK layout: [perryfranks/zmk_corne_prog_dvorak](https://github.com/perryfranks/zmk_corne_prog_dvorak) \
ZMK Project: [ZMK Homepage](https://zmk.dev/docs)