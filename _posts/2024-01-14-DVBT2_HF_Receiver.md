---
layout: post
title: Modding DVB-T2 Receiver (Astrometa DVB-T2/Realtek RTL2832P)
image: /images/astrm_dt2/img_5.webp
---

![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_5.webp)

I'm trying to experiment for receiving a MW/SW radio receiving with my DVB-T2 dongle ([Astrometa DVB-T2 version 2018](https://linuxtv.org/wiki/index.php/Astrometa_DVB-T2)) that dongle is include a RTL2832P chip. but when i searching result is only shown tutorial for RTL2832U based chip (DVB-T model), then i thinking its maybe works for RTL2832P chip too. After that im prepare material such as iron solder, tin, cable, knife for peeling/slash the PCB trace and cable. and first is doing *slash (peel) the pcb trace on *"**pin 1**" *RTL2832P* (**Be careful dont cutting that PCB trace!**).
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_1.webp)

after that soldering that pcb trace with tin and provide a thin cable (on this i use a earphone wire) then make join for cable and pcb trace like this image
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_11.webp)
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_10.webp)
for information dont joint the cable to main antenna for best result, want more best result? try grounding the negative antenna polarization or negative trace of turner.

maybe you need a long thin wire like this image
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_6.webp)

make sure the joint is solid and secure (no short circuits of cource)
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_9.webp)
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_8.webp)

then this is looks like after joining cable with pcb trace
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_7.webp)

then put the casing back on
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_5.webp)
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_4.webp)

connect thin wire to other antenna for HF/SW/MW. for easily i using a crocodile clip (after tin iron and solder on the other end of the cable).
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_3.webp)

connect antenna jack for receiving a VHF/UHF (if want to user TV turner too)
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_2.webp)


if want to listening HF frequency using this parameter on gqrx for example. maybe work on other software with with some adjustments. then set receiver to AM/SSB, tune it!
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/ss.webp)

In action:
<video loading="lazy" width="560" height="315" allow="accelerometer; encrypted-media; gyroscope; picture-in-picture" allowfullscreen src="{{ site.baseurl }}/images/astrm_dt2/video.mp4" controls></video>
<video loading="lazy" width="560" height="315" allow="accelerometer; encrypted-media; gyroscope; picture-in-picture" allowfullscreen src="{{ site.baseurl }}/images/astrm_dt2/video2.mp4" controls></video>
