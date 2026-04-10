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


ritesh@ubuntu:~/Downloads/Sentinel-OS-main$ ./sentinel-build.sh
[sudo] password for ritesh: 
Build of kali-rolling/minimal/amd64 live image failed (see build.log for details)
Log: /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log
ritesh@ubuntu:~/Downloads/Sentinel-OS-main$ /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log
bash: /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log: Permission denied
ritesh@ubuntu:~/Downloads/Sentinel-OS-main$ cat /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log
[2026-04-11 02:12:47] lb_clean --purge
P: Cleaning chroot
[2026-04-11 02:12:48] lb_config -a amd64 --distribution kali-rolling -- --variant minimal
P: Considering defaults defined in /etc/live/build.conf
W: You have specified a value of LB_ISO_VOLUME that is too long; the maximum length is 32 characters.
P: Updating config tree for a ubuntu/amd64 system
W: You have specified a value of LB_ISO_VOLUME that is too long; the maximum length is 32 characters.
[2026-04-11 02:12:48] lb_build 
W: You have specified a value of LB_ISO_VOLUME that is too long; the maximum length is 32 characters.
[2026-04-11 02:12:49] lb_bootstrap 
P: Setting up cleanup function
[2026-04-11 02:12:49] lb_bootstrap_cache restore
P: Restoring bootstrap stage from cache...
[2026-04-11 02:12:49] lb_bootstrap_copy 
[2026-04-11 02:12:49] lb_bootstrap_cdebootstrap 
[2026-04-11 02:12:49] lb_bootstrap_debootstrap 
P: Begin bootstrapping system...
[2026-04-11 02:12:50] lb_testroot 
P: If the following stage fails, the most likely cause of the problem is with your mirror configuration or a caching proxy.
P: Running debootstrap (download-only)... 
W: Cannot check Release signature; keyring file not available /usr/share/keyrings/kali-archive-keyring.gpg
I: Retrieving InRelease 
I: Retrieving Release 
E: Failed getting release file http://archive.ubuntu.com/ubuntu/dists/kali-rolling/Release
P: Begin unmounting filesystems...
P: Saving caches...
chroot: failed to run command ‘/usr/bin/env’: No such file or directory
ritesh@ubuntu:~/Downloads/Sentinel-OS-main$ 


