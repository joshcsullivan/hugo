---
title: "My Mac Toolbox"
slug: /macos-tools
date: 2019-06-13T10:17:00-04:00
draft: false
tags: ["macOS", "workflow"]
categories: ["Tech"]
toc: true
aliases: ["/macos-tools/"]
---

I wanted to expand on the list of hardware and software I use to get my work done.

## Hardware
The hardware I use daily (or almost daily) to get my professional and personal work done.

- Mac Pro Late 2013 Model
	- One for the office and one at home
- HP Z2 Mini Workstation (at work)
- iPad Pro 12.9 256GB
- iPhone XS Max 256GB
- ScanSnap ix1500
- Synology DS418play
- Synology DS1918+

## Software

### Email
I use [Fastmail](https://fastmail.com) as an email provider with a custom domain. I prefer to own the domain, and Fastmail was the best option for privacy while also being easy to use.

I use Apple Mail on macOS and iOS, I know a lot of people have gripes about it, but I find it works very well, it's swiping gestures are more than enough to get me by, and with keyboard shortcuts via [Keyboard Maestro](https://www.keyboardmaestro.com/main/) I have all the sharing features I need.

## Task Management
I first heard of GTD on the [MacPowerUsers](https://www.relay.fm/mpu) podcast, and at that time, it was synonymous with [OmniFocus](https://www.omnigroup.com/omnifocus), so I purchased OmniFocus, and for a long time, about eight years, I used OmniFocus. Then [Federico Viticci](https://macstories.net) began his quest to try every task manager in the book, and I went along for the ride. I tried [Todoist](https://todoist.com), [2Do](https://www.2doapp.com/mac/), [Things](https://culturedcode.com/things/), [GoodTask](http://goodtaskapp.com/), [Remember The Milk](https://www.rememberthemilk.com/), never sticking to one more than a couple of weeks and eventually found my way back to OmniFocus for another year. Then last December, I was getting frustrated with the way the online version of OmniFocus as going so I decided to test Todoist again, mainly because it had the best online component and natural language processing. I've stuck with Todoist since December of 2018 and haven't looked back.

## File Storage
File storage is something I wrestle, and flip flop with a lot and recently have decided to stick to what I am doing now because it is working very well for myself. For everyday sync and general storage, I am using [Dropbox](https://dropbox.com), and I signed up for the professional version last year because of image text searching and Smart Sync. I’ve seen the new plans and am going to stay with Professional due to a few features, image text searching (AutoOCR), Shared link controls, and Viewer history. I didn’t realize how much my sharing habits would change since last year, but I’ve become more public online and more active in forums, in a coming out of my shell sort of way and so the more I share, the more I needed control over these options. I like iCloud Drive, but I did have a horrible experience with an Excel file on which I worked for about 3 hours getting right then instead of saving it to the desktop I saved it to my iCloud Drive, and it was corrupted. I had to run [PhotoRec](https://www.cgsecurity.org/wiki/PhotoRec) to recover the autosave file, but that took two days to finish and ever since then I won’t trust iCloud Drive with my data.

The other file storage location, usually cold storage is a [DEVONthink](https://devontechnologies.com/apps/devonthink) database in the general topic/area of the document — more on DEVONthink to come.

## Writing and Blogging
All of my writing starts and is finished in [Drafts](https://getdrafts.com). It can begin on iOS or macOS (thank you, Greg!) and I can pick it up on any other Apple device I have with me. For long piece articles, I usually save them to DEVONthink as well, so that I have a history of the piece.

For blogging, my blog is hosted with [Blot.im](https://blog.im) and synced via Dropbox. I tried Git for a few weeks but changed back to Dropbox because it was much simpler to use. I now have three Blot.im blogs, my [main blog](https://blog.joshsullivan.io), my [photos blog](https://photos.joshsullivan.io) and my dummy blog, which I use for testing CSS and script changes before pushing to either of the other two sites.

## Security
Internet security is crucial these days, and that starts with strong random passwords, there’s no application I trust more than [1Password](https://1password.com/) to keep track of all my passwords, credit cards, software license, identity cards, secure notes, and very few select documents. I remember three passwords, all different, my 1Password master password, my Apple ID password, and my work password, the last two are only because I enter them every day somewhere. I purchased a family plan for my significant other, my cousin, my grandmother, and I when it first came out. I’m happy to report that all of them use it regularly, and my grandmother is pleased to have a place to put her passwords where she can access them on her iPhone, iPad, and her Windows desktop without having to put them in a notebook, as she used to do.

For ad blocking, I’ve become very partial to [AdGuard](https://adguard.com/en/welcome.html), which continues to get better. It does a better job than anyone else because it uses an HTTPS certificate on the device to grab traffic then section out the ads, scripts, and junk from sites as it loads them. I’ve found it to block more than 1Blocker which I used in the past, while also allowing you to be more selective about whitelisting individual components, subdomains, or the full domain.

## Browsing
My browser goes hand in hand with Security, I use the [Brave Browser](https://brave.com/), which includes excellent ad blocking tools, but my favorite feature is the script blocking. You can disable scripts on a page from running, which is hugely beneficial to blocking the annoying autoplay video popups and the join today javascript popups.

## Note Taking
Almost all of my notes start in Drafts, or the DEVONthink note-taking window. Drafts is easier on iOS due to the immediate cursor when you open it, while on macOS a quick ⇧⌥⌘N will launch the DEVONthink Take Note window, while ⇧⌘1 will launch the Drafts Quick Capture window. All personal notes are sent to either my Notes database or Personal database depending on the nature of the note. Otherwise, they end up in my Knowledge Base database or Work database. All notes are written in Markdown.

## Others
I’m not sure where to put [TheBrain](https://thebrain.com/) because for me it solves many issues. 
* CRM for both Professional and Personal Use
* Processes and Procedures for all of the types of data I handle, this also allows me to keep track of the different application I have and if they can be used for another kind of data at a later date
* I keep a work log, so I know what I did on a given day, and a personal record that doesn’t make it to my [public wiki journal](https://joshisms.io/#Journals) 
* I also keep track of Books, Movies, and TV Shows
* Link Tracking - I'm currently using it to keep track of Forum Posts, Blog Posts, and other general websites that I find while browsing throughout the day, I then send it to DEVONthink if I want to archive the link or will connect the thought to another branch of my Brain.

TheBrain isn’t quite there in terms of note taking so small notes are okay, but there has been some talk of improvements to the note editor in version 11.

## Automation
The software I use for automation isn’t always used actively by me every day, but every day is running and doing tasks. [Keyboard Maestro](https://www.keyboardmaestro.com/main/) and [Hazel](https://www.noodlesoft.com/) are my most used automation applications. Hazel is always copying, moving, uploading, and deleting files on my Mac, I have no idea how much time I’ve saved by setting up the rules in Hazel, but by now, after six years of using it, it has to be days worth of time saved. Likewise, Keyboard Maestro has become an incredible time saver. I use it multiple times a day by invoking a keyboard shortcut that does some action or runs an Apple Script. During the night it runs a few different scripts to backup various applications, DEVONthink and FileMaker are two, mainly it zips the open databases then moves them to my Synology for backup to my cloud backup.

Another more simple automation tool I use is [TextExpander](https://textexpander.com/), I am constantly using it for all kinds of different snippets where it is the date or getting the front most Brave window as a Markdown link or TiddlyWiki link for my wiki. It's incredible powerful with AppleScript and JavaScript support and I'm happy to pay for the subscription.