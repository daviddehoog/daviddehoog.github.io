---
title: 'the site'
date: 2024-09-29T00:06:17+10:00
draft: false
topics: 'workflow'
status: 'reviewing'
---

By design, this is quite a simple web site.

I use a static site generator, [Hugo](https://gohugo.io), to roll [markdown](https://www.markdownguide.org) files I have written into a website (HTML and CSS). The (default) ananke theme gives the files a consistent look and feel.

<!--more-->

## tools

The content files and the [resulting website](http://daviddehoog.github.io) files are under version control with [git](https://git-scm.com), and synchronised with [GitHub](https://github.com). The site is actually built with [GitHub Actions](https://github.com/features/actions) and served by [GitHub Pages](https://pages.github.com).

Most content is written in markdown, often on my phone or tablet on [Bear](https://bear.app) in quieter moments. I use [Visual Studio Code](https://code.visualstudio.com) to edit longer posts and to adjust Hugo configuration and template files.

All the code is available in [the site’s GitHub repository](https://github.com/daviddehoog/daviddehoog.github.io). Ideas for future features and content are stored as [issues](https://github.com/daviddehoog/daviddehoog.github.io/issues) in the repository.

The [Hugo documentation](https://gohugo.io/documentation/) has been very helpful for a new starter.

## git workflow

I tend to write new content directly on the main branch. Each new post is a fresh commit. I also make a daily commit where I am doing editing or proofing across multiple posts.

I create an issue on Github to plan and track each new site feature. For example, I used an issue to capture my plans for a taxonomy to categorise posts and set up a linked branch to develop the cross-cutting configuration changes to the site. I was then able to test these changes on the branch before merging these edits into main.

At the end of each day that I work on a branch for the site, I try to make a commit called 'WIP' to back up my progress from my local repository onto Github.

When a feature is complete and I need to merge the branch into main, I try to squash any WIP commits and then re-base the branch against main to pick up the new content.

This approach helps me to keep changes to the content of the site separate from the changes to the site's configuration files.

A Github action re-builds the site each time the main branch is updated and deploys it to Github pages.

## features

_2024-09-24_: First, I set up a static [about page](({{< ref "/about/" >}})), with a bit about me. I also added a link to the header on each other page.

_2024-10-20_: Second, I set up a taxonomy of post topics, which allows me to add topic tags to each post and provides a [list of all posts on a topic]({{< ref "/topics" >}}).