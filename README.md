<a href="https://github.com/CaninoDev/Mechanical_Keyboard_KiCAD_Templates"><img src="http://i.imgur.com/2TQ86Dp.png" title="Mechanical Keyboards KiCAD Templates" alt="KiCAD Templates"></a>

# Mechanical Keyboard KiCAD Templates

A collection of KiCAD templates to help the budding designer start designing their own mechanical keyboards.

 [![Github Issues](http://githubbadges.herokuapp.com/badges/badgerbadgerbadger/issues.svg?style=flat-square)](https://github.com/badges/badgerbadgerbadger/issues) 
 [![Pending Pull-Requests](http://githubbadges.herokuapp.com/badges/badgerbadgerbadger/pulls.svg?style=flat-square)](https://github.com/badges/badgerbadgerbadger/pulls) 
 [![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

<!-- TABLE OF CONTENTS -->
## Table of Contents

- [About The Project](#about-the-project)
- [Requirements](#requirements)
- [Installation](#installation)
- [Contributing](#contributing)
- [License](#license)

---
<!-- ABOUT THE PROJECT -->
## About The Project

This repository contains a collection of KiCAD mechanical keyboard templates using a variety of MCU's. Within each templates are schematics that lay out the basic connection between essential components as well as sub-sheets where the designer can implement their own key matrix and, in some cases, RGB LED underglow implementations. In most cases the KiCAD libraries in use were provided by [ai03](https://github.com/ai03-2725)

---
<!-- REQUIREMENTS -->
## Requirements

- [KiCAD v5](http://www.kicad-pcb.org/)

<!-- INSTALLATION -->
## Installation

- `git clone https://github.com/CaninoDev/Mechanica_Keyboard_KiCAD_Templates $TEMPLATE_DIRECTORY` where `$TEMPLATE_DIRECTORY` is the path to templates by your version of KiCAD. You can view and set the path by starting up KiCAD and going to `Preferences --> Configure Path --> KICAD_USER_TEMPLATE_DIR` 
- Once installed, go to `File --> Start a New Project From Template` and select the desired template from the list.

<!-- NOTES -->
## Notes

### Key Terms

MCU / Microcontroller
ESD
Voltage Regulator
Decoupling Capacitors
Pull Down Resistors

<!-- Design Guidlines -->
### Design Guidelines

<!-- PCB DESIGN -->
#### PCB Design

- Keep traces from the connector to the MCU as short as possible.
- Generally, avoid the use of sharp bends when laying down track.
- Power and Ground traces should be wide.
- Place the crystal as close to the MCU as possible.
- Isolate the oscillator as much as possible:
  - Separate the ground plane underneath the crystal generally.
- D+ and D- traces should match up in distance as close as possible (so the signals are in sync). Use differential(90Ω) traces.
- Fill Zones: It is not necessary to fill the entire PCB with ground/power plane. It is sufficient to encompass the crystal, USB and MCU footprints in a ground fill.

<!-- REFERENCE KEYBOARDS -->
### Reference Keyboards

Please note, some of the following keyboards have schematics that may be incomplete. I try to make note of those keyboards but cannot guarantee that I have caught them all.

<!-- ATMEGA -->
#### [atmega32](https://www.microchip.com/wwwproducts/en/ATmega32)

- [atmega32u4](https://www.microchip.com/wwwproducts/en/ATmega32U4)
  - [cpm43](https://github.com/Gtrx0/cpm43.git)
  - [ErgoDox](https://github.com/Ergodox-io/ErgoDox.git)
  - [helix](https://github.com/MakotoKurauchi/helix.git)
  - [KBD8X-MKII](https://github.com/ai03-2725/KBD8X-MKII-PCB.git)
  - [Lily58](https://github.com/kata0510/Lily58.git)
  - [Plain60](https://github.com/Maartenwut/plain60-c.git)
  - [Voyager60](https://github.com/ai03-2725/Voyager60.git)
  - [wc40noled](https://github.com/worldspawn00/wc40noled.git)
- [atmega32a](https://www.microchip.com/wwwproducts/en/ATmega32A)
  - [Planck - Throughole Variant](https://github.com/olkb/planck_thk.git)
- [at90usb1286](https://www.microchip.com/wwwproducts/en/AT90USB1286)
  - [JayKey1](https://github.com/josuegaleas/JayKey1.git)

#### [stm32](https://www.st.com/en/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html) 

(NOTE: The stm32 MCU series are, for the most part, interchangeable with minimal changes. Pay particular attention that the F072 series have a built-clock suitable for USB data transmissions.)

- [stm32f0x2](https://www.st.com/en/microcontrollers-microprocessors/stm32f0x2.html)
  - f042
    - [stm32 mech keyboard](https://github.com/julbouln/stm32_mech_keyboard.git)
  - f072
    - [DashKey](https://github.com/logically-c/DashKey.git)
    - [Shi-Chi](https://github.com/FateNozomi/shichi-pcb.git)
    - [st40](https://github.com/coarse/st40.git) *incomplete*
    - [ut47.3](https://github.com/coarse/UT47.3.git) *incomplete*
  - f103
    - [stm60](https://github.com/yangdigi/STM60-Keyboard-PCB.git)
- [stm32f3](https://www.st.com/content/st_com/en/products/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus/stm32-mainstream-mcus/stm32f3-series.html)
  - f303
    - [CO60](https://github.com/jmdaly/CO60.git)
    - [keypad](https://github.com/Fabian0520/keypad)
    - [Shark](https://github.com/Gondolindrim/SharkPCB.git)
    - [SteamVan](https://github.com/jmdaly/steamvan)

<!-- DISCLAIMER -->
## Disclaimer

As I am still learning how to design keyboards, there may be some implementations that does not represent best practices or may even be incorrect. In such cases, please make a pull request and I will incorporate the corrections promptly. When creating a new design from template, KiCAD copies over the local libraries but doesn't preserve their respective git. This results in a relatively larger project with the inability to effortlessly update local libraries.

---
<!-- CONTRIBUTING -->
## Contributing

> As noted above, there may be some mistakes in implementation or improvements could be made. If you note either, please:

### Step 1

    - 🍴 Fork this repo!

### Step 2
    - 👯 Make a branch concering the variant that will be modified.

### Step 3
    - HACK AWAY🔨🔨🔨

### Step 4
    - 🔃 Create a new pull request using <a href="https://github.com/CaninoDev/Mechanica_Keyboard_KiCAD_Templates/compare/" target="_blank">`https://github.com/CaninoDev/Mechanica_Keyboard_KiCAD_Templates/compare/`</a> detailing in the comments whether it is a correction and reference the reasons either by explanation or datasheet reference. If it is an improvement, explain the improvement. This is so  that not only I can learn from mistakes but so that others can as well. 
---
## Thanks

The following people have been invaluable in my journey in learning how to design keyboards:

- Worldspawn#9316, Abec13#3342, Comrade. SeungheonOh#4283, and The_Royal • 🍦 GMK Fro.Yo 🍦#3000 at the '40% Keeb' Discord server. 
- ai03#2725, PheonixStarr#0371, Xaetral#3486 at the 'ai03 Design Studio' Discord server

KiCAD libraries to aid in the schematics and pcb design
- [ai03's MX/Alps Hybrid](https://github.com/ai03-2725/MX_Alps_Hybrid)
- [my fork of ai03's MX/Alps Hybrid](https://github.com/CaninoDev/MX_Alps_Hybrid) that includes hotswap variants as well (pull request approval pending).
- [ai03's random keyboard parts](https://github.com/ai03-2725/random-keyboard-parts.pretty)
- [keebio's parts](https://github.com/keebio/Keebio-Parts.pretty)

These resources were immensely helpful
- [ai03's wiki](https://wiki.ai03.me/)
- [delapoite's list](https://github.com/Delapouite/awesome-keyboard)
- [benroe's awesome list](https://github.com/BenRoe/awesome-mechanical-keyboard)
- [komar's 'How To Make a Keybaord - The Matrix' blog post](http://blog.komar.be/how-to-make-a-keyboard-the-matrix/)
- [blakesmith's 'Making my own USB Keyboard From Scratch' post](http://blakesmith.me/2019/01/16/making-my-own-usb-keyboard-from-scratch.html)
- [Steamvan](https://github.com/jmdaly/steamvan)

These are related resources to mechanical keyboard design
- [3D Hub's guide to CNC Machining](https://www.3dhubs.com/knowledge-base/how-design-parts-cnc-machining)
- [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/)
- [Swill's Plate Building Tool](http://www.keyboard-layout-editor.com/)
- [GeekHack's Making Stuff Together forum](https://geekhack.org/index.php?board=117.0)
- [ElectronicDesign's Make the Most of your USB Functionality](https://www.electronicdesign.com/power/make-most-your-usb-functionality)
- [Crystal Oscillator Design](http://hoani.net/engineering/crystal-oscillator-design/)
- [Make the Most of Your USB Functionality](https://www.electronicdesign.com/power/make-most-your-usb-functionality)
-- 
## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
- Copyright 2019 ©
