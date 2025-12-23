---
layout: post
title: Flatpak GTK (not) Respecting KDE Theme
image: /images/getek/getekconek.webp
---

![GTK Theme Breeze]({{ site.baseurl }}/images/getek/getekconek.webp)


There is some issue with Breeze Dark and flatpak+GTK application, then i found the solution for it
there is the i config for that respecting breeze dark for the GTK3/GTK4, and other version GTK as possible (especially respecting the window control on left, offcourse for me 😁).
## Install Breeze dark
1. Install Dark Breeze on flatpak
![Install Breeze Dark]({{ site.baseurl }}/images/getek/installpkg.webp)
```
flatpak install flathub org.gtk.Gtk3theme.Breeze-Dark
```
2. set the teme to breeze dark
![Override]({{ site.baseurl }}/images/getek/overiddegetek.webp)
```
flatpak override --user --env=GTK_THEME=Breeze-Dark
```

## qt6ct
this make integration have better experience with non-flatpak but you can skip this installation

1. Installing qt6ct for better implementation
![Override]({{ site.baseurl }}/images/getek/qt6ct.webp)
```
# pacman -S qt6ct
```

2. Set environtment to qt6ct
set the `QT_QPA_PLATFORMTHEME` on file `/etc/environtment`:
![set environtment]({{ site.baseurl }}/images/getek/env.webp)
```
QT_QPA_PLATFORMTHEME=qt6ct
```

3. setup the qt6ct
open the qt6ct by on meta/super menu or terminal, type: `qt6ct` to run
settings on qt6ct like this or may you can costumize by yourself its ok!
![settings up!]({{ site.baseurl }}/images/getek/qt6ctst.webp)

## Results
There is the results for what i mplementation, some app its still have a libadwaita, but some gtk3 had theme set for breeze and/or dark mode respect (than before had a light theme adwaita)
![Result GTK App]({{ site.baseurl }}/images/getek/result.webp)
