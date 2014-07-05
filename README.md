roomservice.xml for experimental cm-11 for thunderc

to build:

init androidarmv6 repo

directions here

https://github.com/androidarmv6/android

cd to your androidarmv6 directory, then

git clone https://github.com/bigsupersquid/android_roomservice.git .repo/local_manifests/ -b cm-11.0

then repo sync.

. build/envsetup.sh

lunch internal_cm_thunderc-userdebug

or

lunch os2sd_cm_thunderc-userdebug


then

cd device/lge/thunderc && . version.sh <int or sd> && cd ../../..

and

time mka bacon

(mka instead of make -j* will supposedly optimize the number of threads based on your cpu, and then time will display total time when it finishes your build.)
