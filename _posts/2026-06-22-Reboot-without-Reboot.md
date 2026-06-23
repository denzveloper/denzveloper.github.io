---
layout: post
title: Reboot without Reboot Kexec
image: /images/kexec/main.webp
---

![Ribut mulu]({{ site.baseurl }}/images/kexec/main.webp)

Needs reboot PC for get new features or needed to load new kernel? but had trouble on it? example for me had error battery, cause when reboot had confirm physicaly (damn you HP 😡) to the laptop when remote. you can use features call kexec.


this kexec program design to load another kernel from the currently executing Linux kernel without cold boot. this tools very useful for you who needed quickly restart without going through the BIOS process (but with this process may cause minor problem, likely me had rtl-sdr usb if they fail can be recovery with this process).


for arch-linux base:
1. first install packages kexec
![Ribut mulu]({{ site.baseurl }}/images/kexec/install.webp)
installation with pacman: `# pacman -S kexec-tools`

2. be root user if you on standard user
![Ribut mulu]({{ site.baseurl }}/images/kexec/su.webp)
run command: `$ sudo su` or `$ su`, if already on root skip this

3. set the image/kernel:
![Ribut mulu]({{ site.baseurl }}/images/kexec/kexec_1.webp)
run command:
```
# kexec -l /boot/vmlinuz-<KERNEL_TARGET> \
                          --initrd=/boot/<UCODE_YOUR_CPU>.img \
                          --initrd=/boot/<KERNEL_TARGET>.img \
                          --append="root=UUID=<PLEASE_INSERT_YOUR_UUID_ROOT_DISK> rw reset_devices loglevel=3
```
or simplest:
`# kexec -l /boot/vmlinuz-linux --initrd=/boot/initramfs-linux.img --reuse-cmdline`

4. Reboot to target kernel
![Ribut mulu]({{ site.baseurl }}/images/kexec/kexec_2.webp)
finish it with:
- `# kexec -e` → **Not recomended**: cause the command will force unmount filesystem (that may cause un-clean state)
- `# systemctl kexec` → **Recomended**: let systemd handle all process unmount-reboot system

