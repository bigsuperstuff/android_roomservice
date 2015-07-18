roomservice.xml for experimental cm-11 for thunderc ("stable" repo)
(https://github.com/bigsupersquid/android_roomservice.git is definitely unstable)

to build:

init <R.I.P androidarmv6> repo

Building android from source code

$ mkdir WORKING_DIR
$ cd WORKING_DIR
$ repo init -u git://github.com/bigsuperstuff/android.git -b cm-11.0
$ repo sync
$ sh vendor/cm/get-prebuilts
$ source build/envsetup.sh
$ lunch
$ 
$time mka bacon

(mka instead of make -j* will supposedly optimize the number of threads based on your cpu, and then time will display total time when it finishes your build.)
wait.

$ adb push out/target/product/DEVICENAME/cm-VERSION-DEVICENAME.zip /mnt/sdcard/
