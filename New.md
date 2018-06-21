New bug reports in Linux Mint 19 BETA

All editions - last processed comment: June 12, 2018 at 2:50 pm
---------------------------------------------------------------

- check that ISO installed in BIOS mode (USB stick)
- update inxi
- update timeshift to 18.06
- ubiquity: click rel notes, nothing happens
- remove ureadahead? faster boot?
- Shutdown takes forever: “A stop job is running for Cryptography Setup for cryptoswap1” takes over 5 minutes
- systemd-udev cause high cpu: https://bugs.launchpad.net/ubuntu/+source/udev/+bug/1767968?comments=all
- Boot hangs 1 minute with “gave up waiting for suspend/resume device”, there seems to be a wrong uuid for resume in initramfs. Temporarily solution is here: https://askubuntu.com/questions/1013830/slow-boot-long-kernel-load-time-due-to-wrong-resume-device

Cinnamon Edition
----------------

- csd-power: https://github.com/linuxmint/cinnamon-settings-daemon/issues/209
- machine will not hibernate, (either from the power button (the hibernate option is selected) or from the exit menu) the screen blanks for a couple of seconds then returns to the session)
- With panel set to “smart hide”: if panel was never hidden since the beginning of the session, the status of mintupdate is working as expected. Once panel is hidden (by maximizing a window) the mintupdate tray icon remains static for the rest of the session.
- Wanting to add a new custom Menu category to adding ones own Items to a category is like pulling teeth. Icon's don't save, Can't arrange Items and etc. No way to add desktop Files to the menu after they have already been created.
- Unable to unlock the screensaver via LDAP with libpam-ldap and nscd packages installed pointing to an openldap server.

MATE Edition
------------

Xfce Edition
------------

