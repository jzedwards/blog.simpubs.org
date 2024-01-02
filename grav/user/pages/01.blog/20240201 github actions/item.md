---
title: Github actions
subtitle: ftp automagically
date: 2000/01/01
author: John Edwards

hero_classes: text-light title-h1h2 overlay-dark-gradient hero-large parallax
hero_image: github-actions.png
show_sidebar: true
published: true 

taxonomy:
    category: blog
    tag: [tech]
---
The *simpubs* tech team (ie [jzedward]) have been working on how to easily edit and deploy new blog posts to this site. It is hosted on [x10], a free (as in beer) service, which only has ftp available to load content.  

However, the brilliant [ftp deploy] provides a way to automagically update from a [github] repository (aka repo) to ftp. The code below is added as a *github action* to [blog.simpubs.org] (which has the entire site and a Docker container script to build it) - and the action loads directly to [x10].

**Note:** the code below has `dry-run` set to `true` so will only check differences, not load
```
on: push
name: 🚀 Deploy website on push
jobs:
  web-deploy:
    name: 🎉 Deploy
    runs-on: ubuntu-latest
    steps:
    - name: 🚚 Get latest code
      uses: actions/checkout@v3
    
    - name: 📂 Sync files
      uses: SamKirkland/FTP-Deploy-Action@v4.3.4
      with:
        server: jzedward.x10host.com
        username: ${{ secrets.x10username }}
        password: ${{ secrets.x10usernamefreepassword }}
        dry-run: true
        server-dir: domains/jzedward.x10hosting.com/public_html/user/pages
        local-dir: ./grav/user/pages/
```


[blog.simpubs.org]: https://github.com/jzedwards/blog.simpubs.org
[ftp deploy]: https://github.com/SamKirkland/ftp-deploy
[x10]: https://www.x10hosting.com
[jzedward]: https://jzedwards.github.io
[github]: https://github.com/jzedwards