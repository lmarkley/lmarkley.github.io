---
layout: post
title: "A 'Bourne again' shell scripter"
date: 2015-07-11T17:14:00-04:00
---

I've been playing around with bash (the Bourne Again SHell) scripts for about two years now. At first, it was a passing necessity to automate programs for the research I was working on. Then I realized the tremendous power that lie within scripting in bash. I think about it like this: You are essentially giving directions *directly* to the "brain" of your computer. All that raw power at your fingertips without having to go through someone else's "black box" of a user interface, that does god-knows-what behind the scenes; it is exhilarating (to a nerd like me).

That is not to say that you can't **severely** screw up everything on your computer with this stuff (I have on many occasions done just that), but if you do your homework and experiment a little you're usually safe.

### SSH, SCP, & SFTP

I do a lot of work remotely. Needless to say, I don't want everyone in the world to be able to pick what I'm doing out of the air and have access to any personal data. So I employ the use of SSL (Secure Socket Layer) encryption in the form of SSH, SCP, and SFTP; which are Secure SHell, Secure CoPy, and Secure File Transfer Protocol, respectively. You may have heard of SSL, it is responsible for encrypting anything from secure chats to bank transfers, and with the exception of a few problems (like Heartbleed) it has worked well (especially for being open-source and staffed by mostly volunteers as I understand it). I won't go into the details of exactly how it works (I don't understand it fully, so I wouldn't feel comfortable), but I might throw in an example or two later on. Of the three, I use SSH the most to run remote commands to do work while I'm away (and even to tunnel a VNC session if I have enough bandwidth).

#### SSH

SSH has pretty simple syntax for the most basic applications. For example, if I want to log on to a server called 'myserver' with the username 'bob', on the port '2468' (the default port for SSH is 22, for future reference), I would enter the following in the terminal:

    ssh -p 2468 bob@myserver

Then SSH would prompt me for the password for 'bob', unless I have an SSH key [^keys].

Another cool thing possible with SSH is *tunneling*. It might sound a bit nefarious, but it's used for all sorts of practical things from creating a "poor man's VPN", to circumventing restrictive firewalls, or even just being able to get desktop Gmail at work. There are many types of tunnels, but the one I will share here (without telling you how to do everything, that may require a bit of searching) is for a *dynamic port forwarding tunnel*. In other words, it forwards all of the traffic on your computer through a remote server to the rest of the Internet. This can be done with the following command:

    ssh -D <local port> <user>@<server> -N

The `D` is for dynamic and it takes a port on your local computer as an argument, the `N` is so you don't enter what is called an interactive session (i.e. you can't send commands). It always makes things a little easier to use password-less authentication, but that lies beyond the scope of this post.

#### SCP

The Secure CoPy (SCP) tool can be very useful if you need to send a file to or get a file from somewhere that you don't have physical access to (and possibly don't want to use an SFTP or FTP client, etc.). Again, the syntax is pretty simple for basic stuff. For example, let's say I have the same computer as above and I want to send a shell script ('script.sh') in my home directory (or in the second case, get a shell script *from* the home directory of 'myserver'), then I would enter these commands in the terminal:

    scp -P 2468 shell.sh bob@myserver:~/

or to fetch the same file:

    scp -P 2468 bob@myserver:~/shell.sh ~/

The same thing goes here; you'll be prompted for a password unless you have an SSH key.

### Network tools

There are some really nice network tools available for bash. I'll go over a few (there are *tons*) here and give a brief overview of some things that they can do.

#### Ping

Ping is probably the best known of all of the network tools (possibly even command line tools) in bash. It has extensive applications, but most commonly I use it to see how well one computer (a client) is communicating with another (a host). For example, if I wanted to see if my computer was communicating well with my router (located at, say, 10.0.0.1 which is an IP address) I would enter

    ping 10.0.0.1

That's it! Then it will send some information to the host and see how much it gets back. The more it gets back, the better. Again, that's not all, but it's enough to get you going!

#### Arp

ARP stands for "Address Resolution Protocol". It is how computers know where one another are, and how to get from point A to point B (so to speak) in a network. The `arp -a` returns the ARP table for the network you are connected to, with all of the live hosts (network devices that are connected and on) and their IP and MAC addresses. This is useful information if you want to know how many devices are connected to your network and "where" they are on it.

#### Nmap

