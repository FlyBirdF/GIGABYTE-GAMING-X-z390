# GIGABYTE-GAMING-X-z390-Hackintosh
hackintosh Gigabyte Gaming X z390 i5-9600k with OpenCore0.5.7


## Hardware
|HardWare Type|Model|
| :----:| :----:|
|Motherboard|Gigabyte Gaming X|
|CPU|i5 9600k|
|GPU|Intel UHD 630|
|Memory|CORSAIR VENGEANCE® LPX 2x8GB DDR4 2666MHz|
|Network card|motherboard builtin|


## Long Time Update
** update 2020/04/07 **
------------------------------
### Guide Version
[OpenCore](https://github.com/acidanthera/OpenCorePkg/releases) 0.5.7

### Install Guide
[Step By Step](https://khronokernel-2.gitbook.io/opencore-vanilla-desktop-guide/intel-config.plist/coffee-lake),reference from  OpenCore Vanilla Guide --- Coffee Lake

### Tips
1. My display port type is HDMI which built in motherboard. Please delete config.plist `DeviceProperties -> Add -> framebuffer-con*`, if your display type is DP. More info about [iGPU patching](https://1revenger1.gitbook.io/laptop-guide/prepare-install-macos/display-configuration#intel-coffee-lake-comet-lake-14-nm).
2. You need to add `-v` args in `boot-args` for checking the verbose info.
3. Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS): For generating your SMBIOS.


