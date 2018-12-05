New bug reports in Linux Mint 19.1 BETA

All editions
------------

mintdriver:
	After a standard install, I ran Driver Manager and chose to change from the default nouveau driver to the nvidia-590 driver. Rebooted and all good.
    I then switched back to the nouveau driver, and rebooted.
    When I now go into Driver Manager, it says I have manually installed a driver and it will not allow me to select either the nouveau or nvidia-590 driver.
    Screenshot: https://imgur.com/7EqM6M3

xplayer:
	https://github.com/linuxmint/xplayer/issues/108

ubiquity:
	GRUB TIME OUT isn't set properly
	Wrong French layout: https://github.com/linuxmint/linuxmint/issues/50

Cinnamon Edition
----------------

in HiDPI, keyboard applet, the flags is not the proper size. Hovering it fixes it.

wacom buttons ignored in tablet mode

gwl:
	Ctrl to launch new instance
	middle-click on empty pinned group wants to kill something?
	different system settings modules (say colors and date-time) get grouped together, despite having a different icon
	in settings, "window list" applet (when switched to modern) looks as if it's added and broken.

menu:
	With the modern layout, the Menu icon (the Mint logo) looks blurry compared to the “crisp” icons of the grouped applications taskbar
	I would like a tiny bit more space between the start menu and the following "Grouped windows list" icons, like with "panel launcher" or "window list" that have a bit space to their left.

Fixed in PR:
	calendar text is too small.
	The notification area icons will look more elegant if is set to 22 px. by default (even so, will be bigger than the defaults on Linux Mint 19.0).
	Start menu doesn't auto-shrink – too much space between the lock and favorites button and unused space under "Places".

Fixed in Git:
	xed menu item not translated

MATE Edition
------------

Xfce Edition
------------
