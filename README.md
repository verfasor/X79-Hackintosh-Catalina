<img src="https://img.shields.io/liberapay/receives/verfasor.svg?logo=liberapay">

**Note: You're nothing but an a-hole if you sell EFI folder (config) that's readily available for free.**

# Budget X79 Xeon Build
An example EFI Folder (Clover) and config that works with X79 8-Core Xeon macOS High Catalina Hackintosh. 

![Xeon E5-2650 X79 Hackintosh Rig](https://res.cloudinary.com/mighil/image/upload/v1578646938/hackintosh-x79.jpg)

## System Specs

| Part | Model Number
| --- | --- 
| CPU | Xeon E5-2650 
| Motherboard | Ant Country X79 Basic
| GPU | RX 580 4B (AMD OEM)
| Memory | Samsung 8GB DDR3-1333Mhz ECC x 4
| PSU | Evesky 650W
| CPU Cooler | Frostwind ([Taobao](https://item.taobao.com/item.htm?spm=a1z09.2.0.0.31a12e8dWM24K7&id=535564128486&_u=a2el2vs09de7))
| mATX Case | 钢铁侠M1-N5 ([Tmall](https://detail.tmall.com/item.htm?id=44313549938&spm=a1z09.2.0.0.31a12e8dWM24K7&_u=a2el2vs084c6&skuId=4226396877333)) 
| Storage | 128GB SSD (macOS), 256GB SSD (Windows 10), 1TB HDD (Shared Storage)
| Mechanical KB | 赤暴Readson FH87

## README

- Proceed with caution.
- Tested on macOS Catalina 10.15.2.
- EFI folder is N/A for Opencore bootloader. Go ahead though, if you know what you're doing.
- Applicable for direct upgrade from High Sierra or Mojave.
- The EFI folder is applicable to SSD hot-swap also. ie, if you're planning to swap SSD from a MacBook Pro to ThinkPad 530.

## Before You Proceed

You should modify the EFI (a lot) if your system specs are different. I use the settings for my motherboard. Huanan X79 is another motherboard similar to mine.  The CPU type 0x0a01 I set in Clover is only applicable to 8-core CPU models. You should edit that out if your CPU config is different. Also, note that I’ve manually set my system memory info (4x 8GB) within the SMBIOS in Clover. You should edit that as well.

## Starter EFI 

If things go south, use the clover settings attached in the [starter-EFI](https://github.com/m1qnet/X79-Hackintosh-Catalina/tree/master/starter-EFI) folder. You can use it as a starter. But then you've to tweak settings a bit more.

## About Kexts

* Catalina update broke my LAN. I use a WiFi adapter for the time being. I added Realtek WLAN kexts (RtWlanU & RtWlanU1827) to use with the Comfast USB Wi-Fi adapter. You should edit the config. according to your preferences.
*  I’ve got a lot of other Kexts in place for sensors, just ignore or remove those.  

## BIOS Settings

You may proceed with the default settings for Ant Country X79 Basic. It may vary if you're using another motherboard.

## What Doesn’t Work?

- Ethernent (for the time being). I use a WiFi adapter, so no plans to fix that soon.
- iMessage & Facetime.(it'll work after SMBIOS edits)

## How to create a bootable macOS Catalina USB install drive? (on MacOS)

[Refer to this guide from 9to5mac](https://9to5mac.com/2019/06/27/how-to-create-a-bootable-macos-catalina-10-15-usb-install-drive-video/)

## How to create a bootable macOS Catalina USB install drive? (on Windows)

1. Install [Transmac](https://www.acutesystems.com/scrtm.htm) on a Windows machine. It has a 15-day trial period and works flawlessly flashing DMG files to USB.

2. Download the latest [MacOS 10.15.2 with clover DMG file from here](https://mirrors.dtops.cc/iso/MacOS/daliansky_macos/) or other sources you come across Google SERP.

3. Download the EFI folder from this repo.

4. Download [Clover Configurator for macOS](https://mackie100projects.altervista.org/download-clover-configurator/) (latest version).

5. Connect a 16 GB USB flash drive.

6. Open Transmac. In the left pane, right-click the USB Drive and select Format Disk for Mac

7. Again in the left pane, right-click the USB Drive and select Restore with Disk Image. Then select the DMG file I mentioned in (2). Flashing process will take a few minutes depending on the size of .dmg and speed/port of the USB drive.

8. Install [DiskGenius](https://www.diskgenius.com/).

9. Locate the USB drive in DiskGenius. Delete the EFI folder and replace it with the new EFI folder. 

10. Plug the USB drive into the PC and boot from USB.

11. Format the disk drive to APFS, install macOS Catalina, and restart the system.

12. Connect Hackintosh system to the Internet via USB tethering or a Mac-compatible external WiFi adapter.

13. Download & install Clover Configurator on MacOS. Open EFI partition and copy -> paste the the EFI folder once more. 

14. You may use [Karabiner-Elements](https://pqrs.org/osx/karabiner/) if the keyboard mappings (command and option) are acting up.

All the best.
