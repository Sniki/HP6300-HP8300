# HP6300-HP8300

HP 6300 and HP 8300 (all form factors) using OpenCore Bootloader

### Supported models:
- HP 6300 Pro
- HP 6300 SFF
- HP Elite 8300 Tower
- HP Elite 8300 SFF
- HP Elite 8300 USDT/CMT

**Note**: this is still in experimental stage (in terms of full support for older macOS versions and Dedicated GPU users, for now only compatible with "MacPro6,1" SMBIOS specifically for users with HD4000 that want to upgrade to Big Sur.

### What works:
- Secure Boot
- FileVault
- Sleep and Wake
- Audio
- Power Management
- USB Ports
- LAN
- DisplayPort and DisplayPort Audio

### Issues:
- DRM content
- VGA Port

### Before testing:
1. Generate your SMBIOS values (Serial, MLB, Rom and UUID) to have working iServices
2. Replace EFI/OC/ACPI/ SSDT.aml with your generated Power Management SSDT from the script.
(This one is for the i7-3770 CPU model that is available on my machine).

Work in progress...
