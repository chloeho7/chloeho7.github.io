---
layout: page
title: Prisma Odyssey
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

Prisma Odyssey is an Experimental Art Exploration Game Designed for 16-inch Macbook and Joystick (also supports WASD+SPACE controls and other sized screens) using [Pygame](https://www.pygame.org/)

<div class="row justify-content-sm-center">
<iframe width="853" height="505" src="https://www.youtube.com/embed/c69II9nHpro?si=iewPPxSCMrowyJwS" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>
<div class="caption">
    Gameplay of Prisma Odyssey
</div>

#### Artistic Vision

The assignment given was to create an interactive device that runs off wired power and sends data back to a machine for media generation. It was required to connect components to an ESP32 and create an enclosure for the device. From a software perspective, an ESP32 program that collects and sends sensor data using a serial connection and a media generation program was required.

This work was largely inspired by [The Catacombs of Solaris](https://ianmaclarty.itch.io/catacombs-of-solaris-original) which I learned about from visiting [ACMI](https://www.acmi.net.au/works/61402--the-catacombs-of-solaris/) in 2023. I wanted to create a 3D game and was inspired by the illusion inducing, hynotic, and trippy nature of The Catacombs of Solaris. I was also inspired by my own art peices that featured triangles of various shapes and monochromatic shades.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/greentriart.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   My Artwork from 2020 
</div>

I initially wanted to create a 3D space of triangular prisms that could be explored and climbed on. When researching how to create a 3D game
with pygame, I found a stackoverflow [post](https://stackoverflow.com/a/58675007) that demoed a 3D sky of stars. I iterated from here, transforming the stars into triangles of randoms shapes, shades and sizes and was struck by the kalidescopic effect that was created. To add onto the effect, I added a random mix of different colors each level and music that is relaxing and hypnotic. I wanted the game to be minimalistic so there is no seperate directions. I created display of the pieces that need to be collected and have been collected to imply to goal of the game. I also added a sound effect for when the player collects a piece and when a level is complete. For accessibility, I included a WASD control scheme so the game could be played without the joystick.

#### Technical Challenges

The wiring for the joystick was a little difficult to figure out because the joystick in the enclosure is at a different orientation than the default. So the x and y axis were switched and used different ranges for each direction. I had to adjust the wiring and arduino code to account for this.

The most difficult part of the software was creating the 3D projection in the game. Since pygame does not have a built in 3D engine, I used the formula for 3D projection from [this](https://stackoverflow.com/a/58675007) stackoverflow post. I had to adjust the formula to create rotated triangles and to ensure the triangles were displayed in the correctly.

Timing the data sent via the serial connection, with the game frame rate was also a challenge. I had to adjust the delay between each time data was sent from the ESP32 to my pygame program to ensure the game ran smoothly with minimal errors. I also had issues with the game freezing and was able to fix this bug by checking that the points of each triangle were in the range of the screen.

Another challenge I faced was figuring out how to allow the player to collect triangles when they were close to the triangle. I came up with checking if the triangle took up a significant amount of the screen and allowed the player to collect the triangle if it did. I had to make various small adjustments to the range the triangles can be spawned and the range the player can collect the triangles to make the game challenging but not impossible.

When creating the enclosure I wanted to make sure the joystick could be used ergonomically with just one hand. I also wanted the enclosure to be easy to assemble without many peices. I created many prototypes to ensure that the joystick had a full range of motion and was comfortable to use. I started by taping peices together before gluing. I also wanted to make sure the ESP32 could be accessed in the enclosure so the enclosure needed to be able to open.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/prototype1.jpg" title="example image" class="img-fluid rounded z-depth-1 rotate-right" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/prototype2.jpg" title="example image" class="img-fluid rounded z-depth-1 rotate-right" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/prototype3.jpg" title="example image" class="img-fluid rounded z-depth-1 rotate-right" %}
    </div>
</div>
<div class="caption">
    Prototypes of the enclosure
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/enclosureelevator.jpg" title="example image" class="img-fluid rounded z-depth-1 rotate-right" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/playing.jpg" title="example image" class="img-fluid rounded z-depth-1 rotate-right" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/enclosurelights.jpg" title="example image" class="img-fluid rounded z-depth-1 rotate-right" %}
    </div>
</div>
<div class="caption">
   Finished Enclosure! 
</div>

## Installing

### [Download the code and get enclosure instructions](https://github.com/chloeho7/prisma-odyssey)

<!-- code for GitHub repositories -->

{% if site.data.repositories.module_two_repo %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.module_two_repo %} {% include repository/repo.liquid repository=repo %} {% endfor %}
</div>
{% endif %}
