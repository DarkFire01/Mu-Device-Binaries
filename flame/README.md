## Firmware Info

- Device: Google Pixel 4
- Region: Global
- Version: `QD1A.190821.007` / bootloader `c2f2-0.2-5799621`

## Patches/Fixes

### ButtonsDxe:

- Reason: Helps navigating Menus (e.g. UEFI Menu).
- Patch: Key code was patched for the power button to be mapped as ENTER instead of SUSPEND. Same site as the cepheus patch.

### DALSYSDxe:

- Reason: To avoid Mismatched Cached Copies.
- Patch: Enabled Cache Coherence for UFS. Same table entry as the cepheus patch, 8 bytes earlier in this build.

### UsbConfigDxe:

- Reason: To Make USB Usable in the OS.
- Patch: Removed USB Deinit from Exit Boot Services. Same two branches as the cepheus patch, at 0x48F4 and 0x4950 in this build.

### UsbMsdDxe:

- Reason: To Make Device Non-Removeable in Mass Storage.
- Patch: Changed Removable State to Non-Removable. Same site as the mh2 patch.

### uefipil.cfg:

- Reason: The stock config auto loads ABL.
- Patch: ABL is commented out in the AUTO list.
