---
title: "Dropshare"
date: 2019-03-11T09:27:55-04:00
tags: ["review"]
categories: []
---

I have a constant back and forth with sharing tools. I previously used Droplr, but they abandoned their iOS app (recently re-released but no better than the previous version), the website is abysmal, and support took almost a week to get a response, on to CloudApp I went.

Last January I received a promotion from Smile Software for $20 off CloudApp's yearly subscription plus 6GB of bandwidth per file, so I signed up. Since then they removed their iOS app, then reintroduced it as a new app, but it was the same with more bugs because they did not update anything in my experience. Then they force you to go to the beta website, but the beta website for months now continuously reloads before the page finishes loading. To get to the old UI, you are required to click repeated on the link and hope you get it before the page refreshes. So off I went to Dropshare.

[Dropshare][1] is not like the others (or it wasn't in the beginning). It gave you the same functionality as Droplr and CloudApp but on your hosting solution or cloud storage. I had already used Backblaze B2 Bucket with Arq for backing up my Synology and Macs, so I felt more comfortable with them than anyone else. Once you create the bucket, you need to make it public, then set it up in Dropshare as a connection. The great thing about Dropshare is it gives you the option to have multiple connections. So you could host all images on one connection, then all videos on another, and finally files on a separate one. Recently, thanks to [Jason Burk][2] I've switched to [Wasabi][3] for my cloud storage needs, mainly due to the lower prices and faster loading. Due to Wasabi being an S3 compliant service, any application or service that can use S3 can attach to Wasabi.

One of the best features of Dropshare is the URL shortener service, either theirs or a custom one. At first, I just used theirs, then moved to [Bitly][4]. Recently I implemented [YOURLS][5], a solution which is [self-hosted][6] and uses a domain name you own, so I'm not reliant on a companies URL in case they go out of business. The shortener works for URLs dragged to the icon in the menu bar, so you have an easy way of shortening URLs on the Mac as well as sharing images, Gifs, videos, and files. I'm still working on a code snippet system, but for now, I am sticking with [Github Gists][7] or adding it to my wiki. Dropshare recently added URL shortening on iOS, so now I can shorten URLs on every platform from one application.

If you've been looking for a sharing tool but want the flexibility of a solution you own, then Dropshare is definitely for you, and I would recommend giving it a shot.

[1]:	https://slnks.io/4jtco
[2]:	https://burk.io
[3]:	https://slnks.io/x1hl7
[4]:	https://slnks.io/l0r9y
[5]:	https://slnks.io/ywjf8
[6]:	https://slnks.io/tg81w
[7]:	https://slnks.io/rrb5l