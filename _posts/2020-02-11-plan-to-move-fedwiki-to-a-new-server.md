---
layout: post
title:  Plan To Move Fedwiki To A New Server
date:   2020-02-11 18:01:03
categories: stories
---
It started with an email from Github. The email basically said that the API used to authenticate via Github OAuth is being deprecated and to make a change to my app and I have to July 1, 2020 to make the change.
The app in reference is wiki and specifically [the Passport OAuth](https://github.com/fedwiki/wiki-security-passportjs/blob/master/docs/configuration.md) used to access my site and make changes to it. I went to [the Fedwiki Github](https://github.com/fedwiki) to see if there was any information and not finding any I created [an issue.](https://github.com/fedwiki/wiki/issues/129) 
Next, I logged on to the terminal for my Fedwiki server and ran a command to check to see if there was a new version of the wiki software.

I found that while I have 0.17.0 installed the latest is 0.21.0 and thus I began the process for upgrading the software on my server. First, I created a new snapshot of my server, which is a droplet on Digital Ocean. 
It is fortunate that I created that snapshot because in the process of upgrading I found that I need version 10 or newer of Nodejs and I only found that out while running the command to upgrade wiki. Unfortunately, by running the install I had put a new version of the code on my server that will not run under the version of Nodejs installed on that server.

I then began to try upgrading from v8.17.0 of Nodjes to v10.x and ran into the issue that no matter what I did it would not install. Ultimately I found a forum post stating that versions of Nodejs newer than V8 will not install on 32-bit servers, which turns out is the machine type I selected when I originally built the droplet. The forum message is backed by [information on nodesource](https://github.com/nodesource/distributions/blob/master/README.md#deb) indicating that Nodejs 10 or later is not available for i386 (32-bit) architecture running Ubuntu and Debian.

There is no way to upgrade from a 32-bit droplet to a 64-bit droplet so I am left with the task of migrating my Federated Wiki site to a new server, and here is where I need to think through the process. 
I know that my wiki content is stored in ~/.wiki so I think migrating my site involves copying the contents of ~/.wiki to the new server. The question is, do I copy this folder over before I install wiki, or install wiki first, test, and then migrate? Currently think I will install and test first before migrating.

I currently run the server in a tmux session, so I will need to install it on the new server.
Caddy is a proxy for the site so I will need to install it copy ~/Caddyfile to the new server. I anticipate a challenge with the domain name and any associated SSL certificate that is associated to it. Therefore, I will first create a new subdomain, tmpwiki on frankmcpherson.net and create an A record to tmpwiki.frankmcpherson.net on Hover.

Before I execute my plan I need to search for information about migrating wiki site to a new server.