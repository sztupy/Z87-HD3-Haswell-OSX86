# Z87-HD3-Haswell-OSX86

Haswell OSX86 config for Z87-HD3 supporting OSX 11.5 Sequoia

Prepared using the official OpenCore guide for Haswell, including relevant fixes

Supports:
* NAVI 21 based AMD Radeon GPU (RX6900 XT)
* All USB 2&3 headers on the motherboard
* Dual-boot with Windows using rEFInd to avoid issues related to SSDT patches
* Ethernet
* Sound (ALC892)

## Installation

Use the OpenCore EFI folder provided in the `EFI_INSTALL` directory. This allows the installation be successful but is missing most of the kexts for proper operation. However some of those kexts seem to prevent installation as the installer would enter a reset-loop on the 3rd stage.

Note: you might also need to clear your NVRAM before the first install

## Post-install

Install the EFI setup in `EFI_FINAL` into your local drive's EFI folder. This includes the rest of the fixes. Make sure to change the volume UUID for your Windows installation in the rEFInd config file.
