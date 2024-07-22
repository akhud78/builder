## Devices

### List of known and supported devices

```
YUCHENG  F10H55W3AS      GK7205V300  IMX335  MT7601U_USB    NOR_16M   in progress
YUCHENG  F10H55W3AS-DEV  GK7205V300  IMX335  MT7601U_USB    NOR_16M   in progress
XM       IVG-HP203Y-AE   HI3516CV300 IMX291                 NOR_16M   in progress
AKA      CH v1           GK7205V200  IMX307  RTL8733BU      NOR_16M   in progress
AKA      CH v2           GK7205V200  IMX307  MT7601U_USB    NOR_16M   in progress
AKA      CH-T31 v1       T31L        GC2083  MT7601U_USB    NOR_8M    in progress
AKA      CH-T31 v2       T31L        GC2083  RTL8188EU_USB  NOR_8M    in progress
XM       IVG-G3S         GK7205V210  IMX307  ATBM6032i_USB  NOR_16M   w/ext wifi board
```
### Links
- [releases](https://github.com/akhud78/builder/releases)
- [firmware](https://github.com/OpenIPC/firmware)
- [majestic-webui](https://github.com/OpenIPC/majestic-webui)


### Upgrading
- [Upgrading firmware](https://github.com/OpenIPC/wiki/blob/master/en/sysupgrade.md)
- SD
```
# soc=$(fw_printenv -n soc)
# sysupgrade --kernel=/mnt/mmcblk0p1/uImage.${soc} --rootfs=/mnt/mmcblk0p1/rootfs.squashfs.${soc} -z --force_ver
...
# firstboot
```
- TFTP
```
# soc=$(fw_printenv -n soc)
# serverip=192.168.1.40
# cd /tmp
# tftp -r rootfs.squashfs.${soc} -g ${serverip}
# tftp -r uImage.${soc} -g ${serverip}
# sysupgrade --kernel=uImage.${soc} --rootfs=rootfs.squashfs.${soc} -z --force_ver
```

### Create a Permanent Storage for Downloaded Bundles
- Add to `~/.profile`
```
# OpenIPC
BR2_DL_DIR="${HOME}/buildroot_dl"
[ ! -d "$BR2_DL_DIR" ] && mkdir -p $BR2_DL_DIR
export BR2_DL_DIR
```
- Delete directory or replace archive to update package
- [Source code archive URLs](https://docs.github.com/en/repositories/working-with-files/using-files/downloading-source-code-archives#source-code-archive-urls) - how to download `tar.gz` archive

#### YUCHENG F10H55W3AS

- gk7205v300_ultimate_yucheng-f10h55w3as-nor.tgz
- Majestic: [master+5588001, 2024-06-02](https://t.me/openipc_dev/113457) - jpeg is OK
- WebUI: [majestic-webui-e2cacd9, 2024-06-03](https://github.com/OpenIPC/majestic-webui/archive/e2cacd982aff2fcf44e504edc53fb82c3a9aa30e.tar.gz) - `tar.gz` archive without visual_motion
- easy.cgi: Build: Jul  4 2024 @ 14:17:41
- packages: gesftpserver, qrparse

`$ ./builder.sh gk7205v300_ultimate_yucheng-f10h55w3as`

```
- uImage: [1816KB/2048KB]
- rootfs.squashfs: [6288KB/8192KB]
- builder/archive/gk7205v300_ultimate_yucheng-f10h55w3as/202407060909
```

#### YUCHENG F10H55W3AS-DEV

- gk7205v300_ultimate_yucheng-f10h55w3as-dev-nor.tgz
- Majestic: master+5588001, 2024-06-02
- WebUI: majestic-webui-e2cacd9
- easy.cgi: Build: Jul  4 2024 @ 14:17:41
- packages: gesftpserver, opencv3 + objdetect

`$ ./builder.sh gk7205v300_ultimate_yucheng-f10h55w3as-dev`

```
- uImage: [1855KB/2048KB]
- rootfs.squashfs: [7752KB/8192KB]
- archive/gk7205v300_ultimate_yucheng-f10h55w3as-dev/202407191536

- uImage: [1855KB/2048KB]
- rootfs.squashfs: [7644KB/8192KB]
- archive/gk7205v300_ultimate_yucheng-f10h55w3as-dev/202407060945
```

#### XM IVG-HP203Y-AE

- hi3516cv300_ultimate_xm-ivg-hp203y-ae-nor.tgz
- Majestic: [master+5588001, 2024-06-02](https://t.me/openipc_dev/113461)
- packages: gesftpserver, opencv3

`./builder.sh hi3516cv300_ultimate_xm_ivg_hp203y_ae`

```
- uImage: [1728KB/2048KB]
- rootfs.squashfs: [7544KB/8192KB]
- archive/hi3516cv300_ultimate_xm_ivg_hp203y_ae/202407091755
```

#### AKA CH v1
```
- uImage: [1814KB/2048KB]
- rootfs.squashfs: [5080KB/5120KB]
- archive/gk7205v200_lite_aka-ch-v1/202405231116
```
#### AKA CH v2

- ngrep, mdns, mquery, gesftpserver, qrparse, easy.cgi, ethaddr

`$ ./builder.sh gk7205v200_lite_aka-ch-v2`

```
- uImage: [1814KB/2048KB]
- rootfs.squashfs: [4792KB/5120KB]
- archive/gk7205v200_lite_aka-ch-v2/202407021724
```
#### AKA CH-T31 v1
```
- uImage: [1786KB/2048KB]
- rootfs.squashfs: [4384KB/5120KB]
- archive/t31_lite_aka-ch-v1/202405211035
```
#### AKA CH-T31 v2
```
- uImage: [1786KB/2048KB]
- rootfs.squashfs: [5064KB/5120KB]
- archive/t31_lite_aka-ch-v2/202405211318
```
#### XM IVG-G3S
- gk7205v210_lite_xm-ivg-g3s-nor.tgz
```
- uImage: [1814KB/2048KB]
- rootfs.squashfs: [4968KB/5120KB]
- archive/gk7205v210_lite_xm-ivg-g3s/202405281200
```


