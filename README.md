## Disclaimer
This alpha version is for testing only.
It is not ready for daily use and we do not guarantee its usability.

As [Apple announced](https://www.apple.com/macos/macos-ventura-preview/), the new macOS Ventura will end support for MacbookPro 2016 and earlier (Skylake iGPU issue). The EFI of the Dell Latitude E5570 is based on the 2016 MacbookPro. But fortunately, Kabylabe and Skylake are quite similar (Kabylake iGPU supports VP9 codec, Skylake does not), so in the latest version of [WhateverGreen](https://github.com/acidanthera/WhateverGreen), the developers supported spoofing Kabylake's iGPU on Skylake.
Since Skylake doesn't support VP9 there will be some minor bugs (like playing Youtube videos on Safari may cause the device to freeze), but this is a good sign.

## Installation

* Use [gibMacOS](https://github.com/corpnewt/gibMacOS) to download macOS Ventura Beta.
* Mount the macOS you just downloaded to the USB following the instructions [here](https://support.apple.com/en-ca/HT201372).
* Then, follow the instructions in the [README](https://github.com/misa198/dell-latitude-e5570-hackintosh/blob/master/README.md).