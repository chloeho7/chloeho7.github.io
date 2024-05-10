---
layout: page
title: Persistience of Vision Display
description: Creative Embedded Systems Module 3
img:
importance: 3
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
