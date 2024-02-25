### TWRP device tree for Redmi K60E (rembrandt)

=========================================

The Redmi K60E (codenamed _"rembrandt"_) is a high-end, mid-range smartphone from Xiaomi.

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

![Redmi K60E](https://cdn.cnbj0.fds.api.mi-img.com/b2c-shopapi-pms/pms_1672037146.81276139.png)

## Features
Problems:
- [X] mount system
- [X] unmount vendor

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
      


## Compile

First checkout minimal twrp with aosp tree:

```
repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12.1
repo sync -j$(nproc --all)
```

Then add these projects to .repo/manifest.xml:

```xml
<project path="device/xiaomi/rembrandt" name="mominqimiang/device_xiaomi_rembrandt_TWRP" remote="github" revision="TWRP-12.1_kernel_5.10.136" />
```

Finally execute these:

```
source build/envsetup.sh
repopick <needed patch>
lunch twrp_rembrandt-eng
mka vendorbootimage -j$(nproc --all)
```
## To use it:

```
fastboot flash vendor_boot out/target/product/rembrandt/vendor_boot.img
```
