# Clickety Split | Pepito v1.13

![Pepito v1.13 Wireless](https://github.com/ClicketySplit/build-guides/blob/main/pepito/images/gallery/Pepito_v1.13.jpg)

Keyboard Designer: [clicketysplit.ca](https://clicketysplit.ca) \
GitHub: [ClicketySplit](https://github.com/ClicketySplit) \
Hardware Supported: Seeed Studio XIAO BLE with nice!view Displays

Pepito is a 3x6x4m split keyboard. With Pepito's inaugural release being wireless, it leverages Seeed Studio XIAO BLE microcontrollers and nice!view memory-in-pixel displays.

## Features

- 3x6x4m Split Keyboard
- Support for Kailh Low Profile Choc switches with 18mm x 18mm spacing.
- All switch locations are socketed.
- nice!view Displays are inherently supported, socketed, and no extra wiring is required.
- Support for both 110mAh, 600mAh, or 700mAh batteries.
- Support for JST PH-2 Battery Connectors
- Support for Alps Alpine Micro On/off switches.

# Building Pepito ZMK Firmware

ZMK Firmware: [Introduction to ZMK](https://zmk.dev/docs/) \
Installation: [Installing ZMK](https://zmk.dev/docs/user-setup) \
Customization: [Customizing ZMK](https://zmk.dev/docs/customization) \
Development Environment: [Basic Setup](https://zmk.dev/docs/development/setup)

Build commands for the default keymap of Pepito v1.13:

```
west build -d build/pepito/left -p -b seeeduino_xiao_ble -- -DSHIELD=clickety_split_pepito_left

west build -d build/pepito/right -p -b seeeduino_xiao_ble -- -DSHIELD=clickety_split_pepito_right
```

Build commands for your custom keymap of Pepito v1.13:

```
west build -d build/pepito/left -p -b seeeduino_xiao_ble -- -DSHIELD=clickety_split_pepito_left  -DZMK_CONFIG="/workspaces/zmk-config/[your name]/pepito_v1.13/config"

west build -d build/pepito/right -p -b seeeduino_xiao_ble -- -DSHIELD=clickety_split_pepito_right  -DZMK_CONFIG="/workspaces/zmk-config/[your name]/pepito_v1.13/config"
```

## Building Pepito's ZMK Firmware with nice!view Displays

There is one file that need to be adjusted before the build commands can be run.

### Edit the clickety_split_pepito.conf File

Near the top the clickety_split_pepito.conf file, locate the following code block:

```
# Uncomment the following line to enable nice!view Displays
# CONFIG_ZMK_DISPLAY=y
```

Modify the block to resemble the following:

```
# Uncomment the following line to enable nice!view Displays
CONFIG_ZMK_DISPLAY=y
```

Save your changes and close the file.

### Sample Build Commands for nice!view Displays

Build commands for your custom keymap of Pepito v1.13:

```
west build -d build/pepito/left -p -b seeeduino_xiao_ble -- -DSHIELD=clickety_split_pepito_left  -DZMK_CONFIG="/workspaces/zmk-config/[your name]/pepito_v1.13/config"

west build -d build/pepito/right -p -b seeeduino_xiao_ble -- -DSHIELD=clickety_split_pepito_right  -DZMK_CONFIG="/workspaces/zmk-config/[your name]/pepito_v1.13/config"
```

# Support

If you have any questions with regards to Pepito, please [Contact Us](https://clicketysplit.ca/pages/contact-us).

Clickety Split
For the love of split keyboards.



```


/*                                      42 KEY MATRIX / LAYOUT MAPPING

  ╭────────────────────────┬────────────────────────╮ ╭─────────────────────────┬─────────────────────────╮

  │  0   1   2   3   4   5 │  6   7   8   9  10  11 │ │ LT5 LT4 LT3 LT2 LT1 LT0 │ RT0 RT1 RT2 RT3 RT4 RT5 │

  │ 12  13  14  15  16  17 │ 18  19  20  21  22  23 │ │ LM5 LM4 LM3 LM2 LM1 LM0 │ RM0 RM1 RM2 RM3 RM4 RM5 │

  │ 24  25  26  27  28  29 │ 30  31  32  33  34  35 │ │ LB5 LB4 LB3 LB2 LB1 LB0 │ RB0 RB1 RB2 RB3 RB4 RB5 │

  ╰───────╮ 36  37  38  39 │ 40  41  42  43  ╭──────╯ ╰───────╮ LH3 LH2 LH1 LH0 │ RH0 RH1 RH2 RH3 ╭───────╯

​          ╰────────────────┴─────────────────╯                ╰─────────────────┴─────────────────╯             */

```



​	qwertASDGF-DSAASD---

ow--
