Triaged reports

Not a bug
---------
    Software Manager: remove a package with dependencies, Software Manager continues to show the dependencies as installed. -> we only rebuild
    startup apps: 1) install Caffeine or any other software that will appear in Startup Applications, 2) uninstall it, 3) Open Startup Application and the link is still there -> need to apt purge since it's a conf file

Outside of the scope
--------------------
    could you add a VPN L2TP to the live image. Internet is not present.

Can't reproduce
---------------
    synaptic: On the very first start the quick-filter field + the label placed above are not displayed. Successive starts (with/without reboot) show both. --> probably rebuilding its index.
    pt_BR:
        The users and groups asks for password and when it opens the window it appears ask for password again and it gets in an infinite loop.
        Ppa fonts do not open through the system central, neither by the update manager nor by the menu.
        Bluetooth in system settings takes several minutes to open.
        Desklets in the Download option, the download failed with the following message “A problem occurred while trying to access the server, please try again later. Details: HTTP Error 400: Bad Request ”
    cinnamon:
        crash when restarting nm: https://blog.linuxmint.com/?p=3445#comment-137946
        gnome-keyring-daemon delays session quit
    slick:
        running a live session under VirtualBox with two monitors defined. Playing with the login window settings, just to see what happens. Under “Optional pictures > Other monitors”, selected a different image than the background. Logoff. The second monitor shows the optional picture. The main monitor shows half of each picture.
    gdebi:
        can't install opera with gdebi -> debconf support is there in the terminal dropdown
    Mint Backup crashes when trying to save to another drive other then the home drive. It will get to 13% and crash every time. If you save it to the home drive it works fine. 

Upstream
--------
    goa: https://imgur.com/a/hCLZe
    mate:
        map in calendar applet is stretched
        emblems/colors don't work https://github.com/mate-desktop/caja/issues/506
    Xfce the network manager applet pop up window from the indicator plugin is very small, uncomfortable. --> GTK menu popups.. known limitation in the toolkit.
