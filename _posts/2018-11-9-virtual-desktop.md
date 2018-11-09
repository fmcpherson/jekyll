---
layout: post
date: 2018-11-9 17:34
title: Virtual Desktop
comments: false
category:
- computers
tags:
- iPad,
- Windows
---
I've tinkered on and off with the idea of having a virtual desktop in the cloud, and the challenge has been to having something that is functional but doesn't cost a lot of money. It is real easy and inexpensive to run a Linux server for terminal access, but I would at least like to have access to a desktop browser and a good markdown editor.

In addition to being able to run GUI desktop applications like Chromium and Typora, my ideal set up will not only be accessed from desktop computers but also iOS and Android. I also am curious whether once I get a new Chromebook I'll be able to run Linux versions of remote access software.

I recently decided to take advantage of a couple free month's credit at Digital Ocean to experiment with different Linux XFCE desktop options. In each case I've started with a standard Ubuntu 18.04 server that has 1 vCPU and 1 GB of RAM, which has the lowest per month price at $5 per month. To that standard server I installed XFCE and then different remote access software. 

First, I tried [VNC](https://www.tightvnc.com/), which I have found has a few challenges. One is that its protocol is not secure so you need to first create a SSH tunnel and then connect the VNC session to the tunnel in order to communicate with the remote desktop. The second problem I've seen with VNC is that compared to the other options that I've tried, NoMachine and X2Go, it has the slow performance.

Next, I tried [NoMachine](https://www.nomachine.com/), for which there are clients for iOS, MacOS, and Windows. Unfortunately, I found that the NoMachine Linux server component uses nearly 1 GB of RAM, which does not leave enough RAM for using Chromium. I could load Chromium on a remote XFCE desktop but it would not load any web pages until I increased the RAM on the Ubuntu server to 2 GB. While NoMachine performs well with 2 GB that amount of memory doubles the monthly cost, which is more than I want to pay. 

I then tried [XRDP](https://github.com/neutrinolabs/xrdp), which is the X-windows version of the Remote Desktop Protocol commonly used to remotely access Windows. In this case I found remote access via the Windows Remote Desktop app too slow, when I type there is a very noticeable lag between character display and what I type therefore making it unusable. I tried different display configurations on the client that did improve performance but did not eliminate the lag. 

What I did find, however, is that when using the Microsoft RDP app for iOS to access the desktop using XRDP performance was very good, with no noticeable lag and therefore providing a functional XFCE desktop on my iPad. 

Finally, I tried [X2Go](https://wiki.x2go.org/doku.php), which is a X-windows remote access solution that has clients for Windows, Mac, and Linux. Of all the solutions I tried with Windows, I found X2Go provides the best performance. The problem is that there is no functional X2Go client for iOS. While you will find a X2Go app in the App Store, I could not get it to work on my iPad Pro. 

At this point, it appeared I had to make a compromise. Either use XRDP to provide access to iOS with good performance and tolerate the poor performance from Windows, or use X2Go and just access the remote desktop from Windows. 

What if, I wondered, I ran both XRDP and X2Go, will there be enough memory left on the server so that it will be functional? I built another server and installed both solutions and found that it indeed did work, I can use X2Go from Windows and RDP from my iPad and have a functional XFCE desktop, so I am going to run with this configuration. 

The ideal I think is to have a working X2Go client for iOS so that I can eliminate XRDP and free up that memory on the server. Another option is to use NoMachine with a server that has 2 GB of memory, which could be appealing if the cost of 2 GB virtual servers comes down; right now Lightsail, Digital Ocean, and Linode all charge $10 per month for such servers. I could go with AWS/EC2 and spin up the server on demand and turn off when I don't need it, but that requires access to turn the server on and part of the point is to have the remote desktop available when I need it. 

Since the new iPad Pro announcements I've seen reviews stating that while they now have desktop-class processing and USB-C port, iOS constrains how one uses that hardware. It's also noted that one cannot write applications on iOS. A remote access solution such as I describe above provides a way to use desktop-class software, like development tools, with an iPad. Granted, doing so requires a network connection and the additional cost of a virtual server, but the point is that it is possible.