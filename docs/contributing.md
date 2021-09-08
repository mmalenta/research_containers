---
layout : default
name: "contributing"
title: "Contributing"
permalink: contributing
---

# {{ page.title }}

This website is based on Jekyll and Liquid. This helps us to automate a large
portion of task when adding new content. However, there are still a few 
steps and conventions that have to be followed in order to succesfully
add new resources. These are described in detail below. If you do not follow
them, **your PR may be rejected**. In the future we plan to provide scripts
that will further automate the process of adding new content. Also please
do raise an issue, if you have an idea on how to make this process more
accessible and user friendly! Other than that, feel free to create a fork
of this project and start experimenting!

If you are new to Jekyll and Liquid please look at these quick tutorials:

  * [GitHub Pages introduction to Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll) - this page has some basic introduction to Jekyll. You do not need to
  worry too much about sections on setting the pages up - it's already done!
  The main sections of interest are [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)
  and [Adding content to your GitHub Pages site using Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-content-to-your-github-pages-site-using-jekyll)
  * [GitHub Markdown](https://guides.github.com/features/mastering-markdown/) - this one
  one is the most important one as most of your contributions will depend heavily on Markdown
  * [Jekyll Step by Step Tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/) - here
  you should focus mainly on [short introduction to Liquid](https://jekyllrb.com/docs/step-by-step/02-liquid/), 
  [front matter](https://jekyllrb.com/docs/step-by-step/03-front-matter/) and
  [layouts](https://jekyllrb.com/docs/step-by-step/04-layouts/)
  * [Liquid](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers) - **this 
  one is optional** and necessary only if you are interested in improving
  the website build process.

## Layout

Current approach to layout is to make it "just work". We are using a modified
[minimal theme](https://github.com/pages-themes/minimal). Main modifications
include move to a dark(er) theme and changes to some layouts. There are a
number of things that can be improved though. If you are more into design than
containers (or both equally), we welcome contributions to the page layout. 
We are especially interested in contributions from designers and developers
with experience in **making pages more accessible**.

The default laout is the same as the original one. If you want to override it,
please create a local copy in the `_layouts` directory. This directory
currently contains two layouts: `lesson.html` and `technology.html` which are
used for individual lessons and containerisation technology summary page.
These can be changed in-place and changes will be included in the next build.
