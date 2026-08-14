---
layout: post
title: Global Menu Firefox
image: /images/202607/main.webp
---

![Fire Fox Global Menu]({{ site.baseurl }}/images/202607/main.webp)

New Firefox now can had a Global menu natively (rolled out in version 138, stable on 139), no needed patch or something
just enable it on `about:config`:
turn on the:
- `widget.gtk.global-menu.enabled` set as `true`
- `widget.gtk.global-menu.wayland.enabled` set as `true`

then restart browser, done!
You must have a plugins/widget, like on KDE Plasma just add Global menu widget.

*Notes: **some spinoff firefox based like waterfox cant show that Globalmenu**
