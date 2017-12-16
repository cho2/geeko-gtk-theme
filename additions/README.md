# Geeko Theme

Geeko is a flat theme with transparent elements for GTK 3, GTK 2 and GNOME Shell which supports GTK 3 and GTK 2 based desktop environments like GNOME, Unity, Budgie, Pantheon, Xfce, MATE, etc.

## Geeko is available in three variants 

##### Geeko

![A screenshot of the Geeko theme](/additions/screenshots/light.png)

##### Geeko-Darker

![A screenshot of the Geeko-Darker theme](/additions/screenshots/darker.png)

##### Geeko-Dark

![A screenshot of the Geeko-Dark theme](/additions/screenshots/dark.png)

## Installation

### Manual Installation

To build the theme the follwing packages are required 
* `autoconf`
* `automake`
* `pkg-config` or `pkgconfig` for Fedora
* `libgtk-3-dev` for Debian based distros or `gtk3-devel` for RPM based distros
* `git` to clone the source directory

**Note:** For distributions which don't ship separate development packages, just the GTK 3 package is needed instead of the `-dev` packages.

For the theme to function properly, install the following
* GNOME Shell 3.14 - 3.24, GTK 3.14 - 3.22
* The `gnome-themes-standard` package
* The murrine engine. This has different names depending on the distro.
  * `gtk-engine-murrine` (Arch Linux)
  * `gtk2-engines-murrine` (Debian, Ubuntu, elementary OS)
  * `gtk-murrine-engine` (Fedora)
  * `gtk2-engine-murrine` (openSUSE)
  * `gtk-engines-murrine` (Gentoo)

Install the theme with the following commands

#### 1. Get the source

Clone the git repository with

    git clone https://github.com/LelCP/geeko-theme --depth 1 && cd geeko-theme

#### 2. Build and install the theme

    ./autogen.sh --prefix=/usr
    sudo make install

Other options to pass to autogen.sh are

    --disable-transparency     disable transparency in the GTK3 theme
    --disable-light            disable Geeko Light support
    --disable-darker           disable Geeko Darker support
    --disable-dark             disable Geeko Dark support
    --disable-cinnamon         disable Cinnamon support
    --disable-gnome-shell      disable GNOME Shell support
    --disable-gtk2             disable GTK2 support
    --disable-gtk3             disable GTK3 support
    --disable-metacity         disable Metacity support
    --disable-unity            disable Unity support
    --disable-xfwm             disable XFWM support

    --with-gnome=<version>     build the theme for a specific GNOME version (3.14, 3.16, 3.18, 3.20, 3.22)
                               Note 1: Normally the correct version is detected automatically and this
                               option should not be needed.
                               Note 2: For GNOME 3.24, use --with-gnome-version=3.22
                               (this works for now, the build system will be improved in the future)

After the installation is complete the theme can be activated with `gnome-tweak-tool` or a similar program by selecting `Geeko`, `Geeko-Darker` or `Geeko-Dark` as Window/GTK+ theme and `Geeko` or `Geeko-Dark` as GNOME Shell/Cinnamon theme.

If the `--disable-transparency` option was used, the theme will be installed as `Geeko-solid`, `Geeko-Darker-solid` and `Geeko-Dark-solid`.

## Uninstall

Run

    sudo make uninstall

from the cloned git repository, or

    sudo rm -rf /usr/share/themes/{Geeko,Geeko-Darker,Geeko-Dark}

## Extras

## Troubleshooting

If you use Ubuntu with a newer GTK/GNOME version than the one included by default (i.e Ubuntu 14.04 with GTK 3.14 or Ubuntu 15.04 with GTK 3.16, etc.) the prebuilt packages won't work properly and the theme has to be installed manually as described above.
This is also true for other distros with a different GTK/GNOME version than the one included by default

--

If you get artifacts like black or invisible backgrounds under Unity, disable overlay scrollbars with

    gsettings set com.canonical.desktop.interface scrollbar-mode normal

## License
Geeko is available under the terms of the GPL-3.0.

## Full Preview
![A full screenshot of the Geeko theme](/additions/screenshots/main.png)
<sub>Screenshot Details: Icons: [Papirus](https://github.com/PapirusDevelopmentTeam/papirus-icon-theme) | [Wallpaper](https://github.com/openSUSE/branding/tree/tumbleweed/raw-theme-drop) | [Font](https://github.com/adobe-fonts/source-sans-pro) </sub>
