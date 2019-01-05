Non-blocking bugs
=================

print test page https://github.com/linuxmint/linuxmint/pull/77/files
wine: metapackage, mime handler and menu items

artwork:
  - mintwelcome icon
  - package mint-y variations into flathub

cinnamon:
  - Even after authorize Samba in gufw, Nemo doesn’t show the local network and machine on it. I must manually type smb://user@ip to get in (after workgroup and password) In Mint 18 that was directly available.
  - When in tablet mode (that is, the screen is rotated and covering the keyboard) the RotateWindows key doesn't work anymore... It just does nothing...
  - menu-editor: picking a pixmap in /usr/share/pixmaps for a category results in no icon being shown in the menu.
  - Unable to unlock the screensaver via LDAP with libpam-ldap and nscd packages installed pointing to an openldap server.
  - csd power: https://github.com/GNOME/gnome-settings-daemon/commit/82af1816f32a26f28027ea7ce8edc79cd833bc76
  - in HiDPI, keyboard applet, the flags is not the proper size. Hovering it fixes it.
  - mounted volume applet: no notification when unmounting (as opposed to when it's done in nemo).
  - gwl: Enable "application name" label. Open FF, open at least two browser tabs. Close FF. The label slides over the icon and doesn't disappear: https://kepkuldes.com/image/UoNHl
  - nemo: custom folder colors are blurry (they use png instead of svg)

xapps don't react consistently to ctrl+q and ctrl+w

mintupdate:
    don't gather packages in checkAPT as root: https://github.com/linuxmint/mintupdate/issues/379
    safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).
    notice to reboot the computer when appropriate
    unit tests and improvements for kernel recommendation

update translations for installation guide

Linux Mint 19.2
===============

    system:
        add support for 32-bit EFI: https://forums.linuxmint.com/viewtopic.php?f=29&t=283381

    artwork considerations:
        contrast down to #000?
        switch to ubuntu fonts?
        revamp sound theme?
        revamp isolinux/grub menus?
        revamp plymouth splash?
        cinnamon themes to use system fonts?
        text-size to be configurable in panel zones?
        cinnamon/gtk mint-y: tooltips don't match theme
        grey-on-grey icons (many in cinnamon-settings)
        review color variations in mint-y

    mintlocale:
        https://github.com/linuxmint/mintlocale/issues/36

    pia-manager:
        https://github.com/linuxmint/pia-manager/issues/11

    help
        rtd dev guide
        rtd security guide

    mate:
        consider brisk menu

    mintupdate:
        systray icon or infobar to notify user of new Mint versions
        remember sorting of updates
        have an option for update manager to initiate a timeshift backup prior to applying upgrades?
        retire levels

    port mintstick to python3

    mintreport:
        detect missing l10n packages and hint at mintlocale
        warn about root password if not set

    artwork
        add dark variant support to Mint-Y (needs fixes in Caja/marco)
        cursor theme?
        sound theme?
        bump resolution of branded backgrounds

    cinnamon
        enable recent by default, fix mem leak https://github.com/linuxmint/cinnamon-desktop/commit/2015cc0f8a8fe46384225b0cf10df45f7d3d9315#diff-7ad95a88738c9b5cd253f469add87640

    slick
        would be nice to show release number

    xapps/cinnamon/nemo:
        don't ship icons with generic names in /usr/share/hicolor. All icons should be prefixed (cs-, xapp-, nemo-..etc..) so they don't conflict with other packages

    xfce:
        consider backports https://blog.xfce.org/

    cinnamon
        gtk windows
        merge appsys and cmenus
        ditch docinfo

    nemo
        better navbar
        consider sping loaded folders https://www.youtube.com/watch?v=gdUPrMjlLy8

    xreader:
        consider zoom factor indicator

    xed:
        option to remember past opened-documents

LMDE 4
======

remove debian-multimedia

Roadmap
=======

    main ideas
        mintsystem apt downgrade

    desktop-search:
        local files
        web engines
        recent
        apps
        dictionary
        translations

    mate:
        switch mozo for menulibre

    mintreport:
        dmesg errors
        foreign packages if pinned by mint
        wrong lsb info..etc.
        slow boot sequence
        slow shutdown sequence
        migrate to systemd-coredump (to make it compatible with LMDE)
        systray support
        use systemd-coredump

    implement an alarm clock

    cinnamon:
        cinnamon slow to start after boot --> delay execution of appsys/docinfo until the DE is loaded
        CSD: support mouse wheel speed? Evdev scrolling distance?
        preferences > keyboard > custom shortcuts. Used with a Spanish keyboard layout. Recorded: crtl+number and ctrl+Shift+number (e.g. ctrl+1 and ctrl+shift+1 = ctrl+!) they are recorded correctly. When using the shortcut the command defined in the shift combination is triggered with just ctrl+number (i.e. ctrl+1). The complete combination triggers nothing (i.e. ctrl+shift+1 does nothing) and the comand defined in ctrl+number can never be used. This worked in 17.3.
        track/troubleshoot shutdown sequence (user should know what is happening when shutdown isn't immediate)
        track/troubleshoot vsync, compositing, unredirected windows and policy
        todo list applet/desklet
        calendar events applet/desklet
        multiple clocks https://github.com/simonwiles/cinnamon_applets
        network applet: airplane mode (quick way to rfkill all)
        nemo: retire computer:/// place (which is completely useless) or revamp it into something better
        alt-tab and panel use icon provided by appsys, ignoring icon set by the application itself (example: a python window using widow.set_icon_name())
        actions in panel launchers aren't translated if not present in .desktop file
        When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
        Is there any reason why there are two names for the same item, eg. "Trash" and "Rubbish Bin"? Would it be better to standardise on only one name?
        add gnome-screenshot to panel, right-click and select "Take screenshot of a selected area". This runs gnome-screenshot -a.. it should work but it doesn't. Is it because of the panel launcher capturing the click event or something?

    xapps
        implement an app-sharing protocol to quickly move a document from one app to another

        gestures support:
            pinch:
                zoom document in pix
                zoom view in nemo

            swipe:
                previous/next document in pix

            scroll:
                sound-volume/seek in xplayer

            click:
                pause/resume in xplayer

            double-click:
                full-screen in xplayer
                full-screen in xviewer

        pix
            doesn't rotate videos when playing them
            vignettes should look better, and the same in all themes
            support prefer-dark-themes
            treeview in sidebar shows unecessary "(empty)" when dirs have no subdirs

    artwork:
        Tray icons are black with mint-y themes.
        mint-x-icons: network status icons have a dark background in panel 33px and bigger (sound icon looks wrong in 41px and bigger).
        mint-y The maximize/restore window control button doesn’t change visually between in maximized and restored state (default theme and Mint-Y-Dark)

    system:
        compiler optimization: consider optimizing compiled binaries for Cinnamon/Xapps

    HiDPI support:
        upstream apps using GTK2: Gimp, Hexchat, Tomboy.

R&D
===

    system
        consider enabling recommends

    network discovery:
        easy out-of-the-box interactions (messaging/presence/file-sharing) over the LAN
