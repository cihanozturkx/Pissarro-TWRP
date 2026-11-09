# Pissarro-TWRP
- Android 13+ (MIUI & HyperOS)
- Fixed dm-verity corruption
- Removed AVB and encryption

# Chronic problem with this device
- LK image has hardcoded verifications; you need to use a custom LK.img (like Kaeru) and preloader or use RO2RW and DFE NEO to bypass dm-verity corruption and softbricks.
- My personal suggestion is use RO2RW and DFE NEO to remove AVB and encryption from both boot.img and super.img

# Installation on stock ROMs
- Always use **stock vbmeta images**. Stock LK doesn't accept custom vbmeta images.
- Download boot.img
- fastboot flash boot_ab boot.img
- Use RO2RW and DFE to disable AVB and encryption in your super.img
- Format data
- Done

# Installation on custom ROMs and on a kernel that already includes TWRP/OFOX
- Download twrp-raw image
- From recovery choose - install ramdisk
- You may still need to disable encryption in your ROM (haven't tested)

# Device List
- Redmi Note 11 Pro+ 5G
- Redmi Note 11 Pro
- Redmi Note 11 Pro+
- Xiaomi 11i
- Xiaomi 11i Hypercharge

# Tips
- As you may noticed there are no recovery partition for Pissarro, it's in the boot image.
- Do not flash Magisk or APatch from recovery. Always patch image from app and flash from fastboot.
