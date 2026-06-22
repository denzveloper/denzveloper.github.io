---
layout: post
title: PiAware SkyAware Home Server Public
image: /images/piawai/q.webp
---

![PiAware]({{ site.baseurl }}/images/piawai/q.webp)

Hello all! Now i want to share my Areoplane tracking project to you all!
the porject itself still under heavy developent especially hardware sector, on software sector is currently had no problem.
for currently conditions hardware is still using an cheap RTL-SDR [from this project]({{ site.baseurl }}/DVBT2_HF_Receiver) (Astrometa DVB-T2 Devices), and for antenna is currently using a UHF TV Antenna (may this antenna not proper for receive GigaHertz frequency - 1090MHz frequency), and that will cause detection get only nearest areoplane can be reach and had only certain conditions (altitude, weather, speed, and distance had very depend). and next time i will upgrade all equipment for better received. for the software sector is i use docker and with following image: egortensin/dump1090, egortensin/fr24feed, ghcr.io/sdr-enthusiasts/docker-piaware, ghcr.io/sdr-enthusiasts/docker-adsbexchange, ghcr.io/sdr-enthusiasts/docker-opensky-network, ghcr.io/sdr-enthusiasts/docker-airnavradar, ghcr.io/sdr-enthusiasts/docker-planefinder, caddy(Web Proxy), ghcr.io/techarohq/anubis (Thanks to all authors for the docker package!); futher more for build on this article [here]({{ site.baseurl }}/Airplane-Tracking-Device).


## Availability
<i class="svg-icon maps"></i>

Availability Publicly for the project is on this list (Currently can be reach by IPv6 only! IPv4 unavailable! Please contacts your ISP for availability):
1. [PiAware SkyAware Web](https://dzen2x.freeddns.org:8888/)
2. [dump1090 (RAW Format)](dzen2x.freeddns.org:30002)
3. [dump1090 (BaseStation Format)](dzen2x.freeddns.org:30003)
4. [dump1090 (Beast Format)](dzen2x.freeddns.org:30005)

Others port is open for frontend, but i dont recomended. cause that currenly on trials (without https/secure too) device may unstable and may be sometime cant be reach, for better use above ports/address.


## Others
futher more will be update
*Updated: 2026-06-22*
