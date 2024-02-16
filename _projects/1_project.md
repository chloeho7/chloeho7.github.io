---
layout: page
title: Valentine's Installation
description: creative embedded systems module 1
img: assets/img/12.jpg
importance: 1
category: creative embedded systems
related_publications: false
---

video of mine

<iframe width="420" height="315" src="https://youtu.be/embed/HUqh9DVShdw?si=chUFBxynGYgAitGe" frameborder="0" allowfullscreen="allowfullscreen">&nbsp;</iframe>

<iframe width="560" height="315" src="https://www.youtube.com/embed/HUqh9DVShdw?si=qKnr0yA7k-TIVgIx" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen> </iframe>

This project offers a queer interpretation of Lana Del Rey lyrics and visualizes the cycle of love and loss.
There are three main parts presented. The first part uses tiny that flood the screen and are randomly colored and placed to represent the unexpectedness and the rush of early stages of love. The second part features a rush or rainbow and Lana Del Rey lyrics related to falling in love and being in love and a heart randomly moving around the screen representing happiness and excitement. The final part features a beating heart and lyrics related to sadness and loss appearing. The heart beat slows down and finally the heart breaks and lowers down the screen while the screen dims to black and becomes dormant before repeating the cycle.

video of the installation

blah blah

process of making pictures

### [Download the code](https://github.com/chloeho7/vday-installation-creative-embedded-sys)

<!-- code for GitHub repositories -->

{% if site.data.repositories.module_one_repo %}

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.module_one_repo %} {% include repository/repo.liquid repository=repo %} {% endfor %}
</div>
{% endif %}

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

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
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
