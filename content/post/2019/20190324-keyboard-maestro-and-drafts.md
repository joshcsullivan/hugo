---
title: "Keyboard Maestro and Drafts"
date: 2019-03-24T10:26:59-04:00
tags: ["writing", "blogging"]
categories: []
---

# Posting on macOS with Keyboard Maestro and Drafts

So far on the Drafts for Mac version, I've been using Keyboard Maestro in the absence of actions. It has worked pretty well, although I've found if the macro edits the draft, then it needs to save the version for it to export correctly. One of my favorite macros is posting to my blog. It's a straightforward action, based on keystrokes and pauses, but it creates an almost frictionless posting solution. 

## TextExpander and Drafts

Currently, I enter the tags and metadata via two TextExpander snippets, due to my preference to have time to think about the tags. The first TextExpander snippet is run every time before I start the post; it adds the Permalink, Title, and Tags metadata to the beginning of the draft. Then I start writing the post, once done I add the tags and the ending of the permalink. Finally, I run the second TextExpander snippet which adds the date and the timestamp at the top of the draft.

## Keyboard Maestro Macro

The Keyboard Maestro macro allows me to post the draft to the Dropbox folder quickly. It cuts the first line of the draft, which is the timestamp in the format YYYYMMDD-HHMMSS (ex. `20190324-095114`), then saves the current version with the first line cut, Exports the draft, deletes the full filename, pastes the timestamp and adds `.txt` then saves the file. It's almost as simple as my action on iOS, which after I add the tags I tap the Feather Pen icon in the actions keyboard and it immediately parses out the first line as the file name and saves the body, everything but the first line, as the file contents.

## Simplifying my Writing Workflow

Recently I've been trying to simplify my posting strategy, and once actions are added to the macOS version of Drafts, specifically the ability save to Dropbox, I will be retiring this macro, but for now, it gets the job done efficiently and quickly. Previously I had multiple versions of the TextExpander snippets for it was as Micro.blog post or long-form post, now I've combined them into two TextExpander snippets that cover all post types.

I prefer to do most of my writing in Drafts because it quickly syncs to iOS and I can pick up where I left off on any Apple device without hassle. I do prefer Sublime Text for writing long-form posts due to the ability to pick it up on my Windows machine at work when I have time to write a little bit. For now, most of my long posts start in Drafts then get saved to the drafts folder in my Dropbox Blot folder at which point I can open them in Sublime Text and write. If I know I am going to be starting and finishing a post on macOS or iOS then I will continue to write in Drafts, such as this post which was written entirely on macOS.

You can find the Keyboard Maestro [macro here][1]. **Please be aware the macro will download immediately on clicking the link**

Also be aware this is an incredibly simple workflow that you may have no use for, if you don't include a file name at the top of your draft it will not work correctly, but you can edit it to work within your workflow.

[1]:	https://s3.wasabisys.com/jcs-blog/assets/files/Post-to-Blog.kmmacros