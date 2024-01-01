# DELL Latitude E5570 Hackintosh Opencore

<p align="center">
  <img src="./screens/screenshot.png" style="margin: auto;"/>
</p>

## Overview

This is the Hackintosh Opencore EFI for the DELL Latitude E5570. Available for some DELL Latitude E5470 models. ([See more](https://github.com/misa198/dell-latitude-e5570-hackintosh/issues/9))

This EFI is for `Sonoma`.
If you want to use for `Big Sur/Monterey`, please use [this](https://github.com/misa198/dell-latitude-5570-hackintosh/releases/tag/1.5.2)

## Specs

<p><i>This is spec of my laptop. This EFI can be used for all of DELL Latitude E5570</i></p>

| Part             | Description                                                                                                    |
| ---------------- | -------------------------------------------------------------------------------------------------------------- |
| CPU              | Intel® Core™ i5-6440HQ Processor                                                                               |
| iGPU             | Intel® HD 530                                                                                                  |
| Memory           | 16Gb (2 x Micron 8Gb 2133MHz)                                                                                  |
| Storage          | SSD 256GB SanDisk X300s m2 SATA                                                                                |
| Display          | IPS 15.6 inch 1920x1080                                                                                        |
| Wifi & Bluetooth | Intel® Wireless-AC 8260 Dual Band                                                                              |
| LAN              | Intel® Gigabit Ethernet, 10/100/1000                                                                           |
| Touchpad         | ALPS V8                                                                                                        |
| Audio            | Realtek ALC293                                                                                                 |
| External ports   | 3 x USB 3.0, 1 x RJ45, 1 x SD Card Reader, 1 x HDMI, 1 x 3.5 headphone/microphone combo, 1 x Smart Card Reader |

<h2>What works and what doesn't work?</h2>

| Part                                              | Status | Note                                                                               |
| ------------------------------------------------- | ------ | ---------------------------------------------------------------------------------- |
| Keyboard (with volume keys, , media control keys) | ✅     | Brightness keys does't work on Sonoma.                                             |
| Trackpoint                                        | ✅     |                                                                                    |
| Touchpad & 5 keys & gestures                      | ✅     | All features work, but the `Trackpad settings` are not showed in the `Preference`. |
| RJ45 LAN Port                                     | ✅     |                                                                                    |
| Wifi                                              | ✅     |                                                                                    |
| Bluetooth                                         | ✅     |                                                                                    |
| SD Card Reader                                    | ✅     |                                                                                    |
| Camera & Mic                                      | ✅     |                                                                                    |
| Speaker & 3.5mm audio port                        | ✅     |                                                                                    |
| iGPU & VGA & HDMI                                 | ✅     |                                                                                    |
| USB                                               | ✅     |                                                                                    |
| Sleep                                             | ✅     |                                                                                    |
| Handoff                                           | ✅     |                                                                                    |
| Airdrop                                           | ❌     |                                                                                    |
| AMD dGPU                                          | ❌     | If you have                                                                        |
| Smart card reader                                 | ❌     |                                                                                    |

## How to use?

### Download the EFI

- <a href="https://github.com/misa198/dell-latitude-e5570-hackintosh-opencore/releases">
    <img src="https://img.shields.io/github/v/release/misa198/dell-latitude-e5570-hackintosh?label=EFI&color=blue" />
  </a>

### Edit the efi you just downloaded

<p align="center">
  <img src="./screens/screenshot-smbios.png" style="margin: auto;"/>
</p>

- Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate SMBIOS. (🔴IMPORTANT❗🔴Use **`MacBookPro15,2`**)
- Use [ProperTree](https://github.com/corpnewt/ProperTree) to add SMBIOS information to config.plist file.

### Create boot

- Format your USB to `fat32`.
- Copy folder `EFI` to your USB.
- Create folder `com.apple.recovery.boot` in your USB.
- Download `macOS Recovery` - follow [here](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
- Copy 2 files `BaseSystem.dmg` & `BaseSystem.chunklist` to folder `com.apple.recovery.boot`.

### Installing

- Follow [here](https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html)
