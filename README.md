# HP6300-HP8300

[![macOS](https://img.shields.io/badge/macOS-Big_Sur_11.0.1-green)](https://www.apple.com/macos/big-sur/)
[![OpenCore](https://img.shields.io/badge/OpenCore-0.6.3-green)](https://github.com/acidanthera/OpenCorePkg)

HP 6300 and HP 8300 (all form factors) using OpenCore Bootloader

### Supported models:
- HP 6300 Pro MT
- HP 6300 Pro SFF
- HP Elite 8300 CMT
- HP Elite 8300 SFF
- HP Elite 8300 USDT

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

### What doesn't work:
- DRM content on macOS Big Sur
- VGA Port

### SMBIOS Choices:
1. If you are using Intel HD4000 Graphics only: `MacPro6,1` for macOS Big Sur
2. If you are using Intel HD4000 Gprahics only: `Macmini6,1` or `iMac13,2` for macOS Catalina and below
3. If you are using a Dedicated GPU: `iMacPro1,1` or `iMac13,2`

To change the SMBIOS go to `EFI/OC/Config.plist > PlatformInfo > Generic > SystemProductName`
Refer to SMBIOS Choices to pick the correct SMBIOS choice that fits your needs.

### Before testing:
1. Generate your SMBIOS values (Serial, MLB, Rom and UUID) to have working iServices
2. Replace `EFI/OC/ACPI/SSDT.aml` with your generated Power Management SSDT from the script.
(This one is for the i7-3770 CPU model that is available on my machine).
3. Dedicated GPU users have to remove `EFI/OC/Config.plist > DeviceProperties > PciRoot(0x0)/Pci(0x2,0x0)` entry.

**Note**: this is still work in progress !
