---
layout: single
author_profile: false
permalink: /team/
title: "Our Team"
header:
  #overlay_filter: 0.7 # same as adding an opacity of 0.5 to a black background
  #caption: "Photo: [**Pexels**](https://www.pexels.com/photo/abstract-art-blur-bright-373543/)"
  overlay_image: assets/images/bg.jpg
classes: wide
---

Our team is small but dedicated. If you're interested in collaborating or joining, please speak to [Nussaïbah](mailto:nussaibah.raja.schoob@fau.de).

<h1> Project Leaders </h1>

<div class="teamwrapper">
    {% for author in site.data.authors %}
    <div>
        {% if author[1].avatar %}
        <div class="author__avatar">
            <img src="{{ author[1].avatar }}" alt="{{ author[1].name }}" itemprop="image">
        </div>
        {% else %}
        <div class="author__avatar">
            <img src="/assets/images/anonymous.jpg" alt="{{ author[1].name }}" itemprop="image">
        </div>
        {% endif %}
        <strong>{{ author[1].name }}</strong><br>
        {% if author[1].bio %}
        <i>{{ author[1].bio | markdownify }}</i>
        {% endif %}
    </div>    
    {% endfor %}
</div>
<br>
<h1> Team </h1>

<div class="teamwrapper">
    {% for author in site.data.members %}
    <div>
        {% if author[1].avatar %}
        <div class="author__avatar">
            <img src="{{ author[1].avatar }}" alt="{{ author[1].name }}" itemprop="image">
        </div>
        {% else %}
        <div class="author__avatar">
            <img src="/assets/images/anonymous.jpg" alt="{{ author[1].name }}" itemprop="image">
        </div>
        {% endif %}
        <strong>{{ author[1].name }}</strong><br>
        {% if author[1].bio %}
        <i>{{ author[1].bio | markdownify }}</i>
        {% endif %}
    </div>    
    {% endfor %}
</div>
