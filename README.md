# DELL Latitude E5570 Hackintosh Opencore

<p align="center">
  <img src="./screens/screenshot.png" style="margin: auto;"/>
</p>

## Overview

This is the Hackintosh Opencore EFI for the DELL Latitude E5570. Available for some DELL Latitude E5470 models. ([See more](https://github.com/misa198/dell-latitude-e5570-hackintosh/issues/9))

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

| Part                                                             | Status | Note                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ---------------------------------------------------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Keyboard (with volume keys, brightness keys, media control keys) | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Trackpoint                                                       | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Touchpad & 5 keys & gestures                                     | ✅     | There are 2 versions of EFI in the release. EFI_Acidanthera_VoodooPS2 uses Acidanthera's VoodooPS2 kext, which does not support macOS touchpad gestures. EFI_SkyrilHD_VoodooPS2 uses SkyrilHD's VoodooPS2 kext, which supports all macOS touchpad gestures, but this kext makes your laptop unstable, your laptop may freeze or reboot on its own. If you don't need to use touchpad gestures, I recommend using EFI_Acidanthera_VoodooPS2. |
| RJ45 LAN Port                                                    | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Wifi                                                             | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Bluetooth                                                        | ✅     | Bluetooth can stop working after sleep, this problem happens with all non-native cards. There is no fix yet. You can track the bug [here](https://github.com/acidanthera/bugtracker/issues/1821). If you want Bluetooth to work stably, you can use macOS BigSur instead of Monterey.                                                                                                                                                       |
| SD Card Reader                                                   | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Camera & Mic                                                     | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Speaker & 3.5mm audio port                                       | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| iGPU & VGA & HDMI                                                | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| USB                                                              | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Sleep                                                            | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Handoff                                                          | ✅     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Airdrop                                                          | ❌     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| AMD dGPU                                                         | ❌     | If you have                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Smart card reader                                                | ❌     |                                                                                                                                                                                                                                                                                                                                                                                                                                             |

## How to use?

This EFI is for `Monterey`. If you want to use it for other versions of macOS, you need to replace the 2 kexts in `EFI > OC > Kexts` and OC snapshot again:

- itlwm.kext to [version for your version of macOS](https://github.com/OpenIntelWireless/itlwm/releases)
- BlueToolFixup.kext to [IntelBluetoothInjector.kext](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases)

### Download EFI

- <a href="https://github.com/misa198/dell-latitude-e5570-hackintosh-opencore/releases">
    <img src="https://img.shields.io/github/v/release/misa198/dell-latitude-e5570-hackintosh?label=macOS Monterey&color=blue" />
  </a>

### Edit the efi you just downloaded

<p align="center">
  <img src="./screens/screenshot-smbios.png" style="margin: auto;"/>
</p>

- Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS) to generate SMBIOS.
- Use [ProperTree](https://github.com/corpnewt/ProperTree) to add SMBIOS information to config.plist file.

### Create boot

- Format your USB to `fat32`.
- Copy folder `EFI` to your USB.
- Create folder `com.apple.recovery.boot` in your USB.
- Download `macOS Recovery` - follow [here](https://dortania.github.io/OpenCore-Install-Guide/installer-guide/)
- Copy 2 files `BaseSystem.dmg` & `BaseSystem.chunklist` to folder `com.apple.recovery.boot`.

### Installing

- Follow [here](https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html)

## Credits

- [@quynkk1](https://github.com/quynkk1)
  - Fixing the problem of the vga port.
  - Remap brightness keys
  - Fixing touchpad gesture problem
