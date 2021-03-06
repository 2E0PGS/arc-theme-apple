# Arc Theme

Arc is a flat theme with transparent elements for GTK 3, GTK 2 and GNOME Shell which supports GTK 3 and GTK 2 based desktop environments like GNOME, Unity, Budgie, Pantheon, Xfce, MATE, etc.

## My Changes

This is a custom version of the arc-theme. I have changed the minimise, maximise, close buttons and a couple extra for the unity desktop so it looks more like a apple computer. I believe this looks better than the icons that come with arc by default. The icons I am using to replace the default ones are from: https://github.com/anmoljagetia/Flatabulous

Currently deprecated due to an exsisting project doing the same thing: https://github.com/andreisergiu98/arc-flatabulous-theme

###Arc is available in three variants 

#####Arc

![A screenshot of the Arc theme](https://i.imgur.com/luT6T5N.png)

#####Arc-Darker

![A screenshot of the Arc-Darker theme](https://i.imgur.com/c9nIa48.png)

#####Arc-Dark

![A screenshot of the Arc-Dark theme](https://i.imgur.com/Tx3it2m.png)


### Requirements

* Gnome/GTK 3.14, 3.16, 3.18 or 3.20
* The `gnome-themes-standard` package
* The murrine engine. This has different names depending on your distro.
  * `gtk-engine-murrine` (Arch Linux)
  * `gtk2-engines-murrine` (Debian, Ubuntu, elementary OS)
  * `gtk-murrine-engine` (Fedora)
  * `gtk2-engine-murrine` (openSUSE)
  * `gtk-engines-murrine` (Gentoo)

Main distributions that meet these requirements are

* Arch Linux and Arch Linux based distros
* Ubuntu 15.04, 15.10 and 16.04 (**Ubuntu 14.04 and 14.10 are not supported**)
* elementary OS Freya
* Debian 8, Testing or Unstable
* Gentoo
* Fedora 21 - 24
* openSUSE 13.2, Leap 42.1 and Tumbleweed

Derivatives of these distributions should work, as well.

If your distribution isn't listed, please check the requirements yourself.

### Installation

**Important:** Remove all older versions of the theme from your system before you proceed any further.

    sudo rm -rf /usr/share/themes/{Arc,Arc-Darker,Arc-Dark}
    rm -rf ~/.local/share/themes/{Arc,Arc-Darker,Arc-Dark}
    rm -rf ~/.themes/{Arc,Arc-Darker,Arc-Dark}

#### Manual Installation

To build the theme you'll need 
* `autoconf`
* `automake`
* `pkg-config` or `pkgconfig` if you use Fedora
* `libgtk-3-dev` for Debian based distros or `gtk3-devel` for RPM based distros
* `git` if you want to clone the source directory

Quick install of deps:
* `sudo apt-get install autoconf automake libgtk-3-dev git`

If your distributions doesn't ship separate development packages you just need GTK 3 instead of the `-dev` packages.

Install the theme with the following commands

**1. Get the source**

If you want to install the latest version from git, clone the repository with

    git clone https://github.com/2E0PGS/arc-theme-apple/ --depth 1 && cd arc-theme-apple

**2. Build and install the theme**

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-transparency     disable transparency in the GTK3 theme
    --disable-light            disable Arc Light support
    --disable-darker           disable Arc Darker support
    --disable-dark             disable Arc Dark support
    --disable-cinnamon         disable Cinnamon support
    --disable-gnome-shell      disable GNOME Shell support
    --disable-gtk2             disable GTK2 support
    --disable-gtk3             disable GTK3 support
    --disable-metacity         disable Metacity support
    --disable-unity            disable Unity support
    --disable-xfwm             disable XFWM support

    --with-gnome=<version>     build the theme for a specific GNOME version (3.14, 3.16, 3.18, 3.20)
                               Note: Normally the correct version is detected automatically and this
                               option should not be needed.

After the installation is complete you can activate the theme with `gnome-tweak-tool` or a similar program by selecting `Arc`, `Arc-Darker` or `Arc-Dark` as Window/GTK+ theme and `Arc` or `Arc-Dark` as Gnome-Shell and Xfce-Notify theme.

**Uninstall the theme**

Run

    sudo make uninstall

from the same directory as this README resides in, or

    sudo rm -rf /usr/share/themes/{Arc,Arc-Darker,Arc-Dark}

### Extras

#### Numix-Circle
The icon theme I use in the screenshots above https://github.com/numixproject/numix-icon-theme-circle

#### Arc Firefox theme
A theme for Firefox is available at https://github.com/horst3180/arc-firefox-theme

#### Arc icon theme
The Arc icon theme is available at https://github.com/horst3180/arc-icon-theme

#### Chrome/Chromium theme
To install the Chrome/Chromium theme go to the `extra/Chrome` folder and drag and drop the arc-theme.crx or arc-dark-theme.crx file into the Chrome/Chromium window. The source of the Chrome themes is located in the source "Chrome/arc-theme" folder.

#### Plank theme
To install the Plank theme, copy the `extra/Arc-Plank` folder to `~/.local/share/plank/themes` or to `/usr/share/plank/themes` for system-wide use.
Now open the Plank preferences window by executing `plank --preferences` from a terminal and select `Arc-Plank` as the theme.

#### Arc-Dark for Ubuntu Software Center
The Arc Dark theme for the Ubuntu Software Center by [mervick](https://github.com/mervick) can be installed from [here](https://github.com/mervick/arc-dark-software-center). It solves readability issues with Arc Dark and the Ubuntu Software Center.

### Troubleshooting

If you have Ubuntu with a newer GTK/GNOME version than the one included by default (i.e Ubuntu 14.04 with GTK 3.14 or Ubuntu 15.04 with GTK 3.16, etc.) the prebuilt packages won't work properly and you have to install the theme manually as described above.
This is also true for other distros with a different GTK/GNOME version than the one included by default

--

If you get artifacts like black or invisible backgrounds under Unity, disable overlay scrollbars with

    gsettings set com.canonical.desktop.interface scrollbar-mode normal


### Bug reporting
If you find a bug, please report it at:
* My repo https://github.com/2E0PGS/arc-theme-apple/issues
* Main original dev repo https://github.com/horst3180/arc-theme/issues

### Full Preview
![A full screenshot of the Arc theme](http://image.prntscr.com/image/5cbc6df33da9445b91d86ecb6e91d24d.png)
