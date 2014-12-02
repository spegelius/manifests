I9295 MultiROM
==============

Multirom and TWRP originally from https://github.com/Tasssadar

to init CM11 multirom tree for jactiveltexx:

1. Init CM11 tree and local manifest
- repo init -u git://github.com/CyanogenMod/android.git -b cm-11.0
- cd .repo
- git clone https://github.com/spegelius/manifests.git local_manifests
- cd local_manifests
- git checkout cm-11.0-multirom
- cd ..

2. Sync tree
- cd .repo
- edit manifest.xml and remove/disable project bootable/recovery
- cd ..
- repo sync

2. Edit system/core/rootdir/init.environ.rc.in
- make LD_LIBRARY_PATH like this:
  export LD_LIBRARY_PATH /vendor/lib:/system/lib:.:/sbin

3. Get multirom submodules
- cd system/extras/multirom
- git submodule init
- git submodule update

4. Build
- lunch cm_jactivelte-userdebug
- make -jx multirom trampoline
- make -jx multirom_zip
