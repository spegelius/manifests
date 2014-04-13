manifests
=========

Manifests for different ROMS

to init SlimKat 4.4 for jactiveltexx:

repo init -u git://github.com/SlimRoms/platform_manifest.git -b kk4.4-caf
mkdir .repo/local_manifests
wget https://raw.github.com/spegelius/manifests/slim_kk4.4/roomservice.xml -O .repo/local_manifests/roomservice.xml
repo sync

