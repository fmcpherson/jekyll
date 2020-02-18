---
layout: post
title:  Testing Migration Of FedWiki To New Server
date:   2020-02-17 20:01:03
categories: stories
---

As I wrote in [Plan To Move Fedwiki To New Server](https://writing.frankmcpherson.net/stories/2020/02/11/plan-to-move-fedwiki-to-a-new-server.html) I know that I need to build a 64-bit server that can run the latest versions of Nodejs, which is needed to run the latest versions of Federated Wiki. Building a new server is easy, what I have been most concerned about is copying the content of my wiki to the new server along with the site ownership. 

On February 17th, 2020 I installed wiki on a tyrion, which is one of my Raspberry Pis. Tyrion is running Nodejs version 13.7.0. Installation was straight forward and I confirmed success by running wiki -p 3000.

I have a local copy of wiki running on my Pixelbook which I have been using to store content that I do not want accessible via the Internet. I installed wiki on the Pixelbook following [the Laptop Server instructions](https://fedwiki.frankmcpherson.net/view/welcome-visitors/view/laptop-server) with a slight alteration so that it runs within the Crostini container. To test a migration I decided to use rsync to copy the contents and site ownership from the Pixelbook to the Raspberry Pi.

I used rsync to copy the contents of .wiki from my Pixelbook to tyrion after copying a backup to /tmp/wiki. I then started wiki on tyrion and found that while the content transferred the site ownership did not. I recalled that I use a script to start wiki on the Pixelbook for the purpose of specifying the use of friends as the security type, I believe that passport is the default security if friends is not specified. So, I copied the script to tyrion and ran it to start wiki. 

Next I Iogged into the site and created a new page, which succeeded. The final test was to fork a page. I searched for the Migrate Federated Wiki To A New Server page on my public wiki from the site on Tyrion and clicked the flag/fork button on the journal. Next I looked at the Site Index and observed an entry for of the page with flags for the site on Tyrion and Fedwiki. Finally I opened ~/.wiki/pages and observed that the file for the forked page was listed. 

From this experience I conclude that migrating the content of my current wiki to a new server should be straight forward and I am ready to build the new server. I got [a recommendation on Twitter](https://twitter.com/Synesthesia/status/1227504817653809152) to wait on the next LTS of Ubuntu (20.04) targeted for April, 2020. I do wonder, however, whether Digital Ocean will make 20.04 available as soon as it is released of if it will come along later. Given what I have now learned about the migration, I am inclined to go ahead with 18.04. 