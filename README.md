# MSI Tempered Tower (w/ Intel)

[![macOS](https://img.shields.io/badge/macOS-11.1-orange)](https://www.apple.com.cn/macos/big-sur-preview/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.6.6-9cf)](https://github.com/acidanthera/OpenCorePkg)
[![release](https://img.shields.io/badge/indir-son%20sürüm-blue.svg)](https://github.com/sutsurup/MSI-Hackintosh-Build/releases)

<img align="right" src="Images/logo-png.png" alt="MSI" width="200">

Türkçe | [English](README_EN.md)

**macOS Sürümü: 11.1**

**OpenCore Sürümü: 0.6.6**

Bu OpenCore Hackintosh yapılandırması, B460M Mortar WiFi, i5-10400F ve RX 5500 XT için oluşturulmuştur.

Faydalı olabilecek kaynaklar:

- [OpenCore Yükleme Rehberi](https://dortania.github.io/OpenCore-Install-Guide)

## Donanım Özellikleri

| ║▌║ **MSI** ║▌║ | Model                                                  |
| ------------------- | ------------------------------------------- |
| Kasa           | MSI MPG GUNGNIR 110R Mid-Tower USB 3.2 Gen 1/2 ARGB     |
| Anakart           | MSI MAG B460M MORTAR WIFI (Intel® B460 Chipset)     |
| İşlemci              | Intel® Core™ i5-10400F 2.90GHz (4.30GHz'e kadar) Comet Lake              |
| RAM           | Corsair VENGEANCE® RGB PRO 16GB (2 x 8GB) DDR4 DRAM 3000MHz CL15     |
| Ekran Kartı | MSI Radeon RX 5500 XT GAMING X 8G (1845 MHz) GDDR6                     |
| Wi-Fi             | Intel® AX200 802.11 a/b/g/n/ac/ax 2.4GHz-5GHz, 2.4Gbps'e kadar WiFi 6 |
| Ses Kartı       | Realtek® ALC1200 Codec                        |
| Güç Kaynağı       | Corsair CV Serisi CV650 — 650 Watt 80 Plus Bronze Sertifikalı PSU                        |

### Çalışan Özellikler

- [x] iCloud
- [x] iMessage
- [x] FaceTime
- [x] Sanallaştırma (Bluestacks, VirtualBox vb.)
- [x] Uyku Modu
- [x] Wi-Fi
- [x] Ses (Layout: 1)

### Çalışmayan Özellikler (Henüz)
- [ ] Bluetooth
- [ ] AirDrop

### Dizin Yapısı
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

## Wi-Fi Kurulumu
B460M Mortar WiFi anakart, dahili Wi-Fi ve Bluetooth modülüne sahiptir. Gerekli sürücüler EFI klasörüne eklenmiştir; ancak, Wi-Fi ağlarını görebilmek için HeliPort uygulamasını çalıştırmanız gerekmektedir.
Uygulamayı buradan indirebilirsiniz: [HeliPort](https://github.com/OpenIntelWireless/HeliPort/releases/tag/v1.0.1) (HeliPort.dmg)


## Önemli Notlar
Bu EFI, `config.plist` dosyasını içerir. Lütfen `MLB`, `SystemSerialNumber` ve `SystemUUID` alanlarını kendi sisteminize özel olarak oluşturduğunuz değerlerle güncelleyin.
Nasıl yapılır: [config.plist Düzenleme Rehberi](https://osxinfo.net/konu/opencore-ile-imessage-ve-apple-servislerini-aktif-etmek.16297)
Neden gerekli? Bu bilgiler her cihaza özel olmalıdır. Bu nedenle, kendi cihazınıza özel seri numaraları oluşturmanız gerekir. iCloud'a giriş yapmayacaksanız bu adım zorunlu değildir.

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

### İletişim
Bir sorunla karşılaşırsanız [destek kaydı oluşturabilir](https://github.com/sutsurup/MSI-Hackintosh-Build/issues) veya aşağıdaki kanallardan bana ulaşabilirsiniz:

- **Website:** [sutsurup.tr](https://sutsurup.tr)
- **Mail:** [veysel@sutsurup.tr](mailto:veysel@sutsurup.tr)

### Güncellemeler
  <details>
  <summary>13.02.2021</summary>
  macOS Big Sur 11.1 sürümüne geçildi ve OpenCore 0.6.6'ya güncellendi. Düzenlemeler tamamlandıktan sonra yakın zamanda "Releases" bölümüne eklenecektir.
</details>
<details>
  <summary>26.12.2020</summary>
  OpenCore 0.6.3'e güncellendi.
</details>

### Destek Olun
Projeyi faydalı bulduysanız, yeni donanım ve kaynaklar için bağış yaparak destek olabilirsiniz:
```
₿ 1Q8CEMHTuecxPUJpEdpRiG6Bg2GVtzw4bN
``` 
<a href='https://github.com/sutsurup/sutsurup/blob/main/Donate.md'><img alt='Bağış' src='https://github.com/sutsurup/MSI-Hackintosh-Build/blob/main/Images/donate.png?raw=true' height='360px' width='375px'/></a>
```
QR koda tıklayarak alternatif bağış seçeneklerine ulaşabilirsiniz.
``` 
