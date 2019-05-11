# Resurrection Remix 5.8.5 device tree for CUBOT DINOSAUR 

CUBOT DINOSAUR
==============

Basic   | Spec Sheet
-------:|:-------------------------
CPU     | 1.3GHz Quad-Core MT6735A
GPU     | Mali-T720
Memory  | 3GB RAM
Shipped Android Version | 6.0
Storage | 16GB
Battery | 4150 mAh
Display | 5.5" 720 x 1280 px
Camera  | Front: 5.0MPx, Back 13MPx, LED Flash

![DEXP](https://github.com/h0sch180/android_device_cubot_dinosaur/blob/cm-14.1/cubot_dinosaur.jpg "Cubot Dinosaur")

# Instructions
```
repo init -u https://github.com/ResurrectionRemix/platform_manifest.git -b nougat
repo sync -f --force-sync --no-clone-bundle
git https://github.com/h0sch180/android_device_cubot_dinosaur.git -b rr-5.8.5 device/CUBOT/DINOSAUR
device/CUBOT/DINOSAUR/patches_mtk/apply-patches.sh
. build/envsetup.sh
export JACK_SERVER_VM_ARGUMENTS="-Dfile.encoding=UTF-8 -XX:+TieredCompilation -Xmx8g"
./prebuilts/sdk/tools/jack-admin kill-server
./prebuilts/sdk/tools/jack-admin start-server
brunch DINOSAUR
```

# Acknowledgements

* seluce
* iodine71
* olegsvs
* danielhk
* Zormax
* xcore995
* SRTK
* and others I might have forgotten to include
