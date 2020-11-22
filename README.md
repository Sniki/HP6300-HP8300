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
2. If you are using Intel HD4000 Graphics only: `Macmini6,1` or `iMac13,2` for macOS Catalina and below
3. If you are using a Dedicated GPU: `iMacPro1,1` or even `MacPro6,1` for macOS Big Sur
4. if you are using a Dedicated GPU: `iMac13,2` for macOS Catalina and below
**Note:**Dedicated GPU users have to remove `EFI/OC/Config.plist > DeviceProperties > PciRoot(0x0)/Pci(0x2,0x0)` entry.

To change the SMBIOS go to `EFI/OC/Config.plist > PlatformInfo > Generic > SystemProductName`
Refer to SMBIOS Choices to pick the correct SMBIOS choice that fits your needs.

### SMBIOS
In order to have working iServices, generate your own SMBIOS values like:
- Serial Number 
- MLB (Board Serial Number)
- ROM
- UUID
Refer to SMBIOS Choices to pick the correct SMBIOS choice that fits your needs.
To change SMBIOS go to `EFI/OC/Config.plist > PlatformInfo > Generic > SystemProductName`

### Power Management
1. The included `EFI/OC/ACPI/SSDT.aml` is for Intel Core i7-3770 CPU which is the one that my HP Desktop does have.
If you have same CPU model on your HP machine, you are good to go, nothing is needed to be done.
2. If you have different CPU, grab and copy your `SSDT.aml` that you previously generated that you currently use with Clover or OpenCore and paste it into `EFI/OC/ACPI/` to replace the one i provided so you have Power Management for your CPU Model.

### **Note**: this is still work in progress !
