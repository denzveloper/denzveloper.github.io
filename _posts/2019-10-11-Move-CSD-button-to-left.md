---
layout: post
title: Moving GTK-CSD to left
---

![_config.yml]({{ site.baseurl }}/images/gtkcsdmove.png)

Moving GTK-CSD close-minimize-maximize button to left for current user:

open *~/.config/gtk-3.0/settings.ini* and add line:

```gtk-decoration-layout=close,minimize,maximize:menu```

then ***logout*** and ***login*** again.
