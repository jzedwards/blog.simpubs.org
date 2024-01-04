---
title: Flat Top
subtitle: by Avalon Hill
date: 2024/01/04
author: John Edwards

hero_classes: text-light title-h1h2 overlay-dark-gradient hero-large parallax
hero_image: flattop-map-crop.png
show_sidebar: true
published: true 

twig_first: true
process:
    twig: true

taxonomy:
    category: blog
    tag: [games, ah]
---
A friend requested a rules copy for *Flat Top* ([bgg]) by Avalon Hill on [Facebook] so I revisited my scans and joined the maps. Files are available on [simpubs], including hi quality scans and a *complete* pdf. Rules below formatted for *Dearlip*.

{% for doc in page.media %}
{% if doc.extension == "pdf" %}
 <div class="_df_book" height="720" webgl="true" backgroundcolor="white" source="{{ doc.url|replace({' ':'%20'}) }}" id="df_manual_book"> </div>
{% endif %}
{% endfor %}  

[simpubs]: https://nextcloud.simpubs.org/s/kPDtFYfDA7LQxRf
[facebook]: https://www.jzedward.com
[bgg]: https://www.example.com