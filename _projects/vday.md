---
layout: page
title: Valentine's Installation
description: Creative Embedded Systems Module 1
img: assets/img/thumbnailmod1.jpeg
importance: 1
category: creative embedded systems
related_publications: false
---

<div class="row justify-content-sm-start">

<div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/desc.png" title="desc image" class="img-fluid rounded z-depth-1 rotate-right" %}
</div>
{% if site.data.repositories.module_one_repo %}

{% for repo in site.data.repositories.module_one_repo %} {% include repository/repo.liquid repository=repo %} {% endfor %}
{% endif %}

</div>

This project offers a queer interpretation of Lana Del Rey lyrics and visualizes the cycle of love and loss.

<div class="row justify-content-sm-center">
<iframe width="853" height="505" src="https://www.youtube.com/embed/NHFYFbRfrQA?si=fEZuPPyt5vdalCZ1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
</div>
<div class="caption">
    Installation on Display
</div>

<div class="row justify-content-sm-center">
    <iframe width="853" height="505" src="https://www.youtube.com/embed/HUqh9DVShdw?si=qKnr0yA7k-TIVgIx" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen> </iframe>
</div>
<div class="caption">
    Full video of Sketch
</div>

#### Artistic Vision

The assignment given was to create a generative art installation that runs on the ESP32 TTGO T-Display with a valentine's day theme to be displayed in the envelope as shown. I choosed to use Lana Del Rey lyrics because she is my favorite artist and many lyrics seem to be talking to a lover which corresponds to the envelope in the installation. I choosed to use hearts and rainbows to represent my personal experiences with love being shaped by queerness. There are three main parts presented in the visual display. In the first part, tiny hearts flood the screen and are randomly colored and placed to represent the unexpectedness and the rush of early stages of love. The second part features a rush or rainbow and Lana Del Rey lyrics related to falling in love and being in love and a heart randomly moving around the screen representing happiness and excitement. The final part features a beating heart and lyrics related to sadness and loss appear. The heart beat slows down and finally the heart breaks and lowers down the screen while the screen dims to black and becomes dormant before repeating the cycle.

#### Technical Challenges

Most of the technical work involved making many small adjustments to convey my artistic vision.
I had to slowly adjust two cirlces and a triangle to make the different sized hearts in the display.
I did a lot of testing and adjustment with the timing for the heart beat in the third part and rate of displaying the tiny hearts in the first part.
I also had to adjust the ranges when the heart moved randomly in the second part and in the final part when moving down the screen.
Creating the breaking heart was one of the more challenging animations because the lines needed to be placed such that they looked right while becoming thicker.
Working with the lyrics which are of varaible length was also challenging. Since I wanted the lyrics to display in a more random placement rather than from the top of the screen to the bottom, I used two lists, a list of lyrics and a list of coordinates, where the index of each list represented the order the lyrics were to be displayed. To do this I initially worked from top to bottom to figure out the coordinates for each lyrics with respect to all the others and then shuffled the contents of both lists so the index of the lyric list and the coordinate list coresponded.
While the process of testing and adjusting was not necessarily challenging or complex it was tedious due to the time neeeded to upload to the ESP32.

## Installing

### [Download the code and envelope](https://github.com/chloeho7/vday-installation-creative-embedded-sys)

<!-- code for GitHub repositories -->

{% if site.data.repositories.module_one_repo %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.module_one_repo %} {% include repository/repo.liquid repository=repo %} {% endfor %}
</div>
{% endif %}

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/pluggingin.jpg" title="plugging in" class="img-fluid rounded z-depth-1 rotate-right" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/inside.jpg" title="inside envelope" class="img-fluid rounded z-depth-1 rotate-image" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/outside.jpg" title="outside envelope" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Connecting to battery and positioning in envelope
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/insidetaped.jpg" title="taping" class="img-fluid rounded z-depth-1 rotate-image" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/outsidetaped.jpg" title="taping outside" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/string.jpg" title="string" class="img-fluid rounded z-depth-1" style="transform: scaleY(-1);" %}
    </div>
</div>
<div class="caption">
    Taping envelope and connecting to string
</div>
