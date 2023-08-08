---
layout: post
title: Teletype brute Kernel Log
image: /images/logkernel/kernlog_thumb.webp
---

![Message log]({{ site.baseurl }}/images/logkernel/kernlog_selected.webp)

This message/log always shown while booting? Then when using Teletype/text based mode this message keep distub you while type a prompt and type something?
This is because log level on your boot parameters not set loglevel lower than "3" or you didn't set it at all.

this step to disable that kernel log (Tested on Arch-based distro):

1. open your terminal then type "```sudo nano /etc/default/grub```"
![open file grub config]({{ site.baseurl }}/images/logkernel/runrunrun.webp)

2. serach for "**GRUB_CMDLINE_LINUX_DEFAULT**"

3. then add "```loglevel=3```" on last word before "``` ' ```"
![Set loglevel]({{ site.baseurl }}/images/logkernel/grub_terminal.webp)

4. save file with "*ctrl+x*" then "*y*" then "*<enter>*"

5. then run "```sudo update-grub```" or "```grub-mkconfig -o /boot/grub/grub.cfg```"
![Updating grub configuration]({{ site.baseurl }}/images/logkernel/update-in-grub.webp)

6. restart for best result :)
![Results]({{ site.baseurl }}/images/logkernel/kernlog_done.webp)
