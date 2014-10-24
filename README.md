roomservice.xml for experimental cm-11 for thunderc ("stable" repo)
(https://github.com/bigsupersquid/android_roomservice.git is definitely unstable)

to build:

init androidarmv6 repo

directions here: https://github.com/androidarmv6/android

cd to your androidarmv6 directory, then


git clone https://github.com/bigsuperstuff/android_roomservice.git .repo/local_manifests/ -b cm-11.0


then


repo sync

. build/envsetup.sh


then

//needs fixed: currently going to build for whatever version I'm building

. build/version.sh int

(for internal build, or)


. build/version.sh sd

(for os2sd build.)

//end needs fixed

and then


lunch cm_thunderc-userdebug

time mka bacon


(mka instead of make -j* will supposedly optimize the number of threads based on your cpu, and then time will display total time when it finishes your build.)

output zip in out/target/product/thunderc
