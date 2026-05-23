## Recovery Device Tree for the Samsung Galaxy A13 - SM-A137F (MTK) - TESTING

Forked from the device tree ((Original edward0181 device repository)[https://github.com/edward0181/android_device_samsung_a13ve]) that yall waited. I will add FBE.

## How-to compile it:

# Create dirs
$ mkdir tw; cd tw

# Init repo
$ repo init --depth=1 -u https://github.com/minimal-manifest-twrp/platform_manifest_twrp_aosp.git -b twrp-12

# Clone a13ve repo
$ git clone https://github.com/thereaLabji/a13ve_fbe_twrpdevicetree device/samsung/a13ve

# Clone a13ve kernel
$ git clone https://github.com/edward0181/android_kernel_samsung_a13ve kernel/samsung/a13ve

# Sync
$ repo sync  -f --force-sync --no-clone-bundle --no-tags -j$(nproc --all)

# Build
$ source build/envsetup.sh; export ALLOW_MISSING_DEPENDENCIES=true; lunch twrp_a13ve-eng; mka recoveryimage

# Extra
$ Work In Progress, will add FBE (test if worked)

