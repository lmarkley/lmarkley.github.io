---
layout: post
title: "A 'Bourne again' shell scripter"
date: 2015-07-11T17:14:00-04:00
---

I've been playing around with bash (the Bourne Again SHell) scripts for about two years now. At first, it was a passing necessity to automate programs for the research I was working on. Then I realized the tremendous power that lie within scripting in bash. I think about it like this: You are essentially giving directions *directly* to the "brain" of your computer. All that raw power at your fingertips without having to go through someone else's "black box" of a user interface, that does god-knows-what behind the scenes; it is exhilarating (to a nerd like me). 

That is not to say that you can't **severely** screw up everything on your computer with this stuff (I have on many occasions done just that), but if you do your homework and experiment a little you're usually safe. 

### SSH, SCP, & SFTP

I do a lot of work remotely. Needless to say, I don't want everyone in the world to be able to pick what I'm doing out of the air and have access to any personal data. So I employ the use of SSL (Secure Socket Layer) encryption in the form of SSH, SCP, and SFTP; which are Secure SHell, Secure CoPy, and Secure File Transfer Protocol, respectively. You may have heard of SSL, it is responsible for encrypting anything from secure chats to bank transfers, and with the exception of a few problems (like Heartbleed) it has worked well (especially for being open-source and staffed by mostly volunteers as I understand it). I won't go into the details of exactly how it works (I don't understand it fully, so I wouldn't feel comfortable), but I might throw in an example or two later on. Of the three, I use SSH the most to run remote commands to do work while I'm away (and even to tunnel a VNC session if I have enough bandwidth). 

### Network tools

There are some really nice network tools available for bash. I'll go over a few (there are *tons*) here and give a brief overview of some things that they can do. 

#### Ping

Ping is probably the best known of all of the network tools (possibly even command line tools) in bash. It has extensive applications, but most commonly I use it to see how well one computer (a client) is communicating with another (a host). For example, if I wanted to see if my computer was communicating well with my router (located at, say, 10.0.0.1 which is an IP address) I would enter

    ping 10.0.0.1

That's it! Then it will send some information to the host and see how much it gets back. The more it gets back, the better. Again, that's not all, but it's enough to get you going!

#### Arp

ARP stands for "Address Resolution Protocol". It is how computers know where one another are, and how to get from point A to point B (so to speak) in a network. The `arp -a` returns the ARP table for the network you are connected to, with all of the live hosts (network devices that are connected and on) and their IP and MAC addresses. This is useful information if you want to know how many devices are connected to your network and "where" they are on it. 

#### Nmap 

Nmap doesn't come stock with bash; it is third party software but it is one of my favorites so I'm mentioning it. Before I go on, the obligatory disclaimer: **DO NOT USE NMAP ANYWHERE YOU SHOULDN'T** and **IF YOU AREN'T SURE YOU ARE ALLOWED TO USE IT, YOU PROBABLY AREN'T**. Now that we've that out of the way, Nmap is an incredibly powerful and versatile information gathering tool. It scans the nebulous entities known as ports on a computer; can gather information about the operating system and services available from a computer; and various other features that are rather esoteric. I personally use it to look for my computer when its IP address changes on my local network and I'm not there to check what it might be. There is a GUI version of Nmap called Zenmap that is rather nifty as well. You can find information about Nmap and Zenmap on [the official Nmap site](https://nmap.org).

### File and text tools

#### `vi` (or Vim)

Possibly the most powerful tool at the fingertips of any computer software tinkerer is a good text editor. Luckily, `vi` is a *great* text editor, often lauded as *the* text editor. I have to admit, I've gotten a bit rusty in my Vim skills. I've been spoiled with Sublime Text for some time now. Though having a big, fancy text editor is great, what happens when you don't have those luxuries like a mouse or a user interface? Vim is a veritable (and venerable) Swiss army knife; you *need* to keep it in your pocket, especially out in the wild. To get back to the practical point, `vi` is completely text-based and uses keyboard shortcuts to keep your hands on the keyboard. While it is easy to pick up the basics, becoming proficient can be tough (but it's worth it).

### References

1. [The Art of Command Line](https://github.com/jlevy/the-art-of-command-line)
    - I recently came upon this repository and I was rendered speachless by the wealth of useful information on this page. I recommend checking it out.

2. [Hyperpolyglot: Unix Shells](http://hyperpolyglot.org/unix-shells)
    - I also recently found this gem. It is useful for programming in general, but I've linked to the Unix Shells page here. 


To be continued....
