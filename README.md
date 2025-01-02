# This fork includes community fixes to the original theme.
Changes:
- [Original theme](https://github.com/monday15/lounge-gtk-theme) by [monday15](https://github.com/monday15)
- [Fix linked buttons styling; also add styles for libhandy](https://github.com/monday15/lounge-gtk-theme/pull/22) by [johnfactotum](https://github.com/johnfactotum)
- Metacity theme from [Ceres GTK theme](https://gitlab.com/sixsixfive/ceres-gtk) by [sixsixfive](https://gitlab.com/sixsixfive). Modified by [vyvir](https://github.com/vyvir).
- MATE desktop theme by [vyvir](https://github.com/vyvir).

## Overview
A GTK theme with a vintage scrollbars, inspired by Absolute, based on Adwaita.  
Supported desktop environments: GNOME, XFCE, MATE.  

[**Default theme screenshot**](https://user-images.githubusercontent.com/42862490/64915766-e0395300-d766-11e9-8a0b-1a9b93cc6d3d.png)  
[**Availiable options screenshot**](https://user-images.githubusercontent.com/42862490/64915767-e0395300-d766-11e9-9ced-6516835ed114.png)

Also check Lounge-backgrounds - dynamic wallpaper for gnome-desktop [(repository)](https://github.com/monday15/lounge-backgrounds).
 
## Installation

## Building (preferred)
Requirements:  
`gtk3` (3.22+)   
`meson` (0.45+)  
`sassc`  
`gtk-murrine-engine` (`gtk2-engines-murrine` for debian/ubuntu).

- Download and decompress source tarball (or clone repository);
- Build theme:  
`meson build -Doption=value`

  [(availiable options screenshot)](https://user-images.githubusercontent.com/42862490/64915767-e0395300-d766-11e9-9ced-6516835ed114.png)

  Option | Default value | Other values | Description 
  --- | --- | --- | ---
  tone | tango | salsa rumba jive | Color scheme
  style | prime | flat | Theme style (only for gtk2/gtk3)
  scale_style | casual | fancy | Scales and progressbars style (only for gtk2/gtk3)
  scrollbar_handles | no_handles | with_handles | Handles on scrollbars 
  button_outlines | strong | bright | Focus outline color on regular buttons in a light theme (only for gtk3)
  shell_font | Roboto | any font | Set font for gnome-shell theme
  gtk2_solid_menu | false | true | Use solid border for menus in gtk2 theme - highly recommended option for XFCE/Sway users, but looks bad in GNOME, [screenshot from XFCE](https://user-images.githubusercontent.com/42862490/54489243-230b9280-48cc-11e9-9191-7912a4ef328f.png)
  icons | true | false | Build auxiliary icon theme
  icon_theme | Adwaita | any theme | Set main icon theme for auxiliary one
  gnome_version | auto | 3.28 - 3.34 | Affects only gnome-shell theme and nautilus style. Meson detect gnome version automatically based on gnome-shell version, if there is no gnome-shell and you plan to use nautilus file manager - you need to set version manually, so correct style will be used.

  > For example, `meson build -Dtone=salsa -Dscale_style=fancy -Dshell-font='Liberation Sans'`  
  builds the theme with purple accent colors, colored scales/progressbars, and with Liberation Sans font in gnome-shell.

- Install theme:  
`sudo ninja -C build install`

## Flatpak
Flatpak apps support available via Flathub:  
`flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo`  
`flatpak install flathub org.gtk.Gtk3theme.Lounge`  
`flatpak install flathub org.gtk.Gtk3theme.Lounge-night`  
`flatpak install flathub org.gtk.Gtk3theme.Lounge-compact`  
`flatpak install flathub org.gtk.Gtk3theme.Lounge-night-compact`  

> If you want to use the theme built with custom options for flatpak apps, you can install default flatpak package and copy files from you variant of the theme to flatpak folder. Default location for flatpak packages is `/var/lib/flatpak/...`, full command will look something like `sudo cp -r /usr/share/themes/Lounge/gtk-3.0/* /var/lib/flatpak/runtime/org.gtk.Gtk3theme.Lounge/x86_64/3.22/active/files/`. Note, that flatpak supports only gtk3 themes.


## License
GPLv3+, see LICENSE file.  
Original themes/styles copyrights are in COPYRIGHT file.

## Bugs
Report bugs to [issues page](https://github.com/monday15/lounge-gtk-theme/issues).

## Thanks
Alexey Ignatiev, Allan Day, Carlos Lobano, dcbaker, Emmanuele Bassi, horst3180, nana-4, NicoHood, Sam Hewitt, Thibault Saunier, tista500, vinceliuice, ZMA, all people in copyright file, Gnome developers and maintainers, Fedora developers and maintainers, Greybird theme developers, Meson developers, Yaru theme developers.

## Links
[Adwaita gtk2 theme](https://gitlab.gnome.org/GNOME/gnome-themes-extra), [Adwaita gtk3 theme](https://gitlab.gnome.org/GNOME/gtk), [gnome-shell theme](https://gitlab.gnome.org/GNOME/gnome-shell), [Materia theme](https://github.com/nana-4/materia-theme), [Yaru theme](https://github.com/ubuntu/yaru).  
List of applications (their original css styles used in the theme): [Gedit](https://gitlab.gnome.org/GNOME/gedit), [Nautilus](https://gitlab.gnome.org/GNOME/nautilus), Epiphany.
