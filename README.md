Implemented
===========

    Cinnamon:
        Support for HybridSleep
        network applet: Rescan for wireless network
        cinnamon-settings: spices revamp
        nemo-preview support animated gifs
        better translations for cinnamon-session, cinnamon-settings-daemon, nemo-extensions
        HiDPI mode set to Auto
        window list can show windows from other workspaces
        secondaryActivate on middle-click in indicators (when indicator support is enabled)
        goa/google-drive/owncloud support
        touchpads: full libinput/synaptic support with automatic mode for clickpad/scrolling
        on-screen keyboard: size and position configurable, no animations, fixed response to at-spi, no longer blocks onboard
        alt-tab can show windows from all workspaces
        alt-tab no longer places minimized windows to the end of the list (configurable)

    Slick:
        indicator tooltips
        support for numlockx
        optional panel indicators
        LDAP options (hiding user list, manual login)
        Added option for auto login

    mintsources ported to GTK3

    mintinstall:
        UI and nagivation revamp
        GTK3 + HiDPI
        User mode + aptdaemon backend
        speed improvements

    mintbackup:
        complete revamp
        user mode + aptdaemon backend
        revamped UI
        revamped threading and performance
        restricted to home dir
        always preserves perms/times

    mintdrivers:
        better HiDPI support
        better CPU microcode detection/presentation

    Xapp window-progress now supported by:
        cinnamon
        nemo
        mintinstall
        mintstick
        mintdrivers
        mintbackup
        synaptic dialogs (mintlocale, mintsources, mintupdate)

    xplayer:
        removed xplayer-mozilla
        better fullscreen statusbar

    xed:
        minimap

    xreader:
        Move history to Go menu, bring back navigation buttons into toolbar
        100% zoom means real document size

    nemo:
        provide configure button for extensions
        fixed nemo-media-columns makes nemo 5 times slower to list directories

    mintreport:
        software crash troubleshooting
        info notices

    software selection:
        add timeshift
        add redshift-gtk
        remove mintnanny and mintupload
        add dbg packages (cinnamon + xapps)

    pia-manager in user mode

    flatpak support

    out of the box support for synonyms/spell-check/hyphenation in many languages

    xfce:
        upgrade xfce-terminal to 0.8.0

Linux Mint 18.3
===============

    Maintenance
        backport CSR 3.4.4 in Sonya

    Issues
        Cinnamon
            menu doesn't go all the way down
            cinnamon network status notification icon looks wrong
            [FIXED in GIT (cdesktop)] disable away message in cinnamon by default
            [FIXED IN GIT (cinnamon)] cinnamon-settings-users misses a polkit policy
            [FIXED IN GIT (ccc) - needs new cinnamon-l10n] goa desktop file misses l10n

        hidpi
            mintwelcome icons are blurry
            cinnamon startup apps icons are blurry

        redshift
            doesn't die when logging out

        Artwork
            would be nice if slick showed our release number

        mintinstall
            Google Earth should be featured
            Skype should be featured

        mintreport
            go back and forth between two info and you see the source

        update mint-translations

    MATE
        1.18 updates
        mintmenu PR

    Xfce
        [DONE] upgrade xfce-terminal to 0.8.0
        task manager 1.2
        notifyd 0.3.6
        dict 0.8
        panel 4.12.1

    Release
        new_features
        rel_notes
            Add instructions to upgrade to HWE Xorg 1.19
            explain EFI boot violations
                [PASS] secureboot OFF
                [PASS] secureboot OFF, no network
                [PASS] secureboot ON, no codecs
                [FAIL] secureboot ON, no network -> violation
                [FAIL] secureboot ON, codecs, turn off secureboot in installer -> violation
                [FAIL] secureboot ON, codecs, don't turn off secureboot in installer -> violation
            explain efibootmgr

