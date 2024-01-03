---
title: 1942 Compass rework
subtitle: Paper Wars article
date: 2024/01/03
author: John Edwards

hero_classes: text-light title-h1h2 overlay-dark-gradient hero-large parallax
hero_image: 1942-hero.png
show_sidebar: true
published: true

twig_first: true
process:
    twig: true

taxonomy:
    category: blog
    tag: [games, gdw]
---
*1942* ([BGG] link) was a classic [Series 120] game from GDW, as part of the 1940/1941/1942 collection. This series is being re-issued by [Compass] Games, and was the subject of a recent *[Paper Wars]* article which Ty Bomba shared on [Facebook], available below

{% for doc in page.media %}
{% if doc.extension == "pdf" %}
 <div class="_df_book" height="720" webgl="true" backgroundcolor="white" source="{{ doc.url|replace({' ':'%20'}) }}" id="df_manual_book"> </div>
{% endif %}
{% endfor %}  

[Facebook]: https://www.facebook.com/jzedward
[Compass]: https://www.compassgames.com/product/wwii-campaigns-1940-1941-and-1942-pay-later/
[BGG]: https://boardgamegeek.com/boardgame/6915/1942
[Series 120]: https://boardgamegeek.com/geeklist/1538/gdw-series-120-games
[sample]: https://www.example.com