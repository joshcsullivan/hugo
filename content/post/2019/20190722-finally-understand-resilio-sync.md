---
title: "Finally Understand Resilio Sync"
date: 2019-07-22T10:07:34-04:00
tags: ["resilio sync"]
categories: ["Tech"]
---

After stating that [I was moving on](https://joshsullivan.io/2019/06/thoughts-on-resilio-sync/) from Resilio Sync, I finally grasped its usefulness this past weekend. Over the weekend I was looking to move some preference sync files out of iCloud, mainly because I was never supposed to put them there, but I hadn't had an issue yet so I left them there far longer than I should. Nothing happened to them, but I was reading a post on the [MPU Talk Forum](https://talk.macpowerusers.com/t/dropbox-do-you-trust-them-with-your-data/12830/34) and found this paragraph by TJ Luoma:

> Keyboard Maestro and Alfred both just ask you to point at the file/folder where you can find the sync data for it. Both of them are perfectly happy to put their sync data in ~/.config/ which I sync using Resilio Sync 1 (neé BitTorrent Sync). I’ve been using that for years without any issue.

Immediately Resilio Sync clicked with me. I realized syncing those preference files through Resilio would be great. Then another thought popped into my head, if `.config` can be synced, so can `.ssh`. I immediately synced that over, I know some people are skeptical about syncing their private keys over, but the connection is encrypted, not to mention the Resilio server is actually my Synology NAS at home so I'm not worried about storing the data on a third party server. Finally the shared folder is encrypted, so if someone physically broke into my home and got the drives out of the Synology, they still wouldn't be able to get into that folder. To top it off, the data that I store on my VPS's at DigitalOcean contain zero personal or private information. If they want to get into my wiki, go for it! My link shortner, why not? Blog comments, do it! Joking aside, Resilio has peer to peer encryption, plus on each device I have Resilio on, at the very least the folder is encrypted, if not the entire hard drive.

Moving on, as I said Resilio finally clicked for me, I could sync folders that previously I would copy every so often to other machines, or symlink them. Another handy feature was syncing TheBrain `CustomInputBindings.txt` which was a pain to keep the keyboard shortcuts in sync from one Mac to another.

Now that I'm finally understanding how to properly use Resilio Sync, I'm finding more ways to adopt it into my workflow every day.