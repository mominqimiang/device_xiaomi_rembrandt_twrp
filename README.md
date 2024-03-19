### TWRP device tree for Redmi K60E (rembrandt)

=========================================

Redmi K60E (codenamed _"rembrandt"_) is a smartphone from Xiaomi.
![Redmi K60E](https://cdn.cnbj0.fds.api.mi-img.com/b2c-shopapi-pms/pms_1672037146.81276139.png)
It was released in December 2022.

## Device specifications

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | Octa-core CPU with 4x Arm Cortex-A78 up to 3.1GHz
Chipset | Mediatek Dimensity 8200
GPU     | Mali-G610 MC6
Memory  | 8/12 GB RAM (LPDDR5T 9600Mbps)
Shipped Android Version | 12
Storage | 256 GB (UFS 3.1)
Battery | Li-Po 5500 mAh, non-removable
Display | 1220 x 2712 pixels, 6.67 inches, 60/120 hz

## Features
Problems:
- [X] unmount vendor
- [X] directly flash magisk

Works:

- [X] ADB
- [X] Partially Decryption (Android 13)
- [X] Display
- [X] Fasbootd
- [X] Flashing
- [X] MTP
- [X] Sideload
- [X] USB OTG
- [X] Vibrator

## Donate me
![mmqmem](https://img2.imgtp.com/2024/03/05/FdGtaESF.jpg)

## To use it:

```
fastboot flash vendor_boot vendor_boot.img
```
