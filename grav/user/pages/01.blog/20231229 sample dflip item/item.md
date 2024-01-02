---
title:  Storm Over Asia rules
subtitle: DearFlip pdf page viewer
date: 2023/12/29
author: John Edwards

hero_classes: text-light title-h1h2 overlay-dark-gradient hero-large parallax
hero_image: soa-cover-front.jpg
show_sidebar: true
published: true 

twig_first: true
process:
    twig: true

taxonomy:
    category: blog
    tag: [games]
---
*[Dearflip]* is a nice pdf page flipper, which animates the page turns and presents a friendly interface to the reader. Getting it working on [grav] is a challenge. I'll update this blog with more details later, but definitely not a simple route.

{% for doc in page.media %}
{% if doc.extension == "pdf" %}
 <div class="_df_book" height="720" webgl="true" backgroundcolor="white" source="{{ doc.url|replace({' ':'%20'}) }}" id="df_manual_book"> </div>
{% endif %}
{% endfor %}  

[grav]: https://wwwgetgrav.org
[dearflip]: https://github.com/dearhive/dearflip-jquery-flipbook