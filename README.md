android-toolchain-eabi-linaro-4.7
=================================
Instructions:
-------------
* Download the Android source code you wish to use

* cd [aosp-root]/prebuilts/gcc/linux-x86/arm
* git clone git://github.com/mbobino/android-toolchain.git android-toolchain-eabi
* cd [aosp-root]/build

* edit envsetup.sh to point to your new Linaro toolchain

        export ANDROID_EABI_TOOLCHAIN=
        local ARCH=$(get_build_var TARGET_ARCH)
        case $ARCH in
            x86) toolchaindir=x86/i686-android-linux-4.4.3/bin
                ;;
            arm) toolchaindir=arm/android-toolchain-eabi/bin
                ;;
            *)

and

    export ARM_EABI_TOOLCHAIN=
    case $ARCH in
        x86) toolchaindir=x86/i686-eabi-4.4.3/bin
            ;;
        arm) toolchaindir=arm/android-toolchain-eabi/bin
            ;;
        *)

* Build AOSP as normal

Disclaimer:
-----------
Neither linaro.org nor I am not responsible for failed builds or bricked devices, use this toolchain at your own risk, be smart, and make a backup.
