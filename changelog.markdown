---
layout: page
title: Changelog
permalink: /changelog/
---

One of the reason I have this blog is to keep sharp on basic dev skills which I no longer use that often. Hence I created this changelog to keep track on how I customised the site and which resources I used. Only high-level changes are captured here, further details & minor changes are available in commit history.

### 30092021
- google-analytics setup via built-in key in minima: [enabling Google Analytics][minima-ga] 

### 28092021
- layout and front matter changes on the home page, e.g. customising the minima theme: [overriding theme defaults][overriding-theme-defaults]

### 15092021 GitHub Pages Jekyll - skeleton
- [set up site with Jekyll][setup-gh-pages-jekyll]
- setup Jekyll locally under [WSL][wsl] in Windows 11 [build 10.0.22000.184][w11-build-184]
- develop & test skeleton site locally (minima theme)
- publish an empty blog with basic customisations only (e.g. config.yml keys) on mareksamaj.github.io

[setup-gh-pages-jekyll]: https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll
[wsl]: https://docs.microsoft.com/en-us/windows/wsl/install
[w11-build-184]: https://blogs.windows.com/windows-insider/2021/09/09/announcing-windows-11-insider-preview-build-22000-184/
[overriding-theme-defaults]: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
[minima-ga]: https://github.com/jekyll/minima#enabling-google-analytics