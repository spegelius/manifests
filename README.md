manifests
=========

Manifests for different ROMS

to init CM11 for jactiveltexx:

repo init -u git://github.com/CyanogenMod/android.git -b cm-11.0
mkdir .repo/local_manifests
wget https://raw.github.com/spegelius/manifests/cm-11.0-official/roomservice.xml -O .repo/local_manifests/roomservice.xml
repo sync
