---
title: "Return to Sublime Text"
date: 2019-03-07T08:34:15-04:00
tags: ["writing"]
categories: []
---

In January I asked the Micro.blog community a [question about writing apps][1] for Windows. I received many great suggestions and tried almost everything that was suggested finally ending up with [Sublime Text][2].

## My Journey
I've fallen in love with Sublime Text multiple times over the years, but then I would find a new note-taking app which draws me away ending with forgetting about Sublime Text for months, or in this last instance a year and a half. When I started my [Blot.im][3] blog I started with creating posts in [BBEdit][4] on macOS, [Notepad++][5] on Windows, and [Drafts][6] on iOS. I've since gone through the following applications to get back to Sublime Text: [1Writer][7], [Ulysses][8], [Typora][9], [Brackets][10], [Visual Studio Code][11]. It may seem like an odd mixture of apps, but they have one thing in common: sidebar libraries. Sidebar libraries allow me to add my Dropbox folder for my blog and have everything from posts to the CSS file in one text editor in one window available. It allows me to write and save drafts in the Drafts folder of the directory then once done, drag and drop in the sidebar and the post is published.

## Friction Points
1Writer was only viable for iOS, Ulysses while great on both macOS and iOS wasn't on Windows, and Markdown handling in Ulysses isn't my favorite and leaves much to be desired. Typora is good with Markdown but falls short on other file formats. While testing Typora had some bugs that would freeze the app which caused me to move on. iA Writer came very close, but some decisions by the developers to put all the blame on cloud services scared me, then when I suggested a feature the response was to use the third party keyboard, so they were out. 

## Code Editors
Then came Brackets, I'd never used Brackets, and when a coworker suggested it for another task I needed to accomplish it seemed like a great fit, and for a week it was. Unfortunately, Brackets doesn't have the packages/extension library that Sublime Text has built up over the years. So I went to try Visual Studio Code, and it was a great app with more extensions than Brackets. Unfortunately, it had some weird quirks that created an amount of friction I found acceptable but would keep my eye out for something else. One of the suggestions I received was Sublime Text, which I had a license for version 2 and 3, so I downloaded it. I immediately remembered why I loved Sublime Text, the extensibility of packages, and the ability to write syntax changes into the preferences was incredibly useful for a code editor. 

## Sublime Text Setup
I'm currently using three packages, starting with [WordCount][12] to show live characters and word counts. It's been handy for making sure my Status posts make it under the 280 character Micro.blog limit before truncating and linking back to the blog. One of my criteria for testing these applications was a character count and Sublime Text didn't have a great default one, but with WordCount that doesn't matter. [Monokai Extended][13] then [Markdown Extended][14] to change the Markdown syntax highlighting. Due to Windows having an issue indexing Markdown files, I switched to text files and changed the default Syntax for all text files to Markdown Extended.

I use one project for the blog, which has the Blot.im folder in the sidebar, allowing access to everything. Projects enable me to quickly open the folders I need for the blog all at once, and with workspaces, I can set two windows and have both windows open with the correct folders in each.

## Conclusion
I'm back to using Sublime Text on Windows and macOS, Drafts is still my go-to on iOS. I love Sublime Text focus around getting the words on the screen, then figuring out where the file should go after it's written. The applications I tested acted similarly, but each one had a flaw in some way that pushed me away due to no recourse. Default Sublime Text did have some flaws but through Packages and editing the Settings, one can make Sublime Text precisely what they need from a text editor.

[1]:	https://micro.blog/joshsullivan/1896808
[2]:	https://www.sublimetext.com/
[3]:	https://blot.im
[4]:	http://www.barebones.com/products/bbedit/index.html
[5]:	https://notepad-plus-plus.org/
[6]:	https://getdrafts.com
[7]:	http://1writerapp.com/
[8]:	https://ulysses.app/
[9]:	https://typora.io/
[10]:	http://brackets.io/
[11]:	https://code.visualstudio.com/
[12]:	https://packagecontrol.io/packages/WordCount
[13]:	https://packagecontrol.io/packages/Monokai%20Extended
[14]:	https://packagecontrol.io/packages/Markdown%20Extended