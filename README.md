# OrangeFox Recovery for Xiaomi Mi 10 (umi)

![Device](https://img.shields.io/badge/Device-Xiaomi%20Mi%2010-orange)
![Status](https://img.shields.io/badge/Status-Stable-green)
![Branch](https://img.shields.io/badge/Branch-OrangeFox%2012.1-orange)
![Maintainer](https://img.shields.io/badge/Maintainer-qoij-blue)

## Device Specifications

| Feature | Specification |
|---------|--------------|
| Device | Xiaomi Mi 10 |
| Codename | umi |
| SoC | Qualcomm Snapdragon 865 (kona) |
| Architecture | ARM64 |
| RAM | 8/12 GB |
| Storage | 128/256 GB |
| Display | 6.67" AMOLED 1080x2340 |
| Battery | 4780 mAh |
| Supported MIUI | MIUI 12, 13, 14, HyperOS 1 |
| Supported Android | 12 - 16 |

## Status

| Feature | Status |
|---------|--------|
| Decryption | ✅ Working |
| MTP | ✅ Working |
| ADB | ✅ Working |
| Backup/Restore | ✅ Working |
| Flash ZIPs | ✅ Working |
| Mount Partitions | ✅ Working |

## Build Instructions

### Requirements
- Ubuntu 20.04 or higher
- At least 16GB RAM
- At least 150GB free disk space

### Steps

```bash
# Initialize repo
repo init -u https://gitlab.com/OrangeFox/sync.git -b 12.1
repo sync

# Clone device tree
git clone https://github.com/qoij69/android_device_xiaomi_umi device/xiaomi/umi -b fox_12.1

# Build
export FOX_BUILD_DEVICE=umi
source build/envsetup.sh
lunch twrp_umi-eng
mka recoveryimage
```

## Download
Get the latest build from the [Releases](https://github.com/qoij69/android_device_xiaomi_umi/releases) page.

## Credits
- [OrangeFox Recovery Project](https://orangefox.download)
- [TeamWin (TWRP)](https://twrp.me)
- Xiaomi sm8250-common contributors

## Maintainer
**qoij** — [GitHub](https://github.com/qoij69)
