Philz_Touch_Recovery_CN
=======================

汉化版PhilzTouch 添加MT6592支持
#### Building
__Home page__
手机之家首发 酷派大神F2（8675） Philz Touch Recovery 6.56.2 全触控 汉化版
http://lt.imobile.com.cn/thread-10614983-1-1.html


参考 https://github.com/X-s/android_bootable_recovery
感谢@X-s大神的MTK备份信息 感谢@xiaolu大神的字库文件 感谢@cyanogenmod的核心源码 感谢@philz-cwm6的philztouch源码

如要MTK支持:
Boardconfig.mk加入
BOARD_RECOVERY_MTK := true

Clone philz recovery to bootable/recovery-philz folder

    git clone https://github.com/Mr-zeng/Philz_Touch_Recovery_CN bootable/recovery-philz -b cm-11.0
    
    

If you haven't build recovery ever before, please look up the thread linked above.
If you regularly build ROMs/Recoveries for your device, and have a working CWM setup
on your build machine, then you can quickly set up and build Philz Touch recovery as well

Check these two patches are present in your build/ directory
   1. https://github.com/CyanogenMod/android_build/commit/c1b0bb6
   2. https://github.com/CyanogenMod/android_build/commit/6b21727

Clone philz recovery to bootable/recovery-philz folder

    git clone https://github.com/PhilZ-cwm6/philz_touch_cwm6 bootable/recovery-philz -b cm-11.0

Now build with RECOVERY_VARIANT flag set to philz.

    . build/envsetup.sh && lunch && make -j8 recoveryimage RECOVERY_VARIANT=philz

or

    export RECOVERY_VARIANT=philz
    . build/envsetup.sh && lunch && make -j8 recoveryimage
