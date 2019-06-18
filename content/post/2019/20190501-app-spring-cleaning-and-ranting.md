---
title: "App Spring Cleaning and Ranting"
date: 2019-05-01T11:04:14-04:00
draft: false
tags: ["devonthink", "workflow", "writing", "note taking", "thebrain"]
categories: ["Tech"]
---

> Finally, I tired of the entire process and burned it down. I am starting fresh.

From Jack Baty's [State of the System – Spring 2019](https://copingmechanism.com/2019/state-of-the-system-spring-2019/)

I've been experiencing this but for different reasons. The past few months [TheBrain](https://thebrain.com) development has failed to fix multiple issues related to laggy UI, buggy note taking, and a Windows update issue that has plagued them for the last three months. The Windows update requires you to download the update but not install it. Close TheBrain, navigate to where the installer was downloaded, run the installer, re-open TheBrain at which point it says Updating, then end TheBrain task, open TheBrain a second time and *finally* you are updated. On Windows, the UI is far less laggy, but the notes typing can be delayed up to a few seconds, which is horrible if you use it to take quick notes.

On the Mac, the UI is incredibly clunky, when you drag the notes panel divider over to increase or decrease the panel size, it jerks to the new position spread over 3 seconds. The notes typing delay is less pronounced in some builds, but others are much worse. I'm tired of fighting it to get it to work the way it used to, tired of the friction to take notes, tired of having to set up the way I like TheBrain every time I open it on my Mac Pro.

Also, it is 2019, why the f#&k [^1] are we limited to 30GB of internal storage, give us at least 500GB, and really for the amount we are paying yearly it should be at least a terabyte. 

Recently, DEVONtechnologies released the public beta of version 3 of DEVONthink and I must say even when in private beta it was far less buggy/annoying than the current TheBrain release version. Due to this, I've begun the process of moving data from TheBrain to DEVONthink Server 3. I purchased [TheBrain ProCombo](https://thebrain.com/store), so my license will allow me to use TheBrain without a subscription, which at this point I don't believe I am going to be renewing it this year. Don't get me wrong, if TheBrain Team gets it together and solves a lot of these issues I'll be renewing but I don't think it's worth it to re-subscribe for another year with the way things are going and are handled. I'm tired of dealing with buggy software that has no end in sight. 


## Onward
To get to the point (finally!), I am slowly moving data out of TheBrain and into DEVONthink and Dynalist. 

Currently, with [DEVONthink Server 3](https://devontechnologies.com/apps/devonthink/editions) (DTS3) I can use the web interface on Windows machines, which is much improved over DTPO 2 Server UI. The note area is fast, copying works excellent in the text area[^2], no lag in the UI, and Markdown support [^3]. Most of my notes on Windows this week were written in NotePad++ then copied and pasted into a new Markdown file via the DTS3 Web interface. I can tag the file and move it to the correct group. I'm much happier than with the previous solution, which was to save the file to Dropbox then when I was back on my Mac I would add it to DEVONthink.

Links/URLs are another part of my workflow that changed with DTS3 public beta release. Previously when I came across an interesting link, I would drag it to TheBrain plex and add it to my Inbox thought for processing later. Now on macOS, I clip the link to DTS3 and process the Inbox at night. Currently, there is a bug I've reported to be fixed in the web interface when adding a bookmark, so at the moment I add it to a Markdown file in my Inbox and clear the file out at night on my Mac.

I'm also finding myself store more links as PDFs and with [Print Friendly](https://www.printfriendly.com/) I can grab the resulting PDF and drop it in the DTS3 web interface. It came in handy recently when someone removed their secondary blog, and I had to reference a writeup they did, I pulled up the PDF and got the information that I needed out of it. I am slowly moving away from using services that I don't control, which is one reason I like PDFs. Even if Pinboard, Pocket, and others promise to store a copy, I don't trust it due to the abandonment of Pinboard for a year with archived pages being inaccessible for almost eight months. 

There are parts of TheBrain I will miss. BrainBox was a great addition in version 10 that allowed you to add a URL to your Brain account which was accessible in the app to be added as a thought or attachment later. I do wish DEVONthink had a clip function on Windows, but I'm happy with the current solution. 

### Capturing on iOS, macOS, and Windows 

On iOS I use Drafts for all note capture then use an action to send the text to DEVONthink To Go. With MacDrifter's "[Moving Text Between Drafts and DEVONthink To Go with Shortcuts](http://www.macdrifter.com/2018/11/moving-text-between-drafts-and-devonthink-to-go-with-shortcuts.html)" I have an easy way to take a file in DTTG and edit it in Drafts then send it back to DTTG updating the item.

On macOS, I am using Drafts to quickly capture text or DTS3's Take Note feature, which brings up a window to write a note, name it, tag it, etc., then save it to a specific group or an Inbox. Windows I use Notepad++ to enter text quickly for processing later. All notes now end up in DEVONthink one way or another, so I won't have to go looking through multiple systems to search for what I am looking. One exception to that rule are lists. I store lists in [Dynalist](https://dynalist.io/) because it is so great and now has a Mindmap feature that works very well.

Overall, I'm pretty happy with the way things are shaping up. I like to have most of my reference material and notes in as few applications and areas as possible. I've consolidated to one principal repository, DEVONthink, with DEVONtechnologies continuing to improve DTS3 daily and weekly I'm happy about this decision.

I do hope TheBrain Technologies gets around to fixing the issues that have been a thorn in my side, but I'm glad it finally pushed me to consolidate my random bits of information into one system.

[^1]: I'm sorry for swearing, I rarely swear online, but sometimes it's necessary to get the point across.

[^2]: You currently cannot copy the Markdown preview text in the web interface, but I did request that feature.

[^3]: Myself and many other people on TheBrain forums have asked for TheBrain to either use Markdown notes instead of the current HTML notes or go back to plain text.