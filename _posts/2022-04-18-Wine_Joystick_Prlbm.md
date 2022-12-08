---
layout: post
title: Wine Controller Joystick Error
image: /images/winejoy/wineglass.png
---

![Logo Pipewire]({{ site.baseurl }}/images/winejoy/wineglass.png)

If You have issue with USB Joystick with driver **Bus 002 Device 004: ID 0810:0001 Personal Communication Systems, Inc. Dual PSX Adaptor** on *L1*/*R1* Button like pictures on below You can try downgrade Wine packages before version 7.×, version 5.× is highly recomended. These example for downgrade a Wine packages on Arch linux based distro (Manjaro, Artix, and others Arch-based distro).
![Logo Pipewire]({{ site.baseurl }}/images/winejoy/joy5.png)
![Logo Pipewire]({{ site.baseurl }}/images/winejoy/joy6.png)


## Method 1
### Download old packages of wine
You can download Wine packages on links below:
- [Wine](https://archive.archlinux.org/packages/w/wine/)
- [Wine Staging](https://archive.archlinux.org/packages/w/wine-staging/)
![Logo Pipewire]({{ site.baseurl }}/images/winejoy/winepkg.png)

Pick one of packages with ended by (file extension) *.xz* or *.zst*. And download it by clicking that hyperlinks or you can use *wget* and for example you can follow this command:
```
cd ~/Downloads
wget https://archive.archlinux.org/packages/w/wine-staging/wine-staging-5.5-1-x86_64.pkg.tar.zst
```
![Logo Pipewire]({{ site.baseurl }}/images/winejoy/wgetwine.png)

After package downloaded, go to directory of downloaded package (Usually at: "**~/Downloads**"). then you can run *pacman -U* and for example you run this command:
```
pacman -U wine-staging-5.5-1-x86_64.pkg.tar.zst
```

![Logo Pipewire]({{ site.baseurl }}/images/winejoy/pacmanu.png)


## Method 2
### Install a downgrade package
If you dont have *downgrade* install on your system. you can follow this command:
```
yay -S downgrade
```

![Logo Pipewire]({{ site.baseurl }}/images/winejoy/yaydown.png)

This tools can usefull when you have problem with newer package install on your system when is needed next.

### Run downgrade tools
Next you run downgrade tools with following this command:
```
downgrade wine
```
![Logo Pipewire]({{ site.baseurl }}/images/winejoy/downmain.png)

Then you can select what old packages you want to install on your system and after selecting packages you can follow instruction on downgrade tools like using *pacman* package manager.
![Logo Pipewire]({{ site.baseurl }}/images/winejoy/downpac.png)

# Why this happen?
Wine have new a driver for some Joystick that effected Playstation like Joystick. they mapping *L1*/*R1* Button as a *Z,Rz*.
