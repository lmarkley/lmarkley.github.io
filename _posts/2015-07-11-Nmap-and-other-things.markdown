---
layout: post
title: "Playing around with BASH and other tools"
date: 2015-07-11T17:14:00-04:00
---

# A "Bourne" again shell scripter

I've been playing around with bash (the Bourne Again SHell) scripts for about two years now. At first, it was a passing necessity to automate programs for the research I was working on. Then I realized the tremendous power that lie within scripting in bash. I think about it like this: You are essentially giving directions *directly* to the "brain" of your computer. All that raw power at your fingertips without having to go through someone else's "black box" of a user interface, that does god-knows-what behind the scenes; it is exhilarating (to a nerd like me). 

That is not to say that you can't **severely** screw up everything on your computer with this stuff (I have on many occasions done just that), but if you do your homework and experiment a little you're usually safe. 

## SSH, SCP, & SFTP

I do a lot of work remotely. Needless to say, I don't want everyone in the world to be able to pick what I'm doing out of the air and have access to any personal data. So I employ the use of SSL (Secure Socket Layer) encryption in the form of SSH, SCP, and SFTP; which are Secure SHell, Secure CoPy, and Secure File Transfer Protocol, respectively. You may have heard of SSL, it is responsible for encrypting anything from secure chats to bank transfers, and with the exception of a few problems (like Heartbleed) it has worked well (especially for being open-source and staffed by mostly volunteers as I understand it). I won't go into the details of exactly how it works (I don't understand it fully, so I wouldn't feel comfortable), but I might throw in an example or two later on. Of the three, I use SSH the most to run remote commands to do work while I'm away (and even to tunnel a VNC session if I have enough bandwidth). 

To be continued....
