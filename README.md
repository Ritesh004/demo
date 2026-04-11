xorriso -as mkisofs -o sentinel.iso -isohybrid-mbr /usr/lib/ISOLINUX/isohdpfx.bin -b boot/isolinux/isolinux.bin -c boot/isolinux/boot.cat -no-emul-boot -boot-load-size 4 -boot-info-table -eltorito-alt-boot -e boot/grub/efi.img -no-emul-boot -isohybrid-gpt-basdat -J -R /home/ritesh/Downloads/Sentinel-OS-main
xorriso 1.5.6 : RockRidge filesystem manipulator, libburnia project.

Drive current: -outdev 'stdio:sentinel.iso'
Media current: stdio file, overwriteable
Media status : is blank
Media summary: 0 sessions, 0 data blocks, 0 data, 49.1g free
Added to ISO image: directory '/'='/home/ritesh/Downloads/Sentinel-OS-main'
xorriso : UPDATE :     135 files added in 1 seconds
xorriso : FAILURE : Given path does not exist on disk: -boot_image system_area='/usr/lib/ISOLINUX/isohdpfx.bin'
xorriso : FAILURE : Cannot find in ISO image: -boot_image ... bin_path='/boot/isolinux/isolinux.bin'
xorriso : UPDATE :     135 files added in 1 seconds
xorriso : aborting : -abort_on 'FAILURE' encountered 'FAILURE'
ritesh@ubuntu:~$ 


cd /path/to/Sentinel-OS
sudo apt update
sudo apt install -y live-build debootstrap
chmod +x sentinel-build.sh
./sentinel-build.sh

chmod +x sentinel-live-main/sentinel-live-main/build.sh
./sentinel-build.sh


(http://http.kali.org/kali/pool/main/k/kali-archive-keyring/)
sudo dpkg -i kali-archive-keyring_*_all.deb

wget -qO- 'http://http.kali.org/kali/pool/main/k/kali-archive-keyring/' | grep -oP 'href="\Kkali-archive-keyring_[^"]+_all\.deb'

cd /path/to/Sentinel-OS/sentinel-live-main/sentinel-live-main

./sentinel-build.sh

ln -sf sid /usr/share/live/build/data/debian-cd/kali-rolling

ritesh@ubuntu:~/Downloads/Sentinel-OS-main$ ./sentinel-build.sh
[sudo] password for ritesh: 
mkdir: created directory '/home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/images/'
Build of kali-rolling/minimal/amd64 live image failed (see build.log for details)
Log: /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log
ritesh@ubuntu:~/Downloads/Sentinel-OS-main$ cat /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log
[2026-04-11 07:37:02] lb_clean --purge
P: Cleaning chroot
[2026-04-11 07:41:32] lb_config noauto --apt-indices=false --distribution kali-rolling --debian-installer-distribution kali-rolling --archive-areas main contrib non-free non-free-firmware --debootstrap-options --keyring=/usr/share/keyrings/kali-archive-keyring.gpg --keyring-packages kali-archive-keyring --updates false --backports false --source false --firmware-binary true --firmware-chroot true --mirror-bootstrap http://kali.download/kali --mirror-chroot http://kali.download/kali --mirror-debian-installer http://kali.download/kali --mirror-binary http://http.kali.org/kali --iso-application Sentinel OS --iso-publisher Sentinel --iso-volume Sentinel-Live --linux-packages linux-image --memtest memtest86+ --bootappend-live boot=live components noeject --bootappend-live-failsafe boot=live components noeject memtest noapic noapm nodma nomce nolapic nomodeset nosmp vga=normal --bootappend-install net.ifnames=0 --security false --win32-loader false --debian-installer live -a amd64
lb config: unrecognized option '--debootstrap-options'
lb config: unrecognized option '--updates'
lb config: unrecognized option '--bootappend-live-failsafe'
