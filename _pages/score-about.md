---
layout: page-with-background
title:  "About ossia score"

permalink: /score/about.html
category: "site-score"
---

<h3><a href="https://github.com/ossia/score" target="_blank" >ossia score</a> is a sequencer for audio-visual artists, designed to enable the creation of interactive shows, museum installations, intermedia digital artworks, interactive music and more in an intuitive user interface.</h3>


<br/>
<img class="post-image" src="/assets/score.png" />

It allows to sequence OSC, MIDI, DMX, sound files and more, between multiple software and hardware.
Its novel interactive timeline enables scores written with it to depend on external events and controls through a simple visual language.

ossia score is free, libre & open source software and runs on desktop (Windows / macOS / Linux), mobile and embedded.
It leverages [libossia](../site-libossia/about.html) for its implementation, as well as reputed open-source technologies such as Qt 5, Boost and LLVM. It is written primarily in modern C++.

<br/>
<p align="center">
<a href="/score/download.html" class="page-button" style="padding-left:4em;padding-right:4em;font-size: 27px;" >Download score !</a>
</p>

## License
ossia score is distributed under the terms of the CeCILL license. The french CeCILL license allows the software to be used under the terms of the GNU GPLv3.

## Funding
You can fund the development of ossia on [OpenCollective](https://opencollective.com/ossia).



{% assign cats = "Structure|Audio|Controls|Graphics|Interoperability|Presentation|Scripting|Software model" | split: '|' %}

<div>
    {% for ct in cats %}
         <h2 class="feature-title">{{ ct }}</h2>
         <div class="features-list">
        {% for post in site.score_features %}
            {% if post.tag contains ct %}
            {% if post.visible %}
                <a href="https://ossia.io/score-docs{{post.doclink}}" class="thumbnail dark" >
                    <h1 class="blog-title" style="margin-bottom: 0.4em;">{{post.title}}</h1>
                    <img class="thumbnail-feature" src="/assets/blank.png" alt="{{post.title}}" data-echo="{{post.image}}"  width="auto"/>
                    <span class="feature-description">{{post.description}}</span>
                </a>
            {% endif %}
            {% endif %}
        {% endfor %}
        </div>
    {% endfor %}
</div>

{% include lazyload.html %}
