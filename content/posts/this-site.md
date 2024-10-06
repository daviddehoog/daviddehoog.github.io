+++
title = 'This site'
date = 2024-09-29T00:06:17+10:00
draft = false
+++

## The site - plumbing

This is a relatively simple web site.

The site uses a static site generator, [Hugo](https://gohugo.io), to roll markdown files I have written into HTML, CSS (and JavaScript). The (default) ananke theme gives the files a consistent look and feel. The [Hugo documentation](https://gohugo.io/documentation/) has been very helpful for a new starter.

The content files and the [resulting website](http://daviddehoog.github.io) files are under version control with [git](https://git-scm.com), and synchronised with [GitHub](https://github.com). The site is actually built with [GitHub Actions](https://github.com/features/actions) and served by [GitHub Pages](https://pages.github.com).

Most content is written in [markdown](https://www.markdownguide.org), often on my phone or tablet on [Bear](https://bear.app) in quieter moments. I use [Visual Studio Code](https://code.visualstudio.com) to edit longer posts and to adjust Hugo configuration and template files.

The site's code is available in [the site’s GitHub repository](https://github.com/daviddehoog/daviddehoog.github.io). Possible future content is included as [Issues](https://github.com/daviddehoog/daviddehoog.github.io/issues).

### Git workflow

Write content and add to main, fresh commit.

New site feautres are a branch - eg one branch per issue - then are tested and merged into main.Daily save as WIP.  Squash commits on a branch before merging into main and deploying.

