---
title: "MailMate Bundles"
date: 2019-07-11T10:06:30-04:00
tags: ["omnifocus", "todoist", "gtd"]
categories: []
---

One of my favorite features of [MailMate](https://freron.com/) is sharing bundles. They are basically actions that allow you to quickly send the current email or emails to another application. One of my more frequently used action is the ability to quickly send an email to my Task Manager, for Todoist, it adds a link in the task title, in OmniFocus it adds the link in the task notes. The link can be opened on macOS and iOS, without MailMate, because it uses the default Apple Mail message URL. The link isn't broken even when the message is moved from one folder to another, making the links very useful because I usually send the email to Todoist then archive it.

Depending on the application, the palette allows you to choose multiple options, for example, for both OmniFocus and Todoist there is `Add` and `Add with Summary...` whereas for DEVONthink, there is only `Add`: 

![](/img/2019/20190711-MailMate-Palette.png)

If you use the OmniFocus Add, the Quick Entry popup comes up filled out:

![](/img/2019/20190711-MailMate-OmniFocus.png)

Likewise, Todoist adds the same, but with a Markdown link in the title instead of the notes:

![](/img/2019/20190711-MailMate-Todoist.png)

Where they differ is the `Add with Summary...` in OmniFocus it will add the text of the email to the task notes:

![](/img/2019/20190711-MailMate-OmniFocus-Summary.png)

Todoist will use the API to add the email to Todoist, so it's in the background, but currently it doesn't add the text of the email to the notes of the task.

The other Bundle I use, but not often is DEVONthink. It adds an Email file, `.eml` to DEVONthink with a link back to the message. It strips dynamic content images as it goes, so if the image isn't embedded in the email, it won't be added to the DEVONthink item. Usually if I really need the images, I print the email to PDF then add it to DEVONthink. The reason I don't use these options often is due to DEVONthink's excellent email import options, which were greatly improved in DEVONthink 3, which is currently in public beta.

If you haven't used MailMate, I would recommend taking a look at it, I started using it for the ability to write in Markdown, but now it's a great resource for sharing emails, sorting, and searching. It's smart groups are fantastic with far more options than other applications, they are definitely one of the driving reasons I have stuck with MailMate.