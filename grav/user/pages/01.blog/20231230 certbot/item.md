---
title: Web certificates
subtitle: certbot
date: 2023/12/30
author: John Edwards

hero_classes: text-light title-h1h2 overlay-dark-gradient hero-large parallax
hero_image: letsencrypt.png
show_sidebar: true
published: true 

taxonomy:
    category: blog
    tag: [tech]
---
At simpubs towers we have a number of web sites, some hosted and some running locally and published.
Web *certificates* confirm the ownership of a web page (and not much else...). However, if a web page does not have a nice little padlock in the menu bar, some visitors will be scared away.  
The answer to fear is a certificate from [LetsEncrypt]. I have (finally) managed to make the *wildcard* issue really easy with  

```$ sudo certbot certonly --manual --preferred-challenges=dns --email dummy@example.com --server https://acme-v02.api.letsencrypt.org/directory --agree-tos -d *.example.com```

This will prompt for a DNS `TXT` record to be setup on your domain, called `_acme-challenge` which can be checked with Google tools at [acme example] 

The setup will depend on your provider.

[acme example]: https://toolbox.googleapps.com/apps/dig/#TXT/_acme-challenge.jzedward.com
[letsencrypt]: https://letsencrypt.org