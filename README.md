# HP6300-HP8300

HP 6300 and HP 8300 (all form factors) using OpenCore Bootloader

### Supported models:
- HP 6300 Pro
- HP 6300 SFF
- HP Elite 8300 CMT
- HP Elite 8300 SFF
- HP Elite 8300 USDT

**Note**: this is still work in progress !
For now it is only available for users with Intel HD 4000 Graphics that want to upgrade to Big Sur.
MacPro6,1 is the last supported Ivy Bridge model and that is the SMBIOS we used here.
Will be updated soon with < Catalina support and for Dedicated GPU users as well.


### What works:
- Secure Boot
- FileVault
- Sleep and Wake
- Audio
- Power Management
- USB Ports
- LAN
- DisplayPort and DisplayPort Audio
- Serial Port

### Issues:
- DRM content
- VGA Port

### Before testing:
1. Generate your SMBIOS values (Serial, MLB, Rom and UUID) to have working iServices
2. Replace EFI/OC/ACPI/ SSDT.aml with your generated Power Management SSDT from the script.
(This one is for the i7-3770 CPU model that is available on my machine).

### Work in progress...
