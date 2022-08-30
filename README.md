# Hackintosh-Asus-tuf-15-opencore

This repository was created for everyone looking how to make this laptop (Asus TUF Gaming F15 FX506L) run MacOS Monterey 12.5.1.

This repo was created after I was able to boot with the desktop files for Comet Lake platform. Most of the work to get this to work, was done by VGerris and his repository: https://github.com/VGerris/asus-tuf-15-opencore.

** macOS Version: Monterey 12.5.1 **

[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg)](https://github.com/996icu/996.ICU/blob/master/LICENSE)

**Open Core Version:** [0.8.3](https://github.com/acidanthera/OpenCorePkg/releases/tag/0.8.3)

|macOS Monterey 12.5.1 Tested|

## System's functionality: 

| Part | Functionality | Specific Model |
|---|---|---|
| BIOS VERSION: | ✅ | 310 |
| CPU: | ✅ | Intel(R) Core(TM) i7-10870H CPU @ 2.20GHz |
| RAM: | ✅ | 16GB DDR4 Micron 2933mhz |
| SSD: | ✅ | 500GB SSD SATA WD GREEN |
| IGPU: | ✅ | Intel UHD 630 |
| DGPU: | 🚫 | NVIDIA GTX 1650 4GB GDDR6 |
| WLAN: | ✅ | Intel AX201 Wifi 6 Card |
| Bluetooth: | ✅ | Intel Bluetooth |
| Ethernet: | ✅ | Realtek 8111 Gigabit Ethernet |
| Audio: | ✅ | Realtek HDA |
| Webcam: | ✅ | Integrated 720P Webcam |
| Microphone: | ✅ | Integrated Microphone |
| Internal Screen: | ✅ | 15.6" 1920x1080 144Hz |
| Trackpad: | ✅ / 🚫 | I2C ELAN1201 |

## Perfectly Natively Working Features: 

- [x] Sound Control Keys (Volume Up / Volume Down)
- [x] Intel Graphics UHD 630
- [x] Native Screen Refresh Rate (Legit 144hz)
- [x] Web Camera
- [x] Battery Percentage 
- [x] Native Hardware NVRAM
- [x] Sleep & Wake modes

## Guide:
 
* To learn how Open-Core works, **i would recommend reading the** [documentation_guide](https://dortania.github.io/OpenCore-Install-Guide/) as a first step. 

* If you need the Big Sur or Monterey Image to make an USB Stick, i would recommend visit the [orarlila_vanilla_images_site](https://www.olarila.com/topic/6278-hackintosh-and-macintosh-olarila-vanilla-images-macos-installer/) as a second step. These images come with extra programs to copy on your hackintosh after installation. If you want to make this USB stick from Windows Computer, i would recommend get this program [balena_etcher](https://www.balena.io/etcher/)

* Then you will need the EFI folder corresponding to the archicteture of your processor, in this case i took the efi folder for the commet-lake processors from [orarlila_efi_folders_site](https://www.olarila.com/topic/5676-hackintosh-efi-folder-for-all-chipsets-clover-and-opencore-macos/). In this case, you will only take the EFI Folder from this repository, and put that folder in your USB Stick EFI Partition to get the main features like sound, wifi and blueetooth working. 




