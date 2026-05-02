sudo apt-get update
sudo apt-get install -y xorriso rsync syslinux-common syslinux-utils

sudo mkdir -p /mnt/kaliiso
sudo mount -o loop /path/to/your-kali.iso /mnt/kaliiso

chmod +x ~/Sentinel/sentinel-build/*.sh
sudo ~/Sentinel/sentinel-build/merge-binary-payload-from-iso.sh /mnt/kaliiso ~/Sentinel
sudo umount /mnt/kaliiso

if already a folder 

chmod +x ~/Sentinel/sentinel-build/*.sh
sudo ~/Sentinel/sentinel-build/merge-binary-payload-from-iso.sh /path/to/extracted-iso ~/Sentinel


sudo ~/Sentinel/sentinel-build/04-regenerate-md5sum.sh ~/Sentinel
sudo ~/Sentinel/sentinel-build/build-bootable-iso.sh ~/Sentinel ~/sentinel-os-1-amd64.iso


sudo ~/Sentinel/sentinel-build/build-bootable-iso.sh ~/Sentinel ~/sentinel-os-1-amd64.iso

