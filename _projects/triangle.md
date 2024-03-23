---
layout: page
title: triangle game
description: Creative Embedded Systems Module 2
img: assets/img/Screen-Recording-2024-03-21-at-11.29.59-AM.gif
importance: 2
category: creative embedded systems
---

<div>
{% if site.data.repositories.module_two_repo %}

{% for repo in site.data.repositories.module_two_repo %} {% include repository/repo.liquid repository=repo %} {% endfor %}
{% endif %}

</div>

Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

#### Artistic Vision

The assignment given was to create a generative art installation that runs on the ESP32 TTGO T-Display with a valentine's day theme to be displayed in the envelope as shown.

The goal is to create an interactive device with the provided hardware. The devices will run off wired power and send data back to your laptop for visualization, sonfication, or whatever media generation process you prefer.

From a hardware perspective, you will need to connect the specified components to the ESP32 and create an enclosure for the device. From a software perspective, you will write an ESP32 program that collects sensor data and sends it over either a serial or wifi connection to a laptop. You will also write a media generation program on your laptop to handle this data and create something interesting with it.

What creative decisions did you work lead you to, and which decisions did you take? How were your decisions motivated by your larger creative vision for this project. In the same vein, also address any technical issues you encountered in your work. Particularly focus on issues that other artists may encounter when developing with your hardware setup.



This work was largely inspired by [The Catacombs of Solaris](https://ianmaclarty.itch.io/catacombs-of-solaris-original) and Kalidescopes.

I choosed to use Lana Del Rey lyrics because she is my favorite artist and many lyrics seem to be talking to a lover which corresponds to the envelope in the installation.

I choosed to use hearts and rainbows to represent my personal experiences with love being shaped by queerness. There are three main parts presented in the visual display. In the first part, tiny hearts flood the screen and are randomly colored and placed to represent the unexpectedness and the rush of early stages of love. The second part features a rush or rainbow and Lana Del Rey lyrics related to falling in love and being in love and a heart randomly moving around the screen representing happiness and excitement. The final part features a beating heart and lyrics related to sadness and loss appear. The heart beat slows down and finally the heart breaks and lowers down the screen while the screen dims to black and becomes dormant before repeating the cycle.

#### Technical Challenges

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
