---
layout: post
title: Orion Browser 0.4.1
image: /images/202607/orion041.webp
---

![Orion041]({{ site.baseurl }}/images/202607/orion041.webp)

Orion Browser version 0.4.1 had been released! now with the distibuted url flatpak for auto update, currently avaiable under dedicated Orion Browser team repository (unavaiable under flathub repository).

if you dont have flatpak installed in your system you can follow the instructions here: [https://flathub.org/en-GB/setup]

are you had already installed flatpak in your system then next step required to have a autoupdate under their dedicated server:
1. add beta repository of Orion Browser:
`flatpak remote-add --if-not-exists orion-beta https://flatpak.orionbrowser.com/orion-beta.flatpakrepo`


2. Installing a Orion Broser via Flatpak into your system
`flatpak install orion-beta com.kagi.Orion`


3. if had a newest Orion Brower Beta released you can update it via
`flatpak update` or if only for orion: `flatpak update com.kagi.Orion`. checking avaiable version by: `flatpak remote-info orion-beta com.kagi.Orion`

Other features update what i tested:
1. Download functionality
2. Private Browsing Window support
3. Local Sync
4. Custom Search
5. Password Management, and any others improvement..

You can test by yourself! :D
