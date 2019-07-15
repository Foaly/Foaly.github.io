---
title: CrazyPainter
tags: [Software]
redirect_from: "/2017/09/11/crazypainter.html"
---


Hello again!

Today I would like to show you a little software I wrote.
I guess it falls in the category of generative art.

I wrote the software a while back in 2012.
It has since been sitting around a long time and I haven't had a chance to use it much, but recently I had the chance to showcase it at a small music and arts festival so I thought it deserves its own post now.
I used it to project on the backside of the DJ booth.
You can find a full build log with pictures of the DJ booth we built in [this post][dj booth post].

The program is called CrazyPainter (I know I know, very creative name...) and you can find all the code in [my repository][crazypainter repo].
It is licensed under GPL 3.0, so you are free to read it, compile it and use it yourself.

You can use the program interactively using the mouse or you can just let the computer take over to draw the images.
Refer to the [README.md][readme] inside the repo for an overview of the controls.

Screenshots
-----------

Here are a couple screenshot showing different drawing modes, but as always still images don't really do it justice.
You have to see in motion.

![Hermite interpolation mode][hermite screenshot]

![Circle interpolation mode][circle screenshot]

![Jitter interpolation mode][jitter screenshot]

Here are more images from the festival seeing the projection in action.

![The festival][rainbow]

![Projection on the back of the booth and the camp fire][projection fire]

![The projection on the back of the booth][full projection]



[//]: # (here be images)

[hermite screenshot]: {{ site.url }}/assets/images/crazypainter/hermite.png "Hermite interpolation mode"
[circle screenshot]: {{ site.url }}/assets/images/crazypainter/circle.png "Circle interpolation mode"
[jitter screenshot]: {{ site.url }}/assets/images/crazypainter/jitter.png "Jitter interpolation mode"
[rainbow]: {{ site.url }}/assets/images/crazypainter/rainbow.png "The festival"
[projection fire]: {{ site.url }}/assets/images/crazypainter/projection_fire.png "Projection on the back of the booth and the camp fire"
[full projection]: {{ site.url }}/assets/images/crazypainter/full_projection.png "The projection on the back of the booth"


[//]: # (here be links)

[dj booth post]: {{ site.baseurl }}{% post_url 2017-08-27-building-a-dj-booth %} "DJ booth build log post"
[crazypainter repo]: https://github.com/Foaly/CrazyPainter "The CrazyPainter repository"
[readme]: https://github.com/Foaly/CrazyPainter/blob/master/README.md "The CrazyPainter README.md"
