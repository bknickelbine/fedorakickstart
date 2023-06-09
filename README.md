# Files for making a Fedora 38 KDE automatic installer using Ventoy

Configuration files to:
- Boot the Fedora-Everything-netinst-x86_64-38-1.6_VTNORMAL.iso from a /Fedora directory on the Ventoy flash drive
	> The _VTNORMAL suffix causes the disk to automatically boot into Normal mode in Ventoy **(required for menu replacement)**
- Once booted, the GRUB menu will choose the first option (default="0" in the menu configuration) after 1 second timeout. This bypasses the need for a media check.
- The Fedora installer will then kick off automatically, destroying everything on the first hard drive and installing Fedora 38 with KDE. It will be configured with US keyboard layout, America/Phoenix timezone, and an administrative user named 'kickstart' with a password of 'kickstart'.


- Place the bootgrub2_grub.cfg, efiboot_grub.cfg, and ks2.cfg in a directory called /script on the Ventoy flash drive. Place the ventoy.json file in the /ventoy directory.
### This configuration is meant to facilitate easier OS deployment before device turn in needing any bootable OS. It is not meant to be used as-is for normal deployment scenarios. Almost all non-critical packages have been removed from the installation, and it uses a mirror that provides fast downloads for our environment. However, the kickstart configuration file could be modified to suit your specific needs.
