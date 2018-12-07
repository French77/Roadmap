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

sane:
	https://bugs.launchpad.net/ubuntu/+source/sane-backends/+bug/1731459

Cinnamon Edition
----------------

in HiDPI, keyboard applet, the flags is not the proper size. Hovering it fixes it.

wacom buttons ignored in tablet mode


The ‘system-shutdown’, ‘ system-log-out’ and ‘system-lock-screen’ icons don’t scale properly on big panels (50+). Instead of 48px icons they are upscaled (blurry) 32px. It might also be a nice feature to be able to ‘pin’ them down in the aforementioned applet.

center-align applet text (test with %n in clock applet)

mint-y: tooltips don't match theme
mint-y gwl theme broken for top/right/left panels

gwl:
	different system settings modules (say colors and date-time) get grouped together, despite having a different icon
	mint-x + panel on top -> all groups active
	remove dnd option to pin
	dnd on pin should be persistent
	vertical thumbs, restart cinnamon -> wrong number of thumbs

menu:
	With the modern layout, the Menu icon (the Mint logo) looks blurry compared to the “crisp” icons of the grouped applications taskbar
	I would like a tiny bit more space between the start menu and the following "Grouped windows list" icons, like with "panel launcher" or "window list" that have a bit space to their left.

Fixed in Git:
	xed menu item not translated

MATE Edition
------------

Xfce Edition
------------
