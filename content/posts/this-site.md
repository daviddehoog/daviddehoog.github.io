+++
title = 'This site'
date = 2024-09-29T00:06:17+10:00
draft = false
+++

## The site - plumbing
For the reasons set out aboce, this is not a high-tech website.  
- Uses the Hugo static site generator (written in Go). Hugo takes markdown files and rolls them into HTML, CSS (and JS). It uses the (default) ananke theme to give the sites files a consistent look and feel. Link to Hugo documentation.
- The source files and the resulting website files are under version control with git, and synchronised with GitHub. Each time the main branch changes, a GitHub Action re-builds the site using the new content.
- The resulting static website is about 600 kilobytes and is deployed to and served by a GitHub webserver.
- Future possible features include:
  - linting of the HTML and CSS output files, as part of the GitHub action
  - ensuring the website is accessible (WCAG2.2 compliance)
  - building my own a custom Hugo theme
  - adding an RSS feed

Possible future content is included as [Issues](https://github.com/daviddehoog/daviddehoog.github.io/issues) in [the site’s GitHub repository](https://github.com/daviddehoog/daviddehoog.github.io).

  ### Git workflow