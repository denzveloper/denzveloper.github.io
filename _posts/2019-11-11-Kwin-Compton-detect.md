---
layout: post
title: Detecting Kwin is running or not for run compton
---

![_config.yml]({{ site.baseurl }}/images/kwincmptn.svg)

Make a "**.sh**" file then add to startup script.

This detecting Kwin is running or not. if Kwin is running, compton not execute. if kwin not detected, compton execute.
Useful for avoid bug when using compton alongside kwin.