Nmap doesn't come stock with bash; it is third party software but it is one of my favorites so I'm mentioning it. Before I go on, the obligatory disclaimer: **DO NOT USE NMAP ANYWHERE YOU SHOULDN'T** and **IF YOU AREN'T SURE YOU ARE ALLOWED TO USE IT, YOU PROBABLY AREN'T**. Now that we've that out of the way, Nmap is an incredibly powerful and versatile information gathering tool. It scans the nebulous entities known as ports on a computer; can gather information about the operating system and services available from a computer; and various other features that are rather esoteric. I personally use it to look for my computer when its IP address changes on my local network and I'm not there to check what it might be. There is a GUI version of Nmap called Zenmap that is rather nifty as well. You can find information about Nmap and Zenmap on [the official Nmap site](https://nmap.org)[^nmap].

### File and text tools

#### `vi` (or Vim)

Possibly the most powerful tool at the fingertips of any computer software tinkerer is a good text editor. Luckily, `vi` is a *great* text editor, often lauded as *the* text editor. I have to admit, I've gotten a bit rusty in my Vim skills. I've been spoiled with Sublime Text for some time now. Though having a big, fancy text editor is great, what happens when you don't have those luxuries like a mouse or a user interface? Vim is a veritable (and venerable) Swiss army knife; you *need* to keep it in your pocket, especially out in the wild. To get back to the practical point, `vi` is completely text-based and uses keyboard shortcuts to keep your hands on the keyboard. While it is easy to pick up the basics, becoming proficient can be tough (but it's worth it).

I am actually editing this section of this post in Vim now. I have to say, even being rusty, the shortcuts and syntax highlighting are still incredible and fast.

### Other tools

#### `tmux`

It is my understanding that `tmux` is short for 'terminal multiplexer', which means that you can have multiple instances of shell in the same terminal session in the form of panes or windows.

<figure> <a href="http://lmarkley.github.io/images/tmux.png"><img src='http://lmarkley.github.io/images/tmux.png'></a> A screenshot of writing this post in Vim using tmux panes.</figcaption></figure>

### Other cool stuff

#### Babun

I discovered [Babun](http://babun.github.io) a few days ago after hearing it on a podcast called "Programming Throwdown" which, by the way, is wonderful. You should listen to it. It's funny *and* informative, though I will warn you that the nominal topic only gets about 15-20 minutes toward the end of the show in my experience [^progthrow]. Babun is an implementation of Cygwin and a lot more; it has many plugins and add-ons and one thing that Cygwin lacks out-of-the-box: an included package manager. It's easy to setup and, as the home page states, doesn't interfere with previous Cygwin installations (I can vouch for that, it didn't mess with mine at all). If you are a Windows user but miss a good (sorry Microsoft...) command line interface, try Babun.

#### Atom

Atom is "A hackable text editor for the 21st Century" as the website states. It is free; open-source; and has a plethora of themes, packages, and add-ons for increased utility. I started using Atom well before its 1.0 date, but found it difficult to work with on Windows. This has since changed; it is as simple to install and use as double clicking the installer and starting it up. It is also cross-platform, which is very nice for a person who uses Linux, OS X, and Windows on a rotating basis (occasionally two simultaneously, which can get really confusing) like me. It is *very* customizable and chic, and I recommend giving it a shot if you like free, open-source, awesome stuff [^atom]

### References

1. [The Art of Command Line](https://github.com/jlevy/the-art-of-command-line)
    - I recently came upon this repository and I was rendered speachless by the wealth of useful information on this page. I recommend checking it out.

2. [Hyperpolyglot: Unix Shells](http://hyperpolyglot.org/unix-shells)
    - I also recently found this gem. It is useful for programming in general, but I've linked to the Unix Shells page here.

To be continued....

[^keys]: I like to think of SSH keys this way (though it is a gross oversimplification): It's like having a security system that you have the master code for, but there are other codes for other people (computers) that you 'trust' (or have authorized) so that they can get in as well. Each of these people (computers) has a unique code (signature) so that you know it is them and not someone else.

[^progthrow]: *Programming Throwdown* is hosted by Jason Gauci and Patrick Wheeler. It is my favorite podcast for several reasons, but mainly because the it is always informative and the hosts have real charisma (albeit a nerdy manifestation of it). Here is a link to the Google+ page if you would like more information: https://plus.google.com/communities/103949530542621693799

[^nmap]: Nmap even has a Python module: `python-nmap`.

[^atom]: More information can be found on the [Atom homepage](http://atom.io), as well as the download links. 
