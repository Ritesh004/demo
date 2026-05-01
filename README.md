Act as a senior Linux OS developer and system engineer. You are responsible for building a custom operating system named "Sentinel OS" by modifying an extracted Kali Linux ISO.

Do not give generic explanations. Execute the task step-by-step like you are performing it yourself.

Project Objective:
Transform the extracted Kali Linux ISO into a minimal, CLI-based operating system that boots successfully in a virtual machine (VirtualBox/VMware) with low resource usage and no heavy graphical environment.

Current Status:

* Kali Linux ISO has already been extracted
* Working environment is Linux
* I have terminal access and root privileges

Your Responsibilities:

1. Environment Setup:

* Guide me to enter and prepare the chroot environment correctly
* Mount required directories (/proc, /sys, /dev, /run)

2. System Minimization:

* Identify and remove all unnecessary GUI components (GNOME, KDE, display managers)
* Keep only essential packages (bash, coreutils, networking tools, SSH)
* Ensure system stability after removal

3. CLI Boot Configuration:

* Configure system to boot into CLI mode using systemd
* Set default target to multi-user.target
* Disable graphical services completely

4. System Optimization:

* Disable unnecessary background services
* Reduce boot time
* Clean unused packages and dependencies

5. Branding:

* Change OS name to "Sentinel OS"
* Update hostname, issue file, and any visible OS identifiers accordingly to our project Sentinel OS

6. ISO Rebuild Process:

* Rebuild filesystem.squashfs correctly
* Ensure GRUB bootloader is correctly configured

7. Validation:

* Ensure ISO boots in VirtualBox without errors
* Confirm CLI login prompt appears
* Troubleshoot common boot failures (GRUB issues, kernel panic, missing init)



