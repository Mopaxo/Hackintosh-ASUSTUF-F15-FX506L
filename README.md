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

* If you need the Big Sur or Monterey Image to make an USB Stick, **i would recommend visit the** [orarlila_vanilla_images_site](https://www.olarila.com/topic/6278-hackintosh-and-macintosh-olarila-vanilla-images-macos-installer/) as a second step. These images come with extra programs to copy on your hackintosh after installation. If you want to make this USB stick from Windows Computer, **i would recommend get this program** [balena_etcher](https://www.balena.io/etcher/).

* Then you will need the EFI folder corresponding to the archicteture of your processor, in this case i took the efi folder for the commet-lake processors from [orarlila_efi_folders_site](https://www.olarila.com/topic/5676-hackintosh-efi-folder-for-all-chipsets-clover-and-opencore-macos/). In this case, you will only take the EFI folder from this repository, and put that folder in your USB Stick EFI Partition to get the main features like sound, wifi and blueetooth working. 

## Some Issues & Some Solutions:

### Wifi & Bluetooth

 * To get the wifi and bluetooth working, **you can use the drivers (kexts) from** [open_intel_wireless_repository](https://github.com/OpenIntelWireless/itlwm/releases). The version that worked for me was the itlwm_v2.1.0_stable.kext.zip (14.7mb). 

 * To get the bluetooth working, **you can use the drivers (kexts) from** [open_intel_bluetooth_firmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases). The version that worked for me was the IntelBluetoothFirmware-v2.1.0.zip (14.7mb). I also used "BlueToolFixup" to make the turn on / off switch of bluetooth feature work from this link: https://www.mediafire.com/file/wbelm42pkw5z0h1/Solucion_Intel_BT_%2526_WiFi_Hackintosh.zip/file.
 
  * You need to put these drivers on efi/oc/kexts folder and update the config.plist file with some easy-editor. **I used the ProperTree-Editor from** [corpnewt-propertree-repository](https://github.com/corpnewt/ProperTree).

 * Also you will need a UI program to get the wifi working with the kext. **i would recommend get this program** [heli_port](https://github.com/OpenIntelWireless/HeliPort/releases/tag/v1.4.1). Add heliport to your startup items under login and hide the orginal with dozer and it's hard to see the difference.
 
### Audio

 * To get the audio working, you will need one KEXT to enable the audio support: ```AppleALC.kext```.
 
 * Make sure you inject audio layout-id = 17 in OpenCore - this is in the current config.plist. The option is the NVRAM dictonary, who has one child dictonary called "boot-args" with one atribute called "alcid". Alcid is equal to Layout, it just the same but with another name.

### Elan Trackpad (TPAD)

 * To get the trackpad working, **use the latest VoodooI2C** [voodool2c_repository](https://github.com/VoodooI2C/VoodooI2C/releases)

 * The touchpad works mostly fine, but the buttons only work when the tochpad is touched. both buttons work as left button, so can be used for drag and drop.
 
 * Occassionally there is some delay/tear, right click works by enabling double finger click.



