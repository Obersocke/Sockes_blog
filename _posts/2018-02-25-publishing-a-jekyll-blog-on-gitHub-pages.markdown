---
layout: post
title:  "Publishing a Jekyll-Site on Gihub Pages"
date:   2018-02-25 11:55:33 +0100
categories: jekyll update
---

Requirements: 

- [git installed][git-installation] locally
- [jekyll installed][jekyll-docs-intallation] locally
- [Github][git-hub] Account

Create a new Jekyll Project

    jekyll new <projectName>

Go into your new project and reate a new local git repository

    cd <projectName>
    git init

Create a new branche and checkout

    git checkout -b gh-pages

Go to _config.yml in your project and set the baseUrl.
Put in any folder-name you like or your personal domain (haven't tried that yet) like so:

{% highlight ruby %}
baseurl: "/sockes_blog" 
# or wathever you want as the subpath of your site, e.g. /blog
{% endhighlight %}

Create a new repository on git hub and connect it to your local repository

    git remote add origin https://github.com/<github-username>/<repository-name>.git

Push local repo to Github

    git add .
    git commit -m "<message>"
    git push -u origin gh-pages


Now you can reach your site under:

https://\<github-username\>.github.io/\<baseUrl-you-set-before\>/


e.g. in my case :

[https://obersocke.github.io/sockes_blog/][self-link]

[jekyll-docs-intallation]: https://jekyllrb.com/docs/installation/
[git-installation]:   https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
[git-hub]: https://github.com/
[self-link]: https://obersocke.github.io/sockes_blog/

