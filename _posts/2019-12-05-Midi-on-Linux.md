---
layout: post
title: MIDI playback on Linux
---

![_config.yml]({{ site.baseurl }}/images/midi_logo.jpg)

## Installation
Use your package manager to install FluidSynth and some soundfonts to use (**freepats-general-midi** or **soundfont-fluid**).
In Arch based family you can use the following command:

    sudo pacman -S fluidsynth soundfont-fluid

## systemd FluidSynth service

You must set a default soundfont with the following command:

    ln -s /usr/share/soundfonts/FluidR3_GM.sf2 /usr/share/soundfonts/default.sf2

You may want to start the MIDI synth automatically when you log in your desktop, so you can play midi in media player right away. If your distro is using systemd, you may set up a service file for your user only.

Create the file in systemd directory, in this exact location: `~/.config/systemd/user/fluidsynth.service`.
The file should contain these lines:

```
[Unit]
Description=FluidSynth launched in server mode
After=sound.target

[Service]
ExecStart=/usr/bin/fluidsynth -a pulseaudio -m alsa_seq -i -l -s -p FluidSynth /usr/share/soundfonts/default.sf2

[Install]
WantedBy=default.target
```

This command will start fluidsynth as a server process, using pulseaudio as audio driver and a port named FluidSynth.
You may have to adapt above command to your system.

Let systemd find the new unit file and start the service:

    systemctl --user daemon-reload
    systemctl --user start fluidsynth.service

If it works correctly, you can enable the service to let it start at login:

    systemctl --user enable fluidsynth.service

You can then stop it or disable it at any time with the following commands:

    systemctl --user stop fluidsynth.service
    systemctl --user disable fluidsynth.service
