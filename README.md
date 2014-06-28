roomservice.xml for experimental cm-11 for thunderc

to build:
init androidarmv6 repo

directions here
https://github.com/androidarmv6/android

cd to your androidarmv6 directory, then
git clone https://github.com/bigsupersquid/android_roomservice.git .repo/local_manifests/ -b cm-11.0

then repo sync.

. build/envsetup.sh
lunch cm_thunderc-userdebug
cd device/lge/thunderc

then, for internal version
. version.sh int

or for os2sd version
. version.sh sd

then
time mka bacon

this will supposedly optimize the number of threads, and then display total time when it finishes your build.
