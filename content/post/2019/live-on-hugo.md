---
title: "Hugo Site is Live"
date: 2019-06-17T16:16:27-04:00
draft: false
tags: ["hugo", "blog", "meta"]
categories: ["meta"]
---

# Live on Hugo with Jane Theme

I've finally deployed a [Hugo](https://gohugo.io) site with [Netlify](https://netlify.com) and [Github](https://github.com).

I did so thanks to these posts:

* [Ec-static - How to go Hugo - Bryce Wray](https://brycewray.com/posts/2019/04/ec-static/)
* [Publish or perish - Going live with your Hugo site - Bryce Wray](https://brycewray.com/posts/2019/04/publish-or-perish/)

Special mention for [Jack Baty](https://baty.blog) whom I was able to get a couple lines of the TOML from to get rid of the annoying author box at the bottom of posts.

It was a little more difficult to get going at first, because the theme I chose changed the Posts folder to Post (missing the S) and therefore the site wasn't showing any posts. I've since fixed it. With Netlify, it was very easy to add a custom domain and get a Let's Encrypt cert for the domain.

I did have one issue while deploying where I had to add the theme to `.gitmodules` because the theme was cloned from GitHub.

Now to figure out what to use it for... 🤔