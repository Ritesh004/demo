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

ritesh@ubuntu:~/Downloads/Sentinel-OS-main$ chmod +x sentinel-live-main/sentinel-live-main/build.sh 
ritesh@ubuntu:~/Downloads/Sentinel-OS-main$ ./sentinel-build.sh
ERROR: You need live-build (>= 1:20250225+kali3), you have 3.0~a57-1ubuntu49.1
