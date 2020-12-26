# MSI Tempered Tower (with Intel)

[![macOS](https://img.shields.io/badge/macOS-10.15.7-orange)](https://www.apple.com.cn/macos/big-sur-preview/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.6.3-9cf)](https://github.com/acidanthera/OpenCorePkg)
[![release](https://img.shields.io/badge/download-last%20version-blue.svg)](https://github.com/sutsurup/MSI-Hackintosh-Build/releases)

<img align="right" src="https://storage-asset.msi.com/event/msi_main_style/global_support/images/msilogo-w.png" alt="Critter" width="200">

English | [Türkçe](https://github.com/sutsurup/MSI-Hackintosh-Build/blob/main/README.md)

**macOS Version: 10.15.7**

**OpenCore Version: 0.6.3**

This OpenCore hackintosh repository is made for i5-10400F, RX 5500 XT, Wi-Fi version of B460M Mortar.

Helpful Tips: 

- [OpenCore Install Guide](https://dortania.github.io/OpenCore-Install-Guide)

## Configuration

| ║▌║ **MSI** ║▌║ | Detay                                                  |
| ------------------- | ------------------------------------------- |
| Case           | MSI MPG GUNGNIR 110R Mid-Tower USB 3.2 Gen 1/2 ARGB     |
| MB           | MSI MAG B460M MORTAR WIFI (Intel® B460 Chipset)     |
| CPU              | Intel® Core™ i5-10400F 2.90GHz (up to 4.30GHz) Comet Lake              |
| RAM           | Corsair VENGEANCE® RGB PRO 16GB (2 x 8GB) DDR4 DRAM 3000MHz CL15     |
| GPU | MSI Radeon RX 5500 XT GAMING X 8G (1845 MHz) GDDR6                     |
| Wi-Fi             | Intel® AX200 802.11 a/b/g/n/ac/ax 2.4GHz-5GHz up to 2.4Gbps WiFi 6 |
| Sound       | Realtek® ALC1200 Codec                        |

### Working

- [x] iCloud
- [x] iMessage
- [x] FaceTime
- [x] Virtualization (w/Bluestacks, VirtualBox)
- [x] Sleep

### Not working (yet)
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
│       │   └── SSDT-RX\ 5500\ XT.aml
│       ├── Bootstrap
│       │   └── Bootstrap.efi
│       ├── Drivers
│       │   ├── HfsPlus.efi
│       │   └── OpenRuntime.efi
│       ├── Kexts
│       │   ├── AppleALC.kext
│       │   ├── Lilu.kext
│       │   ├── LucyRTL8125Ethernet.kext
│       │   ├── NVMeFix.kext
│       │   ├── SMCProcessor.kext
│       │   ├── SMCSuperIO.kext
│       │   ├── USBPorts.kext
│       │   ├── VirtualSMC.kext
│       │   ├── WhateverGreen.kext
│       │   ├── XHCI-unsupported.kext
│       │   └── dAGPM.kext
│       ├── OpenCore.efi
│       ├── Tools
│       │   └── OpenShell.efi
│       └── config.plist
└── README.md
```

## For Wi-Fi
The B460M Mortar WiFi already has WiFi-Bluetooth integration. I have added the necessary files to the EFI folder for this integration, but you need to run the HeliPort application to display the WiFi panel.
Download here: [HeliPort](https://github.com/openıntelwireless/heliport/releases/tag/v1.0.1) (HeliPort.dmg)

## Important
The file config.plist. Please change MLB, SystemSerialNumber, SystemUUID into your code.
How-To: [config.plist Setup](https://dortania.github.io/OpenCore-Install-Guide/config.plist/#adding-your-ssdts-kexts-and-firmware-drivers)

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

### Contact me
[Create a new issue](https://github.com/sutsurup/MSI-Hackintosh-Build/issues) or mail: [veyselfurkan@icloud.com](mailto:veyselfurkan@icloud.com)

### Updates
- 2020-12-26
  OC 0.6.3 updated.
<details>
  <summary>2020-12-26</summary>
  OC 0.6.3 updated.
</details>
