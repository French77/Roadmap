New bug reports in Linux Mint 19.1 BETA

All editions
------------

mintdriver:
	After a standard install, I ran Driver Manager and chose to change from the default nouveau driver to the nvidia-590 driver. Rebooted and all good.
    I then switched back to the nouveau driver, and rebooted.
    When I now go into Driver Manager, it says I have manually installed a driver and it will not allow me to select either the nouveau or nvidia-590 driver.
    Screenshot: https://imgur.com/7EqM6M3

ubiquity:
	GRUB TIME OUT isn't set properly
	kabyle
	fcitx recommends

bird in coast wallpaper

xapps don't react consistently to ctrl+q and ctrl+w

Open update manager — View — Linux Kernels –> Continue
Click Remove old kernels…
If the list is empty (no removable kernel):
The “Remove selected kernels” button remain active, and if you click the button, the “Remove old kernels” windows close, and the Kernels window remain inactive.


 I couldn’t do the installation of my HP Laserjet 1132MFP, following the installation of the hplip file from hp, in the final step it says that it requires a binary file, and enters in a loop that never ends.

Cinnamon Edition
----------------

Booting from USB stick take pause for 10-30 seconds with no USB mouse light and no light on USB stick then light up boot continue. Pause for USB ports reset ?

Terminal prompt color still just green for both user &amp; root, LM 18.3 green for user red for root.
Simple System desklet not working.
SAMBA Windows Networking does not show anything, LM 18.3 show all devices.

Could not find a setting to make a default folder view size. All the folder/file icons seem rather large. I can easily resize with ctrl+ (+/-) or the resize bar but it would be nice to have a customized setting that was global and then I could tweak each folder as needed


When I right click on the desktop and select ‘Customize’, my icons are automatically resorted. This is pretty annoying. Any way it can be changed to not do that unless a re-sort is requested?


Right click “Grouped window list” — Preferences — Configure
Click the Panel tab — Chose: Button label: Application name, Window title or Window title (only for the…)
Now
Open Firefox — Open at least two browser tab — Close Firefox
Watch the “Grouped window list” menu. The caption slide over the icon, and will not disappear.
https://kepkuldes.com/image/UoNHl

gwl add shift click

Panel — Removable drives application: if you unmount a disk, the application doesn’t show feedback (popup window), if you a disk unmount in nemo, the notification is show (popup windows).

MATE Edition
------------

Xfce Edition
------------


rel notes
---------

	Samba changed their protocol to work with Windows 10. I don’t understand the details but if you edit (as root) /etc/samba/smb.conf and add the line “client max protocol = NT1” (without the quote marks) in the [global] section, save the file, and reboot, that should restore the Windows Networking
	The latest samba has changed to a protocol that breaks your network browsing.
For home users, the latest protocol is unlikely to be necessary, so a simple fix is:
As root, edit /etc/samba/smb.conf. Find the section “[global]” and underneath that heading add this line:
client max protocol = NT1
Then restart, and you should be ok.
This patch forces samba to use protocol version 1 instead of the latest version 3.