# MSI Tempered Tower (w/ Intel)

[![macOS](https://img.shields.io/badge/macOS-10.15.7-orange)](https://www.apple.com.cn/macos/big-sur-preview/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.6.3-9cf)](https://github.com/acidanthera/OpenCorePkg)
[![release](https://img.shields.io/badge/indir-son%20sürüm-blue.svg)](https://github.com/sutsurup/MSI-Hackintosh-Build/releases)

<img align="right" src="https://storage-asset.msi.com/event/msi_main_style/global_support/images/msilogo-w.png" alt="Critter" width="200">

Türkçe | [English](https://github.com/sutsurup/MSI-Hackintosh-Build/README_EN.md)

**macOS Versiyonu: 10.15.7**

**OpenCore Versiyonu: 0.6.3**

Bu OpenCore Hackintosh yapısı i5-10400F, RX 5500 XT, B460M Mortar (WiFi versiyonu) için yapılmıştır.

Yardımcı olabilecek kaynaklar: 

- [OpenCore Yükleme Rehberi](https://dortania.github.io/OpenCore-Install-Guide)

## Donanım

| ║▌║ **MSI** ║▌║ | Detay                                                  |
| ------------------- | ------------------------------------------- |
| Kasa           | MSI MPG GUNGNIR 110R Mid-Tower USB 3.2 Gen 1/2 ARGB     |
| Anakart           | MSI MAG B460M MORTAR WIFI (Intel® B460 Chipset)     |
| İşlemci              | Intel® Core™ i5-10400F 2.90GHz (up to 4.30GHz) Comet Lake              |
| RAM           | Corsair VENGEANCE® RGB PRO 16GB (2 x 8GB) DDR4 DRAM 3000MHz CL15     |
| Grafik Kartı | MSI Radeon RX 5500 XT GAMING X 8G (1845 MHz) GDDR6                     |
| Wi-Fi             | Intel® AX200 802.11 a/b/g/n/ac/ax 2.4GHz-5GHz up to 2.4Gbps WiFi 6 |
| Ses       | Realtek® ALC1200 Codec                        |

### Çalışıyor

- [x] iCloud
- [x] iMessage
- [x] FaceTime
- [x] Virtualization (w/Bluestacks, VirtualBox)
- [x] Sleep

### Çalışmıyor (henüz)
- [ ] Airdrop

### Klasör Yapısı
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

## Wi-Fi için
B460M Mortar WiFi anakartta halihazırda WiFi-Bluetooth entegrasyonu bulunmaktadır. Bu entegrasyon için gerekli dosyaları EFI klasörüne ekledim fakat WiFi panelini görüntülemek için HeliPort uygulamasını çalıştırmanız gerekiyor.
Buradan indirebilirsiniz: [HeliPort](https://github.com/OpenIntelWireless/HeliPort/releases/tag/v1.0.1) (HeliPort.dmg)


## Önemli
Bu dosya config.plist dosyasıdır. Lütfen change MLB, SystemSerialNumber, SystemUUID bölümlerindeki sayıları kendi sisteminiz için oluşturduğunuz sayılarla değiştirin.
Nasıl yapılır: [config.plist Düzenlemesi](https://osxinfo.net/konu/opencore-ile-imessage-ve-apple-servislerini-aktif-etmek.16297),
Neden yapıyoruz?: Bu bilgiler tek bir cihaza özel olmalıdır. Bu sebeple kendi cihazınıza özel numaralar oluşturmanız gerekiyor. iCloud'a giriş yapmayacaksanız bir önemi yoktur.

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

### İletişim kurun
[Yeni bir destek kaydı oluşturabilirsiniz](https://github.com/sutsurup/MSI-Hackintosh-Build/issues) veya mail: [veyselfurkan@icloud.com](mailto:veyselfurkan@icloud.com)

### Güncellemeler
- 2020-12-26
  OC 0.6.3 güncellendi.
<details>
  <summary>2020-12-26</summary>
  OC 0.6.3 güncellendi.
</details>
