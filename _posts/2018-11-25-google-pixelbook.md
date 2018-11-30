---
layout: post
date: 2018-11-25 15:11
title: The Google Pixelbook
comments: false
category:
- computers
- 
tags:
- 
---
Last update: 2018-11-26

[As I wrote previously](https://writing.frankmcpherson.net/computers/2018/10/31/time-for-new-computer.html), over the course of six weeks I considered several different Chromebooks before deciding to buy the Google Pixelbook. On this page I am going to document my experience with setting up and using the Pixelbook, you can see my raw notes in [my Work Notes outline](http://instantoutliner.com/41).

## Out Of Box Experience
Google, like most hardware companies, copies Apple in their out of box experience, investing in the packaging. In the end there isn't much in the box, the Pixelbook, power supply, and that's it. The box, and its form fitting insides, is destined for the recycle bin.

The quick and easy set up process is a strength for Chrome OS. I logged in using my Google credentials and my past Chrome OS apps appear in the Launcher. On the other hand, it would be nice if there were a way to tell Chrome OS to boot up with a clean experience and remove prior installed apps. Most of the Chrome OS apps I have on my account are things like terminal and editor apps that I will likely replace with Linux or Android apps.

I don't know which version of Chrome OS was originally installed on the Pixelbook because the update began pretty quickly. Right now I am running version 70. 

## Managing Applications
CrOS 70 has a shelf that is equivalent to the Mac OS dock, you can pin app icons to the shelf, and running apps appear on the shelf. All other applications appear in the Launcher for which there is a  large keyboard button located where one normally finds Caps Lock. 

The fastest way to start an app is to press the Launcher button to display a search box and icons of recently used apps and then start typing the name of the app. If the highlighted icon is for the app you want to run press Enter, or tab through the displayed the app icons to select the one you want to run.

Tap the up arrow to expand the Launcher and display all of the installed apps. You can tap and hold an icon to display a menu of options that include Remove from Chrome. Unfortunately, as soon as you remove an app the Launcher closes.

There is not a quick way to expand the Launcher. The natural approach to me would be to press the Launcher button a second time to expand but that instead closes the Launcher. You can tap the up arrow or use the mouse to click, but I think there needs to be a keyboard accelerator to expand the launcher, and there might be one that I have yet to find. 

A faster way to remove a bunch of apps is to go into the Chrome browser settings, More tools, Extensions to list all of the Chrome extensions and apps which you can then click to Remove.

Android and Chrome OS apps have the same type of icon in the Launcher, so there is no way to distinguish between the two, if that matters. All Linux apps, on the other hand, appear in a separate group, and I wonder if this separation will remain when Linux apps come out of beta.

## Running Android and Linux Apps

One reason why I chose to buy a new Chromebook is because of Chrome OS' ability to run Android and Linux applications. Android app support is officially available on the Pixelbook because it comes with the Google Play store built-in. Linux apps support is still in beta and therefore has to be enabled via Settings. 

In my experience so far, I observe two issues regarding Android and Linux app support. The first issue is, if an app is available for more than one of these platforms, which version of the app should I use? A related, issue is that while all compatible apps will run there can be some pretty significant display issues, either with scaling or just poor use of screen real estate. 

For example, should I use the Evernote app for Android or the Evernote web app? I have found the Evernote Android app to run very much like the Windows version and it looks pretty nice on the Pixelbook screen but you can still tell it was designed for a smaller display whereas the web version is clearly designed for larger displays. 

The most significant scaling issue I have seen so far is with Sublime Text. The default app scaling makes the text and UI elements unreadable. Fortunately, you can increase the UI scaling by clicking Preferences, Settings to display a split screen of the default settings and your user preferences. The user preferences may be blank with two curly braces. To increase the UI scaling to something more readable enter:

`"ui_scale": 2.0` 

in the user preferences, click the X to close the Preferences Settings tabs and then restart the app. Note: if there more than one user preference line make sure each one but the last line ends with a comma.

## USB-C Dock

I am going to get a USB-C dock to make it easier to connect the Pixelbook to peripherals like my monitor when I am in the home office. It looks like there are two types of docks, those that have their own power supply that then supplies power to the Pixelbook and those that requires the Pixelbook's power supply. Because I plan to leave this dock on my desk, I want one that has its own power supply. 

So far in my research I have identified two candidates: [the OWC USB-C dock](https://www.amazon.com/dp/B073BDY5J5/?coliid=IRVHAT0RZVFYT&colid=2OSYVCFR78X3K&psc=0&ref_=lv_ov_lig_dp_it) and [the Pluggable USB-C dock](https://www.amazon.com/dp/B076HXWR9M/?coliid=I3S8Q3HU54TEG5&colid=2OSYVCFR78X3K&psc=0&ref_=lv_ov_lig_dp_it); both brands are recommended by Chrome Unboxed. The Pluggable dock has more ports but the OWC dock has a SD card slot that I favor. 

## SmartLock

SmartLock is a feature that uses an Android phone for authentication to log in to Chrome OS, and it is one of the first Chrome OS features that I tried to enable on the Pixelbook. For some reason, I would go through the setup process, receive confirmation emails that the feature is enabled, but not see anything on the Chromebook. 

Last night I shutdown the Pixelbook rather than simply put it to sleep by closing the lid, and when I started it up today, SmartLock was enabled. Apparently one needed to reboot and login to the Pixelbook with your password to get it to work despite there being no direction to do so. So far SmartLock continues to work for me ever since this reboot.

With SmartLock enabled, to log in to the Pixelbook you must unlock your phone and then click your photo on the Chromebook lock screen. I have configured SmartLock on my Pixel 2 to unlock the phone while I am at home and so when I am home and the Pixel 2 is unlocked I can simply click my photo to login on the Pixelbook. All other login methods such as using PIN and password remain available. 