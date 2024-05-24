## Devices

### List of known and supported devices

```
YUCHENG  F10H55W3AS  GK7205V300  IMX335  MT7601U_USB    NOR_16M   in progress
AKA      CH v1       GK7205V200  IMX307  RTL8733BU      NOR_16M   in progress
AKA      CH v2       GK7205V200  IMX307  MT7601U_USB    NOR_16M   in progress
AKA      CH-T31 v1   T31L        GC2083  MT7601U_USB    NOR_8M    in progress
AKA      CH-T31 v2   T31L        GC2083  RTL8188EU_USB  NOR_8M    in progress
XM       IVG-G3S     GK7205V210  IMX307  ATBM6032i_USB  NOR_16M   w/ext wifi board
```
### Upgrading from a SD card
```
# soc=$(fw_printenv -n soc)
# sysupgrade --kernel=/mnt/mmcblk0p1/uImage.${soc} --rootfs=/mnt/mmcblk0p1/rootfs.squashfs.${soc} -z --force_ver
...
# firstboot
```
### Images

#### YUCHENG F10H55W3AS
```
- uImage: [1816KB/2048KB]
- rootfs.squashfs: [6348KB/8192KB]
- Build time: 10:51
Copying files to local archive

Assembled firmware available in:
/mnt/EXT/projii/builder/archive/gk7205v300_ultimate_yucheng-f10h55w3as/202405241407
├── openipc.gk7205v300-nor-ultimate.tgz
├── rootfs.gk7205v300.tar
├── rootfs.squashfs.gk7205v300
└── uImage.gk7205v300
```
#### AKA CH v1
```
- uImage: [1814KB/2048KB]
- rootfs.squashfs: [5080KB/5120KB]
- Build time: 07:18
Copying files to local archive

Assembled firmware available in:
/mnt/EXT/projii/builder/archive/gk7205v200_lite_aka-ch-v1/202405231116
├── openipc.gk7205v200-nor-lite.tgz
├── rootfs.gk7205v200.tar
├── rootfs.squashfs.gk7205v200
└── uImage.gk7205v200
```
#### AKA CH v2
```
- uImage: [1814KB/2048KB]
- rootfs.squashfs: [4484KB/5120KB]
- Build time: 07:08
Copying files to local archive

Assembled firmware available in:
/mnt/EXT/projii/builder/archive/gk7205v200_lite_aka-ch-v2/202405241436
├── openipc.gk7205v200-nor-lite.tgz
├── rootfs.gk7205v200.tar
├── rootfs.squashfs.gk7205v200
└── uImage.gk7205v200
```
#### AKA CH-T31 v1
```
- uImage: [1786KB/2048KB]
- rootfs.squashfs: [4384KB/5120KB]
- Build time: 04:45
Copying files to local archive

Assembled firmware available in:
/mnt/IOTA/DATA/proj/builder/archive/t31_lite_aka-ch-v1/202405211035
├── openipc.t31-nor-lite.tgz
├── rootfs.squashfs.t31
├── rootfs.t31.tar
└── uImage.t31
```
#### AKA CH-T31 v2
```
- uImage: [1786KB/2048KB]
- rootfs.squashfs: [5064KB/5120KB]
- Build time: 04:48
Copying files to local archive

Assembled firmware available in:
/mnt/IOTA/DATA/proj/builder/archive/t31_lite_aka-ch-v2/202405211318
├── openipc.t31-nor-lite.tgz
├── rootfs.squashfs.t31
├── rootfs.t31.tar
└── uImage.t31
```
#### XM IVG-G3S
```
- uImage: [1814KB/2048KB]
- rootfs.squashfs: [4968KB/5120KB]
- Build time: 06:05
Copying files to local archive

Assembled firmware available in:
/mnt/IOTA/DATA/proj/builder/archive/gk7205v210_lite_xm-ivg-g3s/202405161511
├── openipc.gk7205v210-nor-lite.tgz
├── rootfs.gk7205v210.tar
├── rootfs.squashfs.gk7205v210
└── uImage.gk7205v210
```