Linux Mint 19
=============

    desktop-search:
        local files
        web engines
        recent
        apps
        dictionary
        translations

    mintwelcome:
        UI revamp, guide user and hint at things he/she might want to do (codecs, popular settings, popular apps etc..)

    mintreport:
        detect missing l10n packages and hint at mintlocale

    mintupdate:
        safeguard against package removals (for instance, don't let users perform updates which would remove sensitive packages).
        notice to reboot the computer when appropriate
        purge old kernels? https://github.com/Pjotr123/purge-old-kernels-2

    system:
        compiler optimization: consider optimizing compiled binaries for Cinnamon/Xapps

    cinnamon:
        cinnamon slow to start after boot --> delay execution of appsys/docinfo until the DE is loaded

    nemo:
        Skip GVFS when possible
        File search:
            full-text search
            async search
            simplify UI/features
            ability to search string within files and open xed at line number
        Performance issues:
            File operations:
                Mouse-cursor lag
            Loading views:
                switching views is slower than reloading them
                existing thumbs are loaded asynchronously
                loading is slower than with ls (could be Gvfs, could be the way we render view in GTK. For 25k elements, 0.4s with ls, up to 6s in icon view for Nemo/Caja)
        video thumbnails are blurry

Roadmap
=======

    mintreport:
        dmesg errors
        foreign packages if pinned by mint
        wrong lsb info..etc.
        slow boot sequence
        slow shutdown sequence

    implement an alarm clock

    cinnamon:
        CSD: support mouse wheel speed? Evdev scrolling distance?
        menu keywords: looking for display in menu shows color first
        consider: notifications stay on desktop until mouse is moved + a few secs
        preferences > keyboard > custom shortcuts. Used with a Spanish keyboard layout. Recorded: crtl+number and ctrl+Shift+number (e.g. ctrl+1 and ctrl+shift+1 = ctrl+!) they are recorded correctly. When using the shortcut the command defined in the shift combination is triggered with just ctrl+number (i.e. ctrl+1). The complete combination triggers nothing (i.e. ctrl+shift+1 does nothing) and the comand defined in ctrl+number can never be used. This worked in 17.3.
        track/troubleshoot shutdown sequence (user should know what is happening when shutdown isn't immediate)
        track/troubleshoot vsync, compositing, unredirected windows and policy
        menu: consider adopting this layout (https://raw.githubusercontent.com/The-Panacea-Projects/Gnomenu/master/Screenshot.png), same as ours/mintmenu, only better.
        todo list applet/desklet
        calendar events applet/desklet
        multiple clocks https://github.com/simonwiles/cinnamon_applets
        network applet: airplane mode (quick way to rfkill all)
        nemo: retire computer:/// place (which is completely useless) or revamp it into something better
        alt-tab and panel use icon provided by appsys, ignoring icon set by the application itself (example: a python window using widow.set_icon_name())
        actions in panel launchers aren't translated if not present in .desktop file
        gnome-system-monitor moves out of place in Expo
        When using Cinnamon bar at top, and secondary monitor with higher height than the main display, some apps like KDE Apps (Krita, Kdenlive) or Wine Based Apps (teamviewer) will display menus from toolbar in the wrong place. Being more specific: The menus will be displayed in the position that they should be displayed at main monitor, however in this case the window is maximized in the secondary monitor.
        Is there any reason why there are two names for the same item, eg. "Trash" and "Rubbish Bin"? Would it be better to standardise on only one name?
        add gnome-screenshot to panel, right-click and select "Take screenshot of a selected area". This runs gnome-screenshot -a.. it should work but it doesn't. Is it because of the panel launcher capturing the click event or something?

    xapps
        add an option to blank other monitors when in full screen in xviewer/xreader/pix
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
        Mint-Y themes Shade option is unavailable
        mint-x-icons: network status icons have a dark background in panel 33px and bigger (sound icon looks wrong in 41px and bigger).
        mint-y The maximize/restore window control button doesn’t change visually between in maximized and restored state (default theme and Mint-Y-Dark)

R&D
===

    mintupdate:
        prompt for reboot after kernel install?

    nemo:
        remove duplication between Eject and Safely Remove (for removable devices).

    system
        consider enabling recommends

    review logind.conf changes in:
        MATE
        Xfce
        KDE

    ubiquity:
        inhibit sessions via libxapp (need to do it in KDE too)

    libindicator++?
        client-rendered icon/menu (ala libindicator)
        support all the features from GTK statusicon (tooltips, left/right clicks etc..)

    use aptdaemon?
        aptdaemon doesn't work in LMDE and is being abandoned upstream
        in mintupdate, remove dep on synaptic, remove admin rights for checkAPT.py
        in mintwelcome and codec menu entry, switch from apturl to aptdaemon
        in mintsources, remove dep on synaptic
        remove synaptic from default selection
        remove synaptic from mintmenu's favorites

    network discovery:
        easy out-of-the-box interactions (messaging/presence/file-sharing) over the LAN

    windows compatibility layer:
        seamless wine integration

    HiDPI support:
        upstream apps using GTK2: Gimp, Hexchat, VLC, Pidgin, Tomboy.
        mint projects using GTK2: gksu

LMDE 3
======

    gnome-calculator app title is "gnome-calculator"
    live-installer should show partition labels
