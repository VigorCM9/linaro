linaro-4.7
=================================
Instructions:
-------------
* Download the Android source code you wish to use

* cd [aosp-root]/prebuilts/gcc/linux-x86
* git clone git://github.com/IAmTheOneTheyCallNeo/linaro.git linaro
* cd [aosp-root]/build

* edit envsetup.sh to point to your new Linaro toolchain

        export ARM_EABI_TOOLCHAIN=
        case $ARCH in
            arm) toolchaindir=linaro/bin
                ;;
            *)

* Build AOSP as normal

To use as a cross-compiler for kernel building:
-----------
find . -name "*gold"
If no files found it may be pre-patched otherwise run the following:

cp ./bin/arm-linux-androideabi-ld.bfd ./bin/arm-linux-androideabi-ld
cp ./bin/arm-eabi-ld.bfd ./bin/arm-eabi-ld
cp ./arm-eabi/bin/ld.bfd ./arm-eabi/bin/ld
cp ./arm-linux-androideabi/bin/ld.bfd ./arm-linux-androideabi/bin/ld

Disclaimer:
-----------
Neither linaro.org or myself are responsible for failed builds or bricked devices. Use this toolchain at your own risk. Be smart and make a backup.

