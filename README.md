linaro-4.7
=================================
Instructions:
-------------
* Download the Android source code you wish to use

* cd [aosp-root]/prebuilts/gcc/linux-x86
* git clone -b 13.01 git://github.com/VigorCM9/linaro.git linaro
* cd [aosp-root]/build

* edit envsetup.sh to point to your new Linaro toolchain

        export ARM_EABI_TOOLCHAIN=
        case $ARCH in
            arm) toolchaindir=linaro/bin
                ;;
            *)

Do the same also for Android-eabi's arm (kernel): arm) toolchaindir=linaro/bin 
* Build AOSP as normal 

Disclaimer:
-----------
Neither linaro.org or myself are responsible for failed builds or bricked devices. Use this toolchain at your own risk. Be smart and make a backup.
