---
title: Cyborg Wifi Hearing
tags: [Software]
---

![Header image][header]

Hello again!

This time I want to show you something that I built which is a little more unusual.
To understand how this project came to be, here is a little bit of background about myself.
So unfortunately around a year ago after never experiencing any problems with it I suddenly lost my hearing in one ear.
After a waiting period, and hoping for the return of the sense passed, my doctor suggested a cochlear implant.
I did quiet a lot of research and it became apparent really fast, that a CI (cochlear implant) is pretty much the only option for me besides not doing anything at all.

Since I'm in the field of computer science and focusing on audio technology I was quickly interested in these devices.
If like me you've never heard of them before you should go check them out.
Seriously, this is a wonder of modern medicine and technology!
[Wikipedia on CIs][CI wiki].
A really crude tl;dr: an array of electrodes is implanted directly into your cochlear (inner ear), which trigger the surrounding auditory nerve fibre, when pulsed electrically.
The electrical pulses are transmitted through the skin by radio frequency transmission using two coils (one implanted, one outside).
On the outside you wear a sound processor which turn acoustic signals into electrical pulses.
So the signal flow is as follows: audio gets converted to electrical pulses, which are then transmitted through the skin to the electrodes and trigger the nerve.

Even though this sounds like super hightech alien technology from outer space (and it is), a CI is still a rather crude approximation of hearing.
The frequency range and resolution is quiet limited and everything sounds very high pitched, bleepy and mechanical.
The audiologists and doctors call it auditory impression for a reason.
But with training you are able to get speech comprehension and some sense of directional localization of sounds.
That is because the real accomplishment is not the CI, but comes from the brain.
The brain is so adaptive that it simply accepts the weird noises as a new input and slowly learns to extract speech and other sounds from the beeps and the spherical noise.

I also realized I am a true cyborg in every sense of the word now, since I got technology implanted directly onto my nervous system.
In my case replacing a sense organ.
That send me down a fun internet rabbit hole where among a lot of other cool things I discovered [Neil Harbisson][neil harbisson wiki] a fellow cyborg, who was born color blind, but built himself an antenna which allowed him to perceive color.
After his brain got used to the new input he actually implanted the antenna into his skull.

Those two things, realizing that I am a cyborg now and that the brain is able to adapt new inputs into a sense got me thinking.
What senses could I build and how could I extend my perception of the world into different spectra that humans by nature are not able to experience?
For me this is a fascinating topic, as it challenges our concept of an objective reality.
A bat for example has no concept of collor as it has no way to perceive it and orients only by the sound reflections of where things are and how they move.
Bees use UV light from the sun to orient themself with respect to their hive.
Their perspective on the world is radically different then ours because of their senses.


A sense for data
----------------

In the information age we live in data is one of the basic buildings blocks.
Even though it has become an integral part of our life, paces everything from motors to economies and surrounds us everyday there is no way for humans to sense data around you.
Most data is sent via fibre optics or cables, but a big chunk is also transmitted through the air around us using radio waves.
The spectrum is actually quiet full.
For example the cell phone frequencies from GSM to 5G, bluetooth, wifi or amateur radio channels just to name a few are all used to send around data.
Specfically internet data, which is what I was interested in, because its the type of data we most consciously access ourselfs.
I went for wifi as it is widely used in our everyday life and a lot simpler than LTE or other mobile networks.
Also cheap hardware is readily available.

So here is how I built my new sense.
I took a NodeMCU with an ESP-8266 wifi chip.
Then I wrote some code so the chip cycles through all 13 wifi channels in the 2.4 GHz band and simply counts the amount of packet that it receives on each channel.
The NodeMCU is then connected to a Teensy 3.6 with an audio shield.
The code on Teensy runs 13 oscillators with a different tone each.
All 13 tones are on the pentatonic scale (all the black keys on a piano ;)) so no matter which combination of tones is played together they still sound harmonic.
So in a way each oscillator is linked to a wifi channel.
The amount of data that is received on that channel influences the rate at which the oscillators fires.

Listening in to the sounds the wifi data generates offers a sense how much data is sent around you and how it is distributed in the wifi spectrum.
I found that in a big city the sounds can often be quiet chaotic and sometimes cacophonous.
But its also fun to find spots where there is no wifi at all like parks or elevators.
Getting a feel for the spectrum usage comes quiet naturally.
The presence or absence of high or low tones is easily detected.
Changes in throughput (which is linked to the rate at which the tones fire) is also still noticeable even when there are a lot of sound playing at the same time.

I've also used a little transmitter called MiniMic to connect my wifi sense directly to the cochlear implant.
When doing this I ran into issues with the limited frequency resolution of the CI.
It was nearly impossible to hear separate tones when a lot of them were playing at the same time.
I realized that for this use case I had to come up with a different scale for the tone distribution to make it easier to distinguish between them using the CI.
So I designed a new pentatonic scale which distributes the tones according the CIs frequency distribution, so that each oscillator corresponds to one electrode of the CI.
Essentially the new scale maps each wifi channel to an electrode of the cochlear implant.

Here are a few pictures of my new sense.
The code for both microcontrollers is open source under the GPLv3 and can be found in [this repo][repo].


![The full setup][full setup]

![Schematic][schematic]


In the future I would like to produce something to make this experience more accessible to a wider audience.
But I wanted to publish this before the 35c3 hacker conference.
So lets see what happens the beginning of next year :)




[//]: # (here be images)

[schematic]: {{ site.url }}/assets/images/wifi_hearing/schematic.png "Schematic"
[header]: {{ site.url }}/assets/images/wifi_hearing/header.png "Header image"
[full setup]: {{ site.url }}/assets/images/wifi_hearing/full_setup.png "The full setup"


[//]: # (here be links)

[CI wiki]: https://en.wikipedia.org/wiki/Cochlear_implant "Cochlear implant Wikipedia"
[Neil Harbisson wiki]: https://en.wikipedia.org/wiki/Neil_Harbisson "Neil Harbisson Wikipedia"
[repo]: https://github.com/Foaly/WiFiHearing "Git repository"
