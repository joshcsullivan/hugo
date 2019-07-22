---
title: "Thoughts on Resilio Sync"
date: 2019-06-21T12:08:03-04:00
tags: ["synology", "resilio sync"]
categories: []
---

Andrew Canion recently [posted](https://blog.andrewcanion.com/2019/06/14/some-time-ago.html) about using [Resilio Sync](https://www.resilio.com/) as a Dropbox replacement. So naturally I installed it on my Synology and tested it out. 

TLDR; Sync wasn't fast and I'm testing Synology Drive.

## Initial Reaction
When I first installed Resilio, I immediately did the wrong thing, which was to set it up, then create folders in the local client on my Mac instead of in the Web GUI. After a few tries I eventually figured out the best way was to create the folders in the GUI, because it keeps the read/write permissions correct when syncing.

Once I got the hang of Resilio's quirks I started poking around and saw that for some reason the web GUI wasn't using my Let's Encrypt cert that I use for my Synology DSM and other apps. So I went in to set it and found that you cannot specify it in Security > Certificate > Domain Cert. So off to Google I went and found people with the same question on their forum, but each time support said to put in a ticket. In went the ticket, and the response was to specify the cert in the `sync.conf` file, but if the cert isn't reachable via SSH to your user account then you need to change the folder permissions to allow access to that folder. What? I'm not going to be changing the permissions on a folder that works for every other app installed via the package center. So I found some instructions on copying the cert then adding it to another accessible location then specifying the location in the `sync.conf`, which I did and the GUI immediately took the cert. When I asked to have Resilio use the Synology cert permissions, they said it wasn't on the road map, oh well.

## Usage
In usage Resilio has worked well, sync takes some time for changes to be pushed and pulled, which isn't a network issue on either end, I have gigabit at home and gigabit at work. So it has to be the client and you cannot force a sync in the client, so you have to wait for the changes to be found by the client then pulled down or pushed up.

In practice this is usually fine especially if you make a change then leave your computer on but locked when you leave. Unfortunately, this fell apart when I made a change on my MacBook Pro, then closed the lid because I was leaving, the sync didn't occur quickly enough. 

## Conclusion
Due to the issues with the cert, which I will need to update every time the cert is renewed, plus the delay in syncing without a manual start button has pushed me to try Synology Drive. Again, if you don't need instantaneous sync and don't mind updating the cert manually, then I think Resilio is a really good option.

I've been testing the Synology Drive beta for a couple weeks, and so far it's been great. One feature I hope is added before it's released is On-Demand sync being added to the Drive macOS client. Windows currently has the feature and it works great, I've not experienced any issues.

I'll be posting an update on Synology Drive once I've had an appropriate amount of time to stress test it.