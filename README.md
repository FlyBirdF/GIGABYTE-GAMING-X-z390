# GIGABYTE-GAMING-X-z390-Hackintosh
hackintosh Gigabyte Gaming X z390 i5-9600k with OpenCore0.5.7
use matherboard hdmi

## Hardware
|HardWare Type|Model|
| :----:| :----:|
|Motherboard|Gigabyte Gaming X|
|CPU|i5 9600k|
|GPU|Intel UHD 630|
|Memory|CORSAIR VENGEANCE® LPX 2x8GB DDR4 2666MHz|
|Network card|Intel I219V7 PCI Express Gigabit Ethernet|
|Wireless device|FV-T919 BCM94360|


## Long Time Update


update 2020/04/12 Verfying in Catalina 10.15.4
------------------------------
### Update
- add `SMCProcessor.kext` and `SMCSuperIO.kext`
- remove all logs output (`Misc-->Debug-->AppleDebug` set to `NO`, `Misc-->Debug-->DisplayLevel` set to `0`)

### Your BIOS settings (version F7)
**Disable:**
- Fast Boot
- VT-d(can be enabled if you set **DisableIoMapper** to **YES**)
- CSM
- Intel SGX
- Intel Platform Trust
- CFG Lock(MSR 0xE2 write protection)

**Enable:**
- Above 4G decoding
- Hyper-Threading(if your cpu supported)
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10
- DVMT Pre-Allocated(iGPU Memory): 64MB

### Working
- Audio (Onboard)
- Video output with HDMI
- USB3.x bus
- Ethernet
- APFS
- Handoff
- Bluetooth & WIFI
- Airdrop
- Airplay

### Not working
- Sleep/Wake

### Not yet tested
- FileVault


### Another tips
1. If you used **Clover** to boot the system in the past, please clean the NVRAM before boot.
2. Check your BIOS settings, please set default if necessary.


update 2020/04/08 Verfying in Catalina 10.15.4
------------------------------
### Guide Version
[OpenCore](https://github.com/acidanthera/OpenCorePkg/releases) 0.5.7

### Install Guide
[Step By Step](https://khronokernel-2.gitbook.io/opencore-vanilla-desktop-guide/intel-config.plist/coffee-lake),reference from  OpenCore Vanilla Guide --- Coffee Lake

### Tips
1. My display port type is HDMI which built in motherboard. Please delete config.plist `DeviceProperties -> Add -> framebuffer-con*`, if your display type is DP. More info about [iGPU patching](https://1revenger1.gitbook.io/laptop-guide/prepare-install-macos/display-configuration#intel-coffee-lake-comet-lake-14-nm).
2. You need to add `-v` args in `boot-args` for checking the verbose info.
3. Use [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS): For generating your SMBIOS.


