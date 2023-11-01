---
layout: post
title:  "Connect GitHub Pages with Google Analytics (GA4) - minima theme"
date:   2023-11-01 20:00:00 +0100
categories: tips
---

It took me longer than 30 minutes to figure this out, which means it deserves a post. This guide is specific to [minima theme][minima-theme] which is one of the [supported Jekyll themes][supported-jekyll-themes] in GitHub Pages. 

## Create Google tag and add it to your site

1. You need to setup Google Analytics 4 and create a [Google tag][google-tag-overview]. The steps are well documented here - [[GA4] Set up Analytics for a website and/or app][setup-analytics-for-a-website].

2. To enable Google Analytics, add the following line to your Jekyll site *_config.yml*: 
```yaml
# add your Google tag here
google_analytics: G-XXXXXXXXXX
```

## Fix google-analytics.html to work with GA4

3. At the time of writing this post, GitHub Pages use [minima theme version 2.5.1][github-pages-depedencies]. This version doesn't work properly with GA4, see [Issue #561][issue-561]. You can either switch to _remote_theme_ as described in the Issue #561 or copy the latest _google-analytics.html_ file from the current minima theme to your site and keep the default GitHub Pages minima theme. If you prefer the second option, read on.

4. Get the latest version of _google-analytics.html_ from [the minima theme GitHub repo][minima-repo] and put it in your *_includes* folder of your site.

5. Deploy your site and browse to it. You should immediately see the traffic data in your Google Analytics real time dashboard.

![Google Analytics dashboard showing Your data collection is active message and one visitor in the real time dashboard](/assets/images/data-collection-active.png)

**Important**: Check that your privacy settings in your browser do not block Google trackers. You won't see any traffic in the Analytics Dashboard despite everything configured correctly if tracking is blocked by your browser. 

[minima-theme]: https://github.com/jekyll/minima
[supported-jekyll-themes]: https://pages.github.com/themes
[google-tag-overview]: https://support.google.com/analytics/answer/11994839
[setup-analytics-for-a-website]: https://support.google.com/analytics/answer/9304153
[github-pages-depedencies]: https://pages.github.com/versions/
[issue-561]: https://github.com/jekyll/minima/issues/561
[minima-repo]: https://github.com/jekyll/minima/blob/master/_includes/google-analytics.html
