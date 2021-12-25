<h1> DELL Latitude E5570 Hackintosh Opencore</h1>

<p align="center">
  <img src="./screens/screenshot.png" style="margin: auto;"/>
</p>

<h2>Specs</h2>

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

<h2>What works and what doesn't work</h2>

| Part                                                             | Status | Note                                                                                                                                          |
| ---------------------------------------------------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------- |
| Keyboard (with volume keys, brightness keys, media control keys) | ✅     |                                                                                                                                               |
| Trackpoint                                                       | ✅     |                                                                                                                                               |
| Touchpad & 5 keys                                                | ✅     | 2 fingers, smooth scrolling not working (Can be fixed by [MOS](https://mos.caldis.me/) or [SmoothScroll](https://www.smoothscroll.net/mac/)). |
| RJ45 LAN Port                                                    | ✅     |                                                                                                                                               |
| Wifi                                                             | ✅     |                                                                                                                                               |
| Bluetooth                                                        | ✅     |                                                                                                                                               |
| SD Card Reader                                                   | ✅     |                                                                                                                                               |
| Camera & Mic                                                     | ✅     |                                                                                                                                               |
| Speaker & 3.5mm audio port                                       | ✅     |                                                                                                                                               |
| iGPU & VGA & HDMI                                                | ✅     |                                                                                                                                               |
| USB                                                              | ✅     |                                                                                                                                               |
| Sleep                                                            | ✅     |                                                                                                                                               |
| Handoff                                                          | ✅     |                                                                                                                                               |
| Airdrop                                                          | ❌     |                                                                                                                                               |
| AMD dGPU                                                         | ❌     | If you have                                                                                                                                   |
| Smart card reader                                                |        | Not tested yet                                                                                                                                |

<h2>How to use?</h2>
<i>As of EFI version 1.1.0 I only create EFI for macOS Monterey.</i>
<h3>Download EFI</h3>
<ul>
  <li>
    <a href="https://github.com/misa198/dell-latitude-e5570-hackintosh-opencore/releases">
      <img src="https://img.shields.io/github/v/release/misa198/dell-latitude-e5570-hackintosh?label=macOS Monterey&color=blue" />
    </a>
  </li>
  <li>
    <a href="https://github.com/misa198/dell-latitude-e5570-hackintosh/releases/tag/1.0.9">
      <img src="https://img.shields.io/badge/macOS%20Big%20Sur-v1.0.9-brightgreen" />
    </a>
  </li>
</ul>

<h3>Edit the efi you just downloaded</h3>
<p align="center">
  <img src="./screens/screenshot-smbios.png" style="margin: auto;"/>
</p>
<ul>
  <li>
    Use <a href="https://github.com/corpnewt/GenSMBIOS">GenSMBIOS</a> to generate SMBIOS.
  </li>
  <li>
    Use <a href="https://github.com/corpnewt/ProperTree">ProperTree</a> to add SMBIOS information to config.plist file.
  </li>
</ul>

<h3>Create boot</h3>
<ul>
  <li>Format your USB to <code>fat32</code>.</li>
  <li>Copy folder <code>EFI</code> to your USB.</li>
  <li>Create folder <code>com.apple.recovery.boot</code> in your USB.</li>
  <li>Download <code>macOS Recovery</code> - follow <a href="https://dortania.github.io/OpenCore-Install-Guide/installer-guide/">here</a>.</li>
  <li>Copy 2 files <code>BaseSystem.dmg</code> & <code>BaseSystem.chunklist</code> to folder <code>com.apple.recovery.boot</code>.</li>
</ul>

<h3>Installing</h3>
<ul>
  <li>Follow <a href="https://dortania.github.io/OpenCore-Install-Guide/installation/installation-process.html">here.</a></li>
</ul>
