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
┌──(ritesh㉿kali)-[~/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main]
└─$ cd /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log

cd: not a directory: /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log
                                                                             
┌──(ritesh㉿kali)-[~/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main]
└─$ cd ~
                                                                             
┌──(ritesh㉿kali)-[~]
└─$ cd /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log

cd: not a directory: /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log
                                                                             
┌──(ritesh㉿kali)-[~]
└─$ cat /home/ritesh/Downloads/Sentinel-OS-main/sentinel-live-main/sentinel-live-main/build.log

[2026-04-17 22:48:38] lb clean --purge
W: The auto/clean script exists but is not executable, ignoring.
P: Cleaning chroot
[2026-04-17 22:53:08] lb config noauto --apt-indices=false --distribution kali-rolling --debian-installer-distribution kali-rolling --archive-areas main contrib non-free non-free-firmware --keyring-packages kali-archive-keyring --backports false --source false --firmware-binary true --firmware-chroot true --mirror-bootstrap http://kali.download/kali --mirror-chroot http://kali.download/kali --mirror-debian-installer http://kali.download/kali --mirror-binary http://http.kali.org/kali --iso-application Sentinel OS --iso-publisher Sentinel --iso-volume Sentinel-Live --linux-packages linux-image --memtest memtest86+ --bootappend-live boot=live components noeject --bootappend-install net.ifnames=0 --security false --win32-loader false --debootstrap-options --keyring=/usr/share/keyrings/kali-archive-keyring.gpg --updates false --bootappend-live-failsafe boot=live components noeject memtest noapic noapm nodma nomce nolapic nomodeset nosmp vga=normal --debian-installer live -a amd64
P: Updating config tree for a debian/kali-rolling/amd64 system
P: Symlinking hooks...
[2026-04-17 22:53:09] lb build 
P: live-build 20250814+kali3
P: Building for a debian/kali-rolling/amd64 system
[2026-04-17 22:53:09] lb bootstrap 
P: Setting up clean exit handler
[2026-04-17 22:53:09] lb bootstrap_cache restore
[2026-04-17 22:53:09] lb bootstrap_debootstrap 
P: Begin bootstrapping system...
P: eatmydata found. It will be used do disable the sync command in the second stage of debootstrap
P: If the following stage fails, the most likely cause of the problem is with your mirror configuration or a caching proxy.
P: Running debootstrap (download-only)...
I: Retrieving InRelease 
I: Checking Release signature
I: Valid Release signature (key id 827C8569F2518CC677FECA1AED65462EC8D5E4C5)
I: Retrieving Packages 
I: Validating Packages 
I: Retrieving Packages 
I: Validating Packages 
I: Retrieving Packages 
I: Validating Packages 
I: Retrieving Packages 
I: Validating Packages 
I: Resolving dependencies of required packages...
I: Resolving dependencies of base packages...
I: Checking component main on http://kali.download/kali...
I: Retrieving adduser 3.154
I: Validating adduser 3.154
I: Retrieving apt 3.2.0+kali1
I: Validating apt 3.2.0+kali1
I: Retrieving apt-utils 3.2.0+kali1
I: Validating apt-utils 3.2.0+kali1
I: Retrieving base-files 1:2026.1.1
I: Validating base-files 1:2026.1.1
I: Retrieving base-passwd 3.6.8
I: Validating base-passwd 3.6.8
I: Retrieving bash 5.3-2
I: Validating bash 5.3-2
I: Retrieving bsdutils 1:2.41.3-4
I: Validating bsdutils 1:2.41.3-4
I: Retrieving coreutils 9.10-1
I: Validating coreutils 9.10-1
I: Retrieving cpio 2.15+dfsg-2.1
I: Validating cpio 2.15+dfsg-2.1
I: Retrieving cron 3.0pl1-207
I: Validating cron 3.0pl1-207
I: Retrieving cron-daemon-common 3.0pl1-207
I: Validating cron-daemon-common 3.0pl1-207
I: Retrieving dash 0.5.12-12
I: Validating dash 0.5.12-12
I: Retrieving debconf 1.5.92
I: Validating debconf 1.5.92
I: Retrieving debconf-i18n 1.5.92
W: Couldn't download package debconf-i18n (ver 1.5.92 arch all) at http://kali.download/kali/pool/main/d/debconf/debconf-i18n_1.5.92_all.deb
I: Retrieving debian-archive-keyring 2025.1
W: Couldn't download package debian-archive-keyring (ver 2025.1 arch all) at http://kali.download/kali/pool/main/d/debian-archive-keyring/debian-archive-keyring_2025.1_all.deb
I: Retrieving debianutils 5.23.2
W: Couldn't download package debianutils (ver 5.23.2 arch amd64) at http://kali.download/kali/pool/main/d/debianutils/debianutils_5.23.2_amd64.deb
I: Retrieving dhcpcd-base 1:10.3.1-1
W: Couldn't download package dhcpcd-base (ver 1:10.3.1-1 arch amd64) at http://kali.download/kali/pool/main/d/dhcpcd/dhcpcd-base_10.3.1-1_amd64.deb
I: Retrieving diffutils 1:3.12-1
W: Couldn't download package diffutils (ver 1:3.12-1 arch amd64) at http://kali.download/kali/pool/main/d/diffutils/diffutils_3.12-1_amd64.deb
I: Retrieving dmidecode 3.7-1
W: Couldn't download package dmidecode (ver 3.7-1 arch amd64) at http://kali.download/kali/pool/main/d/dmidecode/dmidecode_3.7-1_amd64.deb
I: Retrieving dpkg 1.23.7+kali1
W: Couldn't download package dpkg (ver 1.23.7+kali1 arch amd64) at http://kali.download/kali/pool/main/d/dpkg/dpkg_1.23.7+kali1_amd64.deb
I: Retrieving e2fsprogs 1.47.4-1
W: Couldn't download package e2fsprogs (ver 1.47.4-1 arch amd64) at http://kali.download/kali/pool/main/e/e2fsprogs/e2fsprogs_1.47.4-1_amd64.deb
I: Retrieving fdisk 2.41.3-4
W: Couldn't download package fdisk (ver 2.41.3-4 arch amd64) at http://kali.download/kali/pool/main/u/util-linux/fdisk_2.41.3-4_amd64.deb
I: Retrieving findutils 4.10.0-3
W: Couldn't download package findutils (ver 4.10.0-3 arch amd64) at http://kali.download/kali/pool/main/f/findutils/findutils_4.10.0-3_amd64.deb
I: Retrieving gcc-16-base 16-20260322-1
W: Couldn't download package gcc-16-base (ver 16-20260322-1 arch amd64) at http://kali.download/kali/pool/main/g/gcc-16/gcc-16-base_16-20260322-1_amd64.deb
I: Retrieving grep 3.12-1
W: Couldn't download package grep (ver 3.12-1 arch amd64) at http://kali.download/kali/pool/main/g/grep/grep_3.12-1_amd64.deb
I: Retrieving gzip 1.13-1
W: Couldn't download package gzip (ver 1.13-1 arch amd64) at http://kali.download/kali/pool/main/g/gzip/gzip_1.13-1_amd64.deb
I: Retrieving hostname 3.25
W: Couldn't download package hostname (ver 3.25 arch amd64) at http://kali.download/kali/pool/main/h/hostname/hostname_3.25_amd64.deb
I: Retrieving ifupdown 0.8.45
W: Couldn't download package ifupdown (ver 0.8.45 arch amd64) at http://kali.download/kali/pool/main/i/ifupdown/ifupdown_0.8.45_amd64.deb
I: Retrieving init 1.69+kali1
W: Couldn't download package init (ver 1.69+kali1 arch amd64) at http://kali.download/kali/pool/main/i/init-system-helpers/init_1.69+kali1_amd64.deb
I: Retrieving init-system-helpers 1.69+kali1
W: Couldn't download package init-system-helpers (ver 1.69+kali1 arch all) at http://kali.download/kali/pool/main/i/init-system-helpers/init-system-helpers_1.69+kali1_all.deb
I: Retrieving iproute2 6.19.0-1
W: Couldn't download package iproute2 (ver 6.19.0-1 arch amd64) at http://kali.download/kali/pool/main/i/iproute2/iproute2_6.19.0-1_amd64.deb
I: Retrieving iputils-ping 3:20250605-1
W: Couldn't download package iputils-ping (ver 3:20250605-1 arch amd64) at http://kali.download/kali/pool/main/i/iputils/iputils-ping_20250605-1_amd64.deb
I: Retrieving kali-archive-keyring 2025.2
W: Couldn't download package kali-archive-keyring (ver 2025.2 arch all) at http://kali.download/kali/pool/main/k/kali-archive-keyring/kali-archive-keyring_2025.2_all.deb
I: Retrieving kmod 34.2-2kali1
W: Couldn't download package kmod (ver 34.2-2kali1 arch amd64) at http://kali.download/kali/pool/main/k/kmod/kmod_34.2-2kali1_amd64.deb
I: Retrieving less 668-1
W: Couldn't download package less (ver 668-1 arch amd64) at http://kali.download/kali/pool/main/l/less/less_668-1_amd64.deb
I: Retrieving libacl1 2.3.2-3
W: Couldn't download package libacl1 (ver 2.3.2-3 arch amd64) at http://kali.download/kali/pool/main/a/acl/libacl1_2.3.2-3_amd64.deb
I: Retrieving libapt-pkg7.0 3.2.0+kali1
W: Couldn't download package libapt-pkg7.0 (ver 3.2.0+kali1 arch amd64) at http://kali.download/kali/pool/main/a/apt/libapt-pkg7.0_3.2.0+kali1_amd64.deb
I: Retrieving libattr1 1:2.5.2-4
W: Couldn't download package libattr1 (ver 1:2.5.2-4 arch amd64) at http://kali.download/kali/pool/main/a/attr/libattr1_2.5.2-4_amd64.deb
I: Retrieving libaudit-common 1:4.1.2-1
W: Couldn't download package libaudit-common (ver 1:4.1.2-1 arch all) at http://kali.download/kali/pool/main/a/audit/libaudit-common_4.1.2-1_all.deb
I: Retrieving libaudit1 1:4.1.2-1+b1
W: Couldn't download package libaudit1 (ver 1:4.1.2-1+b1 arch amd64) at http://kali.download/kali/pool/main/a/audit/libaudit1_4.1.2-1+b1_amd64.deb
I: Retrieving libblkid1 2.41.3-4
W: Couldn't download package libblkid1 (ver 2.41.3-4 arch amd64) at http://kali.download/kali/pool/main/u/util-linux/libblkid1_2.41.3-4_amd64.deb
I: Retrieving libbpf1 1:1.7.0-1
W: Couldn't download package libbpf1 (ver 1:1.7.0-1 arch amd64) at http://kali.download/kali/pool/main/libb/libbpf/libbpf1_1.7.0-1_amd64.deb
I: Retrieving libbsd0 0.12.2-2+b1
W: Couldn't download package libbsd0 (ver 0.12.2-2+b1 arch amd64) at http://kali.download/kali/pool/main/libb/libbsd/libbsd0_0.12.2-2+b1_amd64.deb
I: Retrieving libbz2-1.0 1.0.8-6+b1
I: Validating libbz2-1.0 1.0.8-6+b1
I: Retrieving libc-bin 2.42-13
I: Validating libc-bin 2.42-13
I: Retrieving libc-gconv-modules-extra 2.42-13
I: Validating libc-gconv-modules-extra 2.42-13
I: Retrieving libc6 2.42-13
I: Validating libc6 2.42-13
I: Retrieving libcap-ng0 0.9.2-1
I: Validating libcap-ng0 0.9.2-1
I: Retrieving libcap2 1:2.78-1
I: Validating libcap2 1:2.78-1
I: Retrieving libcap2-bin 1:2.78-1
I: Validating libcap2-bin 1:2.78-1
I: Retrieving libcom-err2 1.47.4-1
I: Validating libcom-err2 1.47.4-1
I: Retrieving libcrypt1 1:4.5.1-1+b1
I: Validating libcrypt1 1:4.5.1-1+b1
I: Retrieving libdb5.3t64 5.3.28+dfsg2-11+b1
I: Validating libdb5.3t64 5.3.28+dfsg2-11+b1
I: Retrieving libdebconfclient0 0.282+b2
I: Validating libdebconfclient0 0.282+b2
I: Retrieving libedit2 3.1-20251016-1
I: Validating libedit2 3.1-20251016-1
I: Retrieving libelf1t64 0.194-4
I: Validating libelf1t64 0.194-4
I: Retrieving libext2fs2t64 1.47.4-1
I: Validating libext2fs2t64 1.47.4-1
I: Retrieving libfdisk1 2.41.3-4
I: Validating libfdisk1 2.41.3-4
I: Retrieving libgcc-s1 16-20260322-1
I: Validating libgcc-s1 16-20260322-1
I: Retrieving libgmp10 2:6.3.0+dfsg-5+b1
I: Validating libgmp10 2:6.3.0+dfsg-5+b1
I: Retrieving libgssapi-krb5-2 1.22.1-2+b1
I: Validating libgssapi-krb5-2 1.22.1-2+b1
I: Retrieving libhogweed6t64 3.10.2-1+b1
I: Validating libhogweed6t64 3.10.2-1+b1
I: Retrieving libidn2-0 2.3.8-4+b1
I: Validating libidn2-0 2.3.8-4+b1
I: Retrieving libjansson4 2.14-2+b4
I: Validating libjansson4 2.14-2+b4
I: Retrieving libk5crypto3 1.22.1-2+b1
I: Validating libk5crypto3 1.22.1-2+b1
I: Retrieving libkeyutils1 1.6.3-6+b1
I: Validating libkeyutils1 1.6.3-6+b1
I: Retrieving libkmod2 34.2-2kali1
I: Validating libkmod2 34.2-2kali1
I: Retrieving libkrb5-3 1.22.1-2+b1
I: Validating libkrb5-3 1.22.1-2+b1
I: Retrieving libkrb5support0 1.22.1-2+b1
I: Validating libkrb5support0 1.22.1-2+b1
I: Retrieving liblocale-gettext-perl 1.07-8
I: Validating liblocale-gettext-perl 1.07-8
I: Retrieving liblz4-1 1.10.0-6
I: Validating liblz4-1 1.10.0-6
I: Retrieving liblzma5 5.8.2-2
I: Validating liblzma5 5.8.2-2
I: Retrieving libmd0 1.1.0-2+b2
I: Validating libmd0 1.1.0-2+b2
I: Retrieving libmnl0 1.0.5-3+b1
I: Validating libmnl0 1.0.5-3+b1
I: Retrieving libmount1 2.41.3-4
I: Validating libmount1 2.41.3-4
I: Retrieving libncursesw6 6.6+20251231-1
I: Validating libncursesw6 6.6+20251231-1
I: Retrieving libnettle8t64 3.10.2-1+b1
I: Validating libnettle8t64 3.10.2-1+b1
I: Retrieving libnewt0.52 0.52.25-2
I: Validating libnewt0.52 0.52.25-2
I: Retrieving libnftables1 1.1.6-1
I: Validating libnftables1 1.1.6-1
I: Retrieving libnftnl11 1.3.1-1
I: Validating libnftnl11 1.3.1-1
I: Retrieving libpam-modules 1.7.0-5+b1
I: Validating libpam-modules 1.7.0-5+b1
I: Retrieving libpam-modules-bin 1.7.0-5+b1
I: Validating libpam-modules-bin 1.7.0-5+b1
I: Retrieving libpam-runtime 1.7.0-5
I: Validating libpam-runtime 1.7.0-5
I: Retrieving libpam0g 1.7.0-5+b1
I: Validating libpam0g 1.7.0-5+b1
I: Retrieving libpcre2-8-0 10.46-1+b1
I: Validating libpcre2-8-0 10.46-1+b1
I: Retrieving libpopt0 1.19+dfsg-2+b1
I: Validating libpopt0 1.19+dfsg-2+b1
I: Retrieving libproc2-0 2:4.0.4-9+b1
I: Validating libproc2-0 2:4.0.4-9+b1
I: Retrieving libreadline8t64 8.3-4
I: Validating libreadline8t64 8.3-4
I: Retrieving libseccomp2 2.6.0-2+b1
I: Validating libseccomp2 2.6.0-2+b1
I: Retrieving libselinux1 3.9-4+b1
I: Validating libselinux1 3.9-4+b1
I: Retrieving libsemanage-common 3.9-1
I: Validating libsemanage-common 3.9-1
I: Retrieving libsemanage2 3.9-1+b1
I: Validating libsemanage2 3.9-1+b1
I: Retrieving libsepol2 3.10-1
I: Validating libsepol2 3.10-1
I: Retrieving libslang2 2.3.3-5+b3
I: Validating libslang2 2.3.3-5+b3
I: Retrieving libsmartcols1 2.41.3-4
I: Validating libsmartcols1 2.41.3-4
I: Retrieving libss2 1.47.4-1
I: Validating libss2 1.47.4-1
I: Retrieving libssl3t64 3.6.1-3
I: Validating libssl3t64 3.6.1-3
I: Retrieving libstdc++6 16-20260322-1
I: Validating libstdc++6 16-20260322-1
I: Retrieving libsystemd-shared 260.1-1
I: Validating libsystemd-shared 260.1-1
I: Retrieving libsystemd0 260.1-1
I: Validating libsystemd0 260.1-1
I: Retrieving libtext-charwidth-perl 0.04-11+b5
I: Validating libtext-charwidth-perl 0.04-11+b5
I: Retrieving libtext-iconv-perl 1.7-8.1
I: Validating libtext-iconv-perl 1.7-8.1
I: Retrieving libtext-wrapi18n-perl 0.06-10
I: Validating libtext-wrapi18n-perl 0.06-10
I: Retrieving libtinfo6 6.6+20251231-1
I: Validating libtinfo6 6.6+20251231-1
I: Retrieving libtirpc-common 1.3.7+ds-1
I: Validating libtirpc-common 1.3.7+ds-1
I: Retrieving libtirpc3t64 1.3.7+ds-1
I: Validating libtirpc3t64 1.3.7+ds-1
I: Retrieving libudev1 260.1-1
I: Validating libudev1 260.1-1
I: Retrieving libunistring5 1.4.2-1
I: Validating libunistring5 1.4.2-1
I: Retrieving libuuid1 2.41.3-4
I: Validating libuuid1 2.41.3-4
I: Retrieving libxtables12 1.8.13-1
I: Validating libxtables12 1.8.13-1
I: Retrieving libxxhash0 0.8.3-2+b1
I: Validating libxxhash0 0.8.3-2+b1
I: Retrieving libzstd1 1.5.7+dfsg-3+b1
I: Validating libzstd1 1.5.7+dfsg-3+b1
I: Retrieving linux-sysctl-defaults 4.15
I: Validating linux-sysctl-defaults 4.15
I: Retrieving login 1:4.16.0-2+really2.41.3-4
I: Validating login 1:4.16.0-2+really2.41.3-4
I: Retrieving login.defs 1:4.18.0-2
I: Validating login.defs 1:4.18.0-2
I: Retrieving logrotate 3.22.0-1
I: Validating logrotate 3.22.0-1
I: Retrieving logsave 1.47.4-1
I: Validating logsave 1.47.4-1
I: Retrieving mawk 1.3.4.20260302-1
I: Validating mawk 1.3.4.20260302-1
I: Retrieving mount 2.41.3-4
I: Validating mount 2.41.3-4
I: Retrieving nano 8.7.1-1
I: Validating nano 8.7.1-1
I: Retrieving ncurses-base 6.6+20251231-1
I: Validating ncurses-base 6.6+20251231-1
I: Retrieving ncurses-bin 6.6+20251231-1
I: Validating ncurses-bin 6.6+20251231-1
I: Retrieving netbase 6.5
I: Validating netbase 6.5
I: Retrieving nftables 1.1.6-1
I: Validating nftables 1.1.6-1
I: Retrieving openssl-provider-legacy 3.6.1-3
I: Validating openssl-provider-legacy 3.6.1-3
I: Retrieving passwd 1:4.18.0-2
I: Validating passwd 1:4.18.0-2
I: Retrieving perl-base 5.40.1-7+b1
I: Validating perl-base 5.40.1-7+b1
I: Retrieving procps 2:4.0.4-9+b1
I: Validating procps 2:4.0.4-9+b1
I: Retrieving readline-common 8.3-4
I: Validating readline-common 8.3-4
I: Retrieving sed 4.9-2
I: Validating sed 4.9-2
I: Retrieving sensible-utils 0.0.26
I: Validating sensible-utils 0.0.26
I: Retrieving sqv 1.3.0-5
I: Validating sqv 1.3.0-5
I: Retrieving systemd 260.1-1
I: Validating systemd 260.1-1
I: Retrieving systemd-sysv 260.1-1
I: Validating systemd-sysv 260.1-1
I: Retrieving sysvinit-utils 3.18-1
I: Validating sysvinit-utils 3.18-1
I: Retrieving tar 1.35+dfsg-4
I: Validating tar 1.35+dfsg-4
I: Retrieving tzdata 2026a-1
I: Validating tzdata 2026a-1
I: Retrieving udev 260.1-1
I: Validating udev 260.1-1
I: Retrieving util-linux 2.41.3-4
I: Validating util-linux 2.41.3-4
I: Retrieving vim-common 2:9.2.0218-1
I: Validating vim-common 2:9.2.0218-1
I: Retrieving vim-tiny 2:9.2.0218-1
I: Validating vim-tiny 2:9.2.0218-1
I: Retrieving whiptail 0.52.25-2
I: Validating whiptail 0.52.25-2
I: Retrieving zlib1g 1:1.3.dfsg+really1.3.1-3
I: Validating zlib1g 1:1.3.dfsg+really1.3.1-3
E: Couldn't download packages: dhcpcd-base libapt-pkg7.0 ifupdown libbsd0 less gzip init-system-helpers libaudit1 libacl1 dmidecode kmod iputils-ping dpkg libaudit-common kali-archive-keyring iproute2 gcc-16-base libbpf1 findutils libattr1 diffutils hostname debian-archive-keyring debconf-i18n init debianutils fdisk libblkid1 grep e2fsprogs
E: An unexpected failure occurred, exiting...
