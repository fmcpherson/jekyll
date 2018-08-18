---
layout: post
date: 2018-8-18 15:34
title: Managing Tasks With NotePlan
comments: false
category:
- iPad
tags:
- 
---
My first experience with to-do lists was in college when I used a [Daytimer](https://www.daytimer.com/daytimer/browse/Planners/_/N-12o7ukh/?Description=tier20planner&couponId=TIER20A&redirect=false&gclid=CjwKCAjwh9_bBRA_EiwApObaOImwFb5_pYQ_V7LO3dy1saz8OpNLqv5gRo9jp3Klw6YvufI76EAHaBoCEoEQAvD_BwE) to track my class assignments and appointments. Later when I started my career my company sent me to a time management class that taught me how to use a [Franklin Planner](https://shop.franklinplanner.com/store/buy/Planners/cat2120006/), which I used for several years.

I diligently used the Franklin Planner, but one thing that annoyed me was the process of rewriting incomplete tasks across each day, which I found cumbersome. Being in IT I felt a computer would be much better at tracking and managing my to-do list, but this was during the early 1990s and smartphones and tablets did not exist. 

Eventually I bought a [Sharp Wizard](https://en.m.wikipedia.org/wiki/Sharp_Wizard) and have been using an electronic device to manage my calendar, contacts, and tasks ever since. For some of that time there were limited app options for managing this information, but since I started using Android there have been numerous options available.

While I have found Google Calendar and Contacts to be good enough, I continue to bounce between different apps for tasks.  The problem is in part due to the variety of time/task management methodologies available. [Getting Things Done](https://gettingthingsdone.com/) (GTD) is the most popular today and therefore many tasks apps implement GTD in some manner.

I use some GTD concepts, but I find that apps that implement GTD tend to be complicated by too many features. In my opinion [OmniFocus 3](https://www.omnigroup.com/omnifocus/ios/), which seems very popular amongst the Mac and iOS folks, is a case in point. To me OmniFocus is overwhelming to learn, so much so that overcoming that learning curve is not worth buying the app. 

My latest tasks app discovery is [NotePlan](https://noteplan.co/), which is billed as a markdown calendar, todos, and notes app, while others claim it to be a digital [bullet journal](http://bulletjournal.com/). The reference as a digital bullet journal is ironic given that bullet journals are considered the analog system for the digital age. However, the description as a bullet journal is apt in that the app simply maintains a daily list of tasks either accomplished (journal) or to be done (ToDo) and it uses symbols common to bullet journals for completed, scheduled, and deferred items. 

So far I've stuck with NotePlan for a little more than a month, which is a bit of an accomplishment. I think the main reason why NotePlan has "stuck" is that it is simple enough to learn fully and seems to fit well in my workflow. What I've found I like the most is how NotePlan enables you to carry forward incomplete tasks between each day, which is automation of the process I learned during those first Franklin Planner classes I attended in the '90s.

The process forces me to review my incomplete tasks and think about what I want to do each day. If I find that I repeatedly forward a task from day to day to day, I ask myself whether it is something that I really need to get done and whether rather than being on a daily list should the item be moved to a Someday list. (Nod to GTD!) 

NotePlan has two halves, one that is built around a calendar and the other that is a list of notes. You could use NotePlan for taking notes, but I use OneNote for that and so I use this feature to list project tasks like a simple project planner and to store Someday, Things To Try, and Shopping lists.

A new sheet is created for each day, and on the top of the sheet is a list of appointments from your calendar, followed by space for the tasks you identify for that day. The difference here is that most todo apps create one or more lists of tasks and puts the focus on those tasks, where NotePlan creates focus on each day and what it is you wish to get done each day. It might be that this difference is too subtle, but it clicks for me.

![A Day Sheet in Noteplan](https://frankm.org/images/notePlanDaySheet.JPG){: .center-image}

Tasks appear on a day's sheet because you either entered it on that day or because you scheduled it for that day. The key for me is that a task that you have on today's sheet will not end up on tomorrow's sheet unless you explicitly forward it to tomorrow, which builds in a daily review process. 

The journal part of NotePlan comes in the ability to look at past days to see what you did on each day. Each calendar sheet and note in NotePlan is actually a plain text file that is stored in iCloud. When you install NotePlan on an iOS device it creates a folder in iCloud Drive with two sub folders, Calendar and Notes. Daily sheets/files are named using the year+month+day format. 

Because NotePlan stores files in iCloud you can access the same data across your iOS devices running NotePlan, and a version also exists for MacOS. Unfortunately, the application's authors do not plan to make a version of NotePlan for Android or Windows. However, because the files are plain text you can easily view and presumably edit them using a text editor. 

Another feature in NotePlan that I really like is how you can create links to Notes and Calendar sheets. Links to Notes display using a double bracket format familiar to those who have created links to internal wiki pages. By default links to Calendar sheets are prefixed with the at sign followed by a year-month-date line @2018-06-14. 

I recommend enabling the setting Append Links When Scheduling Todos, which when enabled results in a link automatically inserted to the Calendar sheet containing the todo item. A way to manage a project is to create a Note for the project that contains a list of tasks to be completed. To track the work done on the project, open the Note and schedule the task to be completed. NotePlan will add the item to the Calendar sheet and append a link back to the Note from which it was scheduled. 

![A Day Sheet in Noteplan](https://frankm.org/images/notePlanPreferences.JPG){: .center-image}

If you use links you will notice the one thing that I find most frustrating about NotePlan, which is that due to how it uses markdown it is modal. If the keyboard is open, tapping on a link inserts the cursor at the location of the tap rather than open the item associated with the link, to navigate to a note or calendar sheet you need to close the keyboard and then tap the link.

NotePlan's use of [markdown](https://en.m.wikipedia.org/wiki/Markdown), which is a markup language, is odd because it doesn't really have a display mode. For example, you can surround a word with two asterisk to make it bold but while the text is displayed in bold the asterisk remain around the word. You can, however, share a note or calendar sheet with an app like Ulysses that will render the markup for proper display or print. Given that NotePlan already has different behavior when the keyboard is open or closed, I think the app should render display of markdown when the keyboard is closed and show the markdown when the keyboard is open. 

Linking and explicit scheduling of todos are the two features that make NotePlan work for me. You can search for words and tags within each half of the app but search does not work across the two. NotePlan does not have the number of tagging and filtering capabilities as other apps like OmniFocus, so GTD affecianados may find it limiting. You cannot create reminder notifications in NotePlan, but it does have a badge notification of the number of open tasks for given day. NotePlan does have a x-callback-url scheme for automation between iOS apps.

If you are like me and have found that apps like OmniFocus and Things do not fit the way you work, I recommend that you consider NotePlan. Unfortunately, while you can download a trial version of the Mac OS version, you do have to buy the iOS version, which costs $14.99. I've only used the iOS version and the MacOS version has a few additional features, such as the ability to add events and reminders to MacOS Calendar and Reminders app.