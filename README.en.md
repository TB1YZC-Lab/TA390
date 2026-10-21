<p align="center"><img src="assets/icon.png" width="120" alt="TA390"></p>

<h1 align="center">TA390</h1>

<p align="center">
An <b>unofficial</b> DMR / FM firmware for the TYT MD-UV380 / MD-UV390, based on OpenGD77,<br>
with a Windows flashing and codeplug (CPS) program and an Android app.
</p>

<p align="center">
<a href="https://github.com/TB1YZC-Lab/TA390/releases/latest"><b>⬇ Download the latest release</b></a> ·
<a href="docs/TA390_v1.3_User_Manual_EN.pdf">User manual</a> ·
<a href="README.md">Türkçe</a>
</p>

---

## Download

All the files are on the [Releases](https://github.com/TB1YZC-Lab/TA390/releases/latest) page.

| File | Purpose |
|---|---|
| `TA390_v1.3.zip` | Radio firmware (`TA390_v1.3.bin`), language files, readme, licences |
| `TA390_Kurulum_v1.3.exe` | Windows program (setup): firmware flashing / update, backups, CPS |
| `TA390_v1.3.apk` | Android app: the same functions as the Windows program (over a USB OTG cable) |
| `TA390_v1.3_User_Manual_EN.pdf` | User manual (English) |
| `TA390_v1.3_Kullanim_Kilavuzu.pdf` | User manual (Turkish) |

The firmware, the Windows program and the Android app always have **the same version number**.

## Features

- **Dual Watch:** two stored channels of the zone are shown one under the other and monitored together (like the original TYT firmware).
- **Turkish or English menus** (chosen when flashing), a **shortcut list** readable on the radio.
- **Logs:** received DMR and FM calls are stored with date, time, length and channel.
- **APRS:** position sent independently of the open channel, **APRS messages** from the radio, DMR TA.
- **VFO:** step / range / FM-DMR scan, tone and colour code finder, save the frequency as a channel, signal strength (S / dBm).
- **Channel details:** the talkgroups of the TG list are selected with the knob.
- **Screen saver** (clock, date, battery), missed call and speaker icons, games (Snake, Tetris, Mines).
- **Windows and Android:** firmware flashing / update, Flash / MCU ROM / calibration backups, boot image, satellite data, CPS with drag and drop.

The programs can be switched to English in *Settings › Program language*.

## Quick installation

1. **Make backups first:** in the TA390 program, *Backup and more* › Flash, MCU ROM and Calibration.
2. Switch the radio off, switch it on while holding **PTT and the key above it** (the LED flashes red / green), plug the USB cable.
3. In the *Install / Update* tab select `TA390_v1.3.zip`, choose the radio language and press **Flash**.

See the user manual for the details.

### DMR audio (donor file)

The DMR audio codec (AMBE) is protected by copyright and patents and is **not distributed by this project**. For the first installation the program
downloads the official TYT **MD-9600 v26.45** firmware (the donor) to the user's own computer / phone, from the link given in the OpenGD77
installation guide, and adds the codec from it. Do not give your donor file to others.

### Good to know

- The Windows setup and the APK are not commercially signed: Windows may show a **SmartScreen** warning (“More info › Run anyway”), Android
  may ask to allow **installing from unknown sources**. Only download the files from this page.
- The Android app needs a phone with **USB OTG** support and an OTG cable / adapter.
- Flashing does not erase the calibration, but make backups before flashing anyway.

## Reporting issues

Please use [Issues](https://github.com/TB1YZC-Lab/TA390/issues).
**Do not contact the OpenGD77 team or forum about TA390 problems**; TA390 is not made by them.

## Licence and important notes

- TA390 is derived from the open source [OpenGD77](https://www.opengd77.com) firmware and is **not an official OpenGD77 release**.
  It is not made, endorsed or supported by the OpenGD77 developers.
- **Free of charge. No commercial use**: it may not be sold or made part of a paid product (OpenGD77 licence, clause 4).
- **No warranty.** Flashing and use are entirely at your own risk.
- This is amateur radio software; only use your radio on the frequencies and powers of your licence.

Licence: [LICENSE](LICENSE). Licences of the components: [LISANSLAR](LISANSLAR).

## Credits

OpenGD77: Kai DG4KLU (original design), Roger Clark VK3KYY, Daniel Caujolle-Bert F1RMB, Alex DL4LEX, Colin G4EML and the other OpenGD77
developers. The flashing method and the encoding tables are adapted from the OpenGD77 STM32 firmware loader.
FreeRTOS (MIT), STMicroelectronics STM32 HAL and USB Device Library, Arm CMSIS (Apache-2.0), libusb (LGPL-2.1),
APRS symbols: aprs.fi symbol set (OH7LZB), brand logos removed.

TA390: **TB1YZC**
