---
layout: post
title: CSD gap space Firefox Problem in KDE
---

![_config.yml]({{ site.baseurl }}/images/ssff.png)

## Disclamer
This **doesnt working on Firefox v.66**

## Configuration
Modify file ***userChrome.css*** on */home/USER/.mozilla/firefox/[profile-id].default/chrome/userChrome.css*. if doesnt exists you can create that.

The file should contain these lines:
```
/* Hide Menu Bar */
#toolbar-menubar {
  display: none !important;
}

/* Show Window Control Button on Tab Bar */
#toolbar-menubar[autohide="true"]:not([inactive]) + #TabsToolbar > .titlebar-buttonbox-container {
  visibility: visible !important;
}
```