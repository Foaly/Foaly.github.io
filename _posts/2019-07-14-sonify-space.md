---
title: Sonifying Space
tags: [Building Stuff]
---


Hello again!

I made a new thing and I think it turned out quite cool, so I wanted to share some pictures of the build process and the finished result with you :)

![The finished installation][finished]

Continuing to follow the idea of extending the human senses with technology to create new cyborg senses (like [my Wifi hearing sense][wifi sense]), I wanted to create a new sense that allows you to tune in and listen to the particle showers emitted by our sun.
Similar to how people enjoy listening to the rain I wanted to create an experience that lets you listen to the solar rain.
My first idea was to use a GPS sensor to get your current position and let you listen to the particles directly above you.
Unfortunatelly, but logically, real "movement" in the data happens only every 12 hours with the sun cycle.
So to get some more variance and interactivity I turned it into an installation instead.
As the input I made an interactive map of the world with an intensity overlay.
Choosing a position on the map lets you experience the current solar rain at that point.
The data I used to influence the sound is the total electron count in the ionosphere, which is made [available by the European Space Agency][esa] (ESA) in near real-time.
To make it look nice I took an old CRT monitor and gave it a crashed space ship look.
I already have a few ideas on how to improve it, so maybe I will bring it along to the CCC congress at the end of the year :)


### Description of the installation

> The piece on display is a module recovered from the remains of a crashed spacecraft.
> Studying it revealed it was used by an alien, space fairing civilization to tune into the winds and particle storms of stars.
> It's assumed that this was done for the purpose of pleasure or relaxation, offering space travellers the experience of natural processes during long voyages through the emptiness of interstellar space.
>
> The device was restored and reconfigured to tap into the satellites and ground stations of the European Space Agency.
> Restored to its intended function it now allows the inhabitants of planet earth to experience the pleasure of listening to solar winds and the particle rain of their star.


![Side view][side_view]

----------------

| ![The left side][left_side] | ![The right side][right_side] |
|:---------------------------:|:-----------------------------:|
|                             |                               |

![The map][map]



Build process
-------------

| ![The old monitor][before] | ![Opened up monitor][bare] |
|:--------------------------:|:--------------------------:|
|                            |                            |

![Spray painting in progress][sprayed]

----------------

![Decorated monitor][cables]


[//]: # (here be images)

[finished]: {{ site.url }}/assets/images/sonify_space/finished.png "The finished installation"
[side_view]: {{ site.url }}/assets/images/sonify_space/side_view.png "Side view"
[left_side]: {{ site.url }}/assets/images/sonify_space/left_side.png "The left side"
[right_side]: {{ site.url }}/assets/images/sonify_space/right_side.png "The right side"
[map]: {{ site.url }}/assets/images/sonify_space/map.png "The map"

[before]: {{ site.url }}/assets/images/sonify_space/before.png "The old monitor"
[bare]: {{ site.url }}/assets/images/sonify_space/bare.png "Opened up monitor"
[sprayed]: {{ site.url }}/assets/images/sonify_space/sprayed.png "Spray painting in progress"
[cables]: {{ site.url }}/assets/images/sonify_space/cables.png "Decorated monitor"




[//]: # (here be links)

[wifi sense]: https://foaly.github.io/2018/12/06/wifi-hearing.html "My WIFI sense"
[esa]: http://esc-sso.dlr.de/Total_Electron_Content/TEC_Near_Real-Time/Global-beta/ "My WIFI sense"
