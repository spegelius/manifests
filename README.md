manifests
=========

Manifests for different ROMS

to init CM11 multirom tree for jactiveltexx:

repo init -u git://github.com/CyanogenMod/android.git -b cm-11.0
mkdir .repo/local_manifests
wget https://raw.github.com/spegelius/manifests/cm-11.0-multirom/local_manifest.xml -O .repo/local_manifests/local_manifest.xml
repo sync
