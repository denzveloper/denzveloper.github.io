---
layout: post
title: Teletype brute Kernel Log
image: /images/kernlog_thumb.webp
---

![Message log]({{ site.baseurl }}/images/kernlog_selected.webp)
This message/log always shown while booting? Then when using Teletype/text based mode this message keep distub you while type a prompt and type something?
This is because log level on your boot parameters not set loglevel at "3" or you didn't set it at all.

this step to disable that kernel log:

1. open your terminal then type "```sudo nano /etc/default/grub```"
2. serach for "**GRUB_CMDLINE_LINUX_DEFAULT**"
3. then add "```loglevel=3```" on last word before "``` ' ```"
4. save file with "*ctrl+x*" then "*y*" then "*<enter>*"
5. then run "```sudo update-grub```" or "```grub-mkconfig -o /boot/grub/grub.cfg```"
6. restart for best result :)
