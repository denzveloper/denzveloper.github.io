---
layout: post
title: Modding DVB-T2 Receiver (Astrometa DVB-T2/Realtek RTL2832P)
image: /images/astrm_dt2/img_5.webp
---

![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_5.webp)

I'm trying to experiment for receiving a MW/SW radio receiving with my DVB-T2 dongle with RTL2832P. but when i searching result is only for RTL2832U, then i maybe it works for RTL2832P too. then im doing slash the pcb line on pin 1 RTL2832P (Becareful dont cutting PCB trace!).
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_1.webp)

after that soldering that pcb line and provide a thin cable (on this i use a earphone wire) then make join for cable and pcb line like this image
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_11.webp)
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_10.webp)
for information dont joint the cable to main antenna for best result, want more best grounding the negative cable.

maybe you need a long thin wire like me
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_6.webp)

make sure the joint is solid and secure
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_9.webp)
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_8.webp)

then this is looks like after joining cable with pcb line
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_7.webp)

then put the casing back on
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_5.webp)
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_4.webp)

connect thin wire to other antenna for HF/SW/MW. for easily i using a crocodile clip (after tin iron and solder on the other end of the cable).
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_3.webp)

connect antenna jack for receiving a VHF/UHF
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/img_2.webp)


if want to listening HF frequency using this parameter on gqrx for example. maybe work on other software with with some adjustments
![Modding DVB-T2]({{ site.baseurl }}/images/astrm_dt2/ss.webp)

In action:
<video loading="lazy" width="560" height="315" allow="accelerometer; encrypted-media; gyroscope; picture-in-picture" allowfullscreen src="{{ site.baseurl }}/images/astrm_dt2/video.mp4" controls></video>
<video loading="lazy" width="560" height="315" allow="accelerometer; encrypted-media; gyroscope; picture-in-picture" allowfullscreen src="{{ site.baseurl }}/images/astrm_dt2/video2.mp4" controls></video>
