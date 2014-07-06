roomservice.xml for experimental cm-11 for thunderc

to build:

init androidarmv6 repo

directions here: https://github.com/androidarmv6/android

cd to your androidarmv6 directory, then


git clone https://github.com/bigsupersquid/android_roomservice.git .repo/local_manifests/ -b cm-11.0


then


repo sync

. build/envsetup.sh


then


. build/version.sh int

(for internal build, or)


. build/version.sh sd

(for os2sd build.)


and then


time mka bacon


(mka instead of make -j* will supposedly optimize the number of threads based on your cpu, and then time will display total time when it finishes your build.)

output zip in out/target/product/thunderc
