[Android Open Source Dark Project]
====================================

![Photo](https://imgur.com/R0QIBwZ)

Download the Source
===================

Please read the [AOSP building instructions](http://source.android.com/source/index.html) before proceeding.

Initializing Repository
-----------------------

Initiate core trees without any device/kernel/vendor:

    $ repo init -u https://github.com/Android-Open-Source-Dark-Project/platform_manifest.git -b oreo

Sync the repository:

    $ repo sync --force-sync

***

Building
--------

After the sync is finished, please read the [instructions from the Android site](http://s.android.com/source/building.html) on how to build.

    . build/envsetup.sh
    lunch

You can also build for specific devices like this:

    . build/envsetup.sh
    lunch dark_<device codename>-userdebug
    brunch -j (add the number of your proccesor threads)

Remember to `make clobber && make clean` every now and then!
