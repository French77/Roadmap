Fixed Issues since Linux Mint 18.3 BETA

All editions
------------

    mintsources:
        doesn't start in some locales due to unicode error (German, Russian..etc) + various unicode issues
        can't add PPA
        segfault in base repository speed tests

    Xed has some untranslated items for pt_BR in the “View, Larger Text, Smaller Text, Normal size” option.
    virtualbox guest support removed (no longer needed, well done Oracle ;))

    mintinstall:
        flatpaks do not install when they miss dependencies (discord for instance)
        the installation/removal progress needs to show more info than just the progressbar
        window is too big and won't maximize in 1024x768
        reset scrolledwindows when appropriate
        fix name collisions in search/lists
        missing xdg-desktop-portal-gtk
        fix flatpaks not showing up in menus on first login
        can't install steam (debconf)
        flatpak spinner should indicate that it will take some time...
        some flatpaks are missing icons

    mintbackup:
        the icon for Personal data (home directory) should be the same as home directory icon

    mintupdate:
        no window progress when installing/removing kernel

    mintreport
        go back and forth between two info and you see the source

    blueberry:
        rfkill survives logout
        double-tray when toggling systray switch

Cinnamon Edition
----------------
    menu doesn't go all the way down
    nemo grid https://github.com/linuxmint/nemo/issues/1642
    Panel edit mode - Applets can not be repositioned, except in central green area, left (red) and right (blue) areas appear grey and non-functional
    I can’t put any applets at all to the panel, just remove the existing.
    menu makes cinnamon crash https://github.com/linuxmint/Cinnamon/issues/7021
    switch audio to HDMI, disconnect HDMI, it's not possible to switch back then

Xfce Edition
------------
    Fix focus stealing prevention for whisker menu
    Add xed, calculator, task manager to menu favorites.