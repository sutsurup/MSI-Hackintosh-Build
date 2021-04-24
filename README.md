# MSI Tempered Tower (w/ Intel)

[![macOS](https://img.shields.io/badge/macOS-11.1-orange)](https://www.apple.com.cn/macos/big-sur-preview/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.6.6-9cf)](https://github.com/acidanthera/OpenCorePkg)
[![release](https://img.shields.io/badge/indir-son%20sürüm-blue.svg)](https://github.com/sutsurup/MSI-Hackintosh-Build/releases)

<img align="right" src="Images/logo-png.png" alt="MSI" width="200">

Türkçe | [English](https://github.com/sutsurup/MSI-Hackintosh-Build/blob/main/README_EN.md)

**macOS Versiyonu: 11.1**

**OpenCore Versiyonu: 0.6.6**

Bu OpenCore Hackintosh yapısı B460M Mortar WiFi, i5-10400F, RX 5500 XT için yapılmıştır.

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
| Güç Kaynağı       | Corsair CV Serisi CV650 — 650 Watt 80 Plus Bronz Sertifikalı PSU                        |

### Çalışıyor

- [x] iCloud
- [x] iMessage
- [x] FaceTime
- [x] Sanallaştırma (w/Bluestacks, VirtualBox)
- [x] Uyku
- [x] Wireless
- [x] Ses (Layout: 1)

### Çalışmıyor (henüz)
- [ ] Bluetooth
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
[Destek kaydı oluşturabilirsiniz](https://github.com/sutsurup/MSI-Hackintosh-Build/issues) veya mail: [veyselfurkan@icloud.com](mailto:veyselfurkan@icloud.com)

### Güncellemeler
  <details>
  <summary>2021-02-13</summary>
  macOS Big Sur 11.1 sürümüne geçildi. OC 0.6.6 güncellendi. Düzenlemelerimi yaptıktan sonra Releases bölümüne yakın zamanda eklenecektir.
</details>
<details>
  <summary>2020-12-26</summary>
  OC 0.6.3 güncellendi.
</details>

### Destek olun.
Projeyi faydalı bulduysanız, kaynak bulma konusunda bana yardımcı olmak için bağış yapabilirsiniz:
```
₿ 1Q8CEMHTuecxPUJpEdpRiG6Bg2GVtzw4bN
``` 
<a href='https://github.com/sutsurup/sutsurup/blob/main/Donate.md'><img alt='Bağış' src='https://github.com/sutsurup/MSI-Hackintosh-Build/blob/main/Images/donate.png?raw=true' height='360px' width='375px'/></a>
```
QR koda tıklayarak alternatif seçeneklere ulaşabilirsiniz
``` 
