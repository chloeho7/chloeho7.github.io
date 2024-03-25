---
layout: page
title: prisma odyssey
description: Creative Embedded Systems Module 2
img: assets/img/triangle.png
importance: 1
category: creative embedded systems
---

<div class="row justify-content-sm-start">

{% if site.data.repositories.module_two_repo %}

{% for repo in site.data.repositories.module_two_repo %} {% include repository/repo.liquid repository=repo %} {% endfor %}
{% endif %}

</div>

<div class="row justify-content-sm-center">
<iframe width="853" height="505" src="https://www.youtube.com/embed/c69II9nHpro?si=iewPPxSCMrowyJwS" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>
<div class="caption">
    Gameplay of Prisma Odyssey
</div>

#### Artistic Vision

The assignment given was to create an interactive device that runs off wired power and sends data back to a machine for media generation. It was required to connect components to an ESP32 and create an enclosure for the device. From a software perspective, an ESP32 program that collects and sends sensor data using a serial connection and a media generation program was required.

This work was largely inspired by [The Catacombs of Solaris](https://ianmaclarty.itch.io/catacombs-of-solaris-original) which I learned about from visiting [ACMI](https://www.acmi.net.au/works/61402--the-catacombs-of-solaris/) in 2023. I wanted to create a 3D game and was inspired by the illusion inducing, hynotic, and trippy nature of The Catacombs of Solaris. I was also inspired by my own art peices that featured triangles of various shapes and monochromatic shades.

<div class="row justify-content-sm-center">
    {% include figure.liquid path="assets/img/greentriart.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
<div class="caption">
    Gameplay of Prisma Odyssey
</div>

I initially wanted to create a 3D space of triangular prisms that could be explored and climbed on. When researching how to create a 3D game
with pygame, I found a [stackoverflow post](https://stackoverflow.com/a/58675007) that demoed a 3D sky of stars. I iterated from here, transforming the stars into triangles of randoms shapes, shades and sizes and was struck by the kalidescopic effect that was created. To add onto the effect, I added a random mix of different colors each level and music that is relaxing and hypnotic. I wanted the game to be minimalistic so there is no seperate directions. I created display of the pieces that need to be collected and have been collected to imply to goal of the game. I also added a sound effect for when the player collects a piece and when a level is complete. For accessibility, I included a WASD control scheme so the game could be played without the joystick.

#### Technical Challenges

In the same vein, also address any technical issues you encountered in your work. Particularly focus on issues that other artists may encounter when developing with your hardware setup.

DECISIONS: more colors, displaying information, kalidescope, trippy, hypnoitc , music, SFX, goal, learning, mininal, focus, 3D, ergonomic, protottyping, accessibility, contrast, WASD

Wires , prototyping, serial, timing, adjusitng randomness, difficulty, freeze bug, collecting logic, stackoverflow math

Most of the technical work involved making many small adjustments to convey my artistic vision.
I had to slowly adjust two cirlces and a triangle to make the different sized hearts in the display.
I did a lot of testing and adjustment with the timing for the heart beat in the third part and rate of displaying the tiny hearts in the first part.
I also had to adjust the ranges when the heart moved randomly in the second part and in the final part when moving down the screen.
Creating the breaking heart was one of the more challenging animations because the lines needed to be placed such that they looked right while becoming thicker.
Working with the lyrics which are of varaible length was also challenging. Since I wanted the lyrics to display in a more random placement rather than from the top of the screen to the bottom, I used two lists, a list of lyrics and a list of coordinates, where the index of each list represented the order the lyrics were to be displayed. To do this I initially worked from top to bottom to figure out the coordinates for each lyrics with respect to all the others and then shuffled the contents of both lists so the index of the lyric list and the coordinate list coresponded.
While the process of testing and adjusting was not necessarily challenging or complex it was tedious due to the time neeeded to upload to the ESP32.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
