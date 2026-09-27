# Pissarro-TWRP
There are many faulty images of TWRP out there that are shared for Pissarro. This provides proper images.
I already shared these on some platforms but GitHub is more organized.

- Android 13+ (MIUI & HyperOS)
- Removed AVB and Forced Encryption (fixes dm-verity corruption)
- Pre-built an Android 13 boot image with TWRP so you won't encounter the nonsense I encountered
- Prebuilt image is for stock ROMs (or stock based ROMs) only; you can try raw TWRP image on your custom kernel
- In releases: boot.img is prebuilt kernel, twrp-raw is TWRP ramdisk only

# Device List
- Redmi Note 11 Pro+ 5G
- Redmi Note 11 Pro
- Redmi Note 11 Pro+
- Xiaomi 11i
- Xiaomi 11i Hypercharge

# Tips
- Always use stock vbmeta images. Pissarro's LK doesn't accept custom vbmeta images.
- As you may noticed there are no recovery partition for Pissarro, it's in the boot image.
- Do not flash Magisk or APatch from recovery. Always patch image from app and flash from fastboot.

# Warning
Even if this solves the AVB and Forced Encryption problem, your ROM will still throw dm-verity corruption error. That's because you also need to disable AVB and Forced Encryption in your super.img which can be done by RO2RW and DFE NEO script.
