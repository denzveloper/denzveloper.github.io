---
layout: post
title: Moving GTK-CSD to left
---

![CSD Left Like MAC for GTK]({{ site.baseurl }}/images/gtkcsdmove.png)

Moving GTK-CSD (gtk3-CSD) close-minimize-maximize button to left for current user:

open *~/.config/gtk-3.0/settings.ini* and add line:

```gtk-decoration-layout=close,minimize,maximize:menu```

then ***logout*** and ***login*** again.
