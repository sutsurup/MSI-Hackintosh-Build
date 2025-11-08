# MSI Tempered Tower (w/ Intel)

[![macOS](https://img.shields.io/badge/macOS-11.1-orange)](https://www.apple.com.cn/macos/big-sur-preview/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.6.6-9cf)](https://github.com/acidanthera/OpenCorePkg)
[![release](https://img.shields.io/badge/download-last%20version-blue.svg)](https://github.com/sutsurup/MSI-Hackintosh-Build/releases)

<img align="right" src="Images/logo-png.png" alt="MSI" width="200">

[Türkçe](README.md) | English

**macOS Version: 11.1**

**OpenCore Version: 0.6.6**

This OpenCore Hackintosh build is made for B460M Mortar WiFi, i5-10400F, RX 5500 XT.

Helpful resources:

- [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide)

## Hardware

| ║▌║ **MSI** ║▌║ | Detail                                                  |
| ------------------- | ------------------------------------------- |
| Case           | MSI MPG GUNGNIR 110R Mid-Tower USB 3.2 Gen 1/2 ARGB     |
| Motherboard           | MSI MAG B460M MORTAR WIFI (Intel® B460 Chipset)     |
| Processor              | Intel® Core™ i5-10400F 2.90GHz (up to 4.30GHz) Comet Lake              |
| RAM           | Corsair VENGEANCE® RGB PRO 16GB (2 x 8GB) DDR4 DRAM 3000MHz CL15     |
| Graphics Card | MSI Radeon RX 5500 XT GAMING X 8G (1845 MHz) GDDR6                     |
| Wi-Fi             | Intel® AX200 802.11 a/b/g/n/ac/ax 2.4GHz-5GHz up to 2.4Gbps WiFi 6 |
| Audio       | Realtek® ALC1200 Codec                        |
| Power Supply       | Corsair CV Series CV650 — 650 Watt 80 Plus Bronze Certified PSU                        |

### Working

- [x] iCloud
- [x] iMessage
- [x] FaceTime
- [x] Virtualization (w/Bluestacks, VirtualBox)
- [x] Sleep
- [x] Wireless
- [x] Audio (Layout: 1)

### Not working (yet)
- [ ] Bluetooth
- [ ] Airdrop

### Folder Structure
```
.
├── EFI
│   ├── BOOT
│   │   └── BOOTx64.efi
│   └── OC
│       ├── ACPI
│       │   ├── SSDT-AWAC.aml
│       │   ├── SSDT-EC-USBX-DESKTOP.aml
│       │   ├── SSDT-PLUG.aml
│       │   └── SSDT-RX 5500 XT.aml
│       ├── Bootstrap
│       │   └── Bootstrap.efi
│       ├── Drivers
│       │   ├── HfsPlus.efi
│       │   └── OpenRuntime.efi
│       ├── Kexts
│       │   ├── AppleALC.kext
│       │   ├── dAGPM.kext
│       │   ├── itlwm.kext
│       │   ├── Lilu.kext
│       │   ├── LucyRTL8125Ethernet.kext
│       │   ├── NVMeFix.kext
│       │   ├── SMCProcessor.kext
│       │   ├── SMCSuperIO.kext
│       │   ├── USBPorts.kext
│       │   ├── VirtualSMC.kext
│       │   ├── WhateverGreen.kext
│       │   └── XHCI-unsupported.kext
│       ├── OpenCore.efi
│       ├── Tools
│       │   └── OpenShell.efi
│       └── config.plist
│   README_EN.md
└── README.md
```

## For Wi-Fi
The B460M Mortar WiFi motherboard already has WiFi-Bluetooth integration. I have added the necessary files for this integration to the EFI folder, but you need to run the HeliPort application to view the WiFi panel.
You can download it here: [HeliPort](https://github.com/OpenIntelWireless/HeliPort/releases/tag/v1.0.1) (HeliPort.dmg)


## Important
This file is the config.plist file. Please replace the numbers in the MLB, SystemSerialNumber, SystemUUID sections with the numbers you generated for your own system.
How to do it: [Editing config.plist](https://osxinfo.net/konu/opencore-ile-imessage-ve-apple-servislerini-aktif-etmek.16297),
Why are we doing this?: This information must be unique to a single device. Therefore, you need to generate your own unique numbers for your device. It doesn't matter if you're not signing into iCloud.

```
<dict>
    <key>AdviseWindows</key>
    <false/>
    <key>MLB</key>
    <string>xxxxxxxxxxxxxxx</string>
    <key>ROM</key>
    <data>ESIzRFVm</data>
    <key>SpoofVendor</key>
    <true/>
    <key>SystemProductName</key>
    <string>iMac19,1</string>
    <key>SystemSerialNumber</key>
    <string>xxxxxxxxxxx</string>
    <key>SystemUUID</key>
    <string>xxxxxxxx-xxxxx-xxxxx-xxxx-xxxxxxxx</string>
</dict>
```

### Get in touch
Website: https://sutsurup.tr // Mail: veysel@sutsurup.tr

### Updates
  <details>
  <summary>2021-02-13</summary>
  Switched to macOS Big Sur 11.1. Updated to OC 0.6.6. It will be added to the Releases section soon after I make my edits.
</details>
<details>
  <summary>2020-12-26</summary>
  Updated to OC 0.6.3.
</details>

### Support me.
If you found the project useful, you can donate to help me find resources:
```
₿ 1Q8CEMHTuecxPUJpEdpRiG6Bg2GVtzw4bN
``` 
<a href='https://github.com/sutsurup/sutsurup/blob/main/Donate.md'><img alt='Donate' src='https://github.com/sutsurup/MSI-Hackintosh-Build/blob/main/Images/donate.png?raw=true' height='360px' width='375px'/></a>
```
Click on the QR code for alternative options
``` 
