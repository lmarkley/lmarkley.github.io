---
layout: post
title: "Gaming keyboards and productivity"
date: 2015-07-29T13:30:00-04:00
---

# Gaming keyboards and productivity

It turns out that computers that are good for doing complex mathematics, large calculation, and parallel processing, are also good for gaming. Interestingly enough, gaming keyboards are also good for things other than gaming. They happen to be, for the most part, well-crafted, mechanical, and possess macro keys that can be used in many ways. In this post, I would like to give an anecdotal look at how a gaming keyboard can be repurposed for productivity, particularly with regard to programming.

## Macro keys: shortcuts galore

I have a Logitech G910 "Orion Spark"[^Orion] with a numerical pad and also nine programmable macro keys [^keys]. With Logitech's Gaming Software, you can assign these macro keys to a regular old single key, a many-key shortcut, a macro, or even to enter a block of text. Basically, you can have those keys do *anything* you can come up with.

For example, I use one such macro key to enter my signature for emails. This may not seem very useful at first, but if you write a lot of emails for different purposes, it's nice to have a way to add a signature when needed sporadically. I have another couple of macros that launch my Cygwin terminal (currently using the Babun distribution from an [earlier post](http://particles.fitzlarolds.net/Nmap-and-other-things/)) and send commands to connect to an SSH session on a remote machine. This reduces my clicking and typing to a single keystroke. These are some *simple* examples of things you can do with macros; I am finding new uses every time I log in to my computer.

### Keyboard shortcuts with AutoHotkey

Many programs come with multi-key, system-wide shortcuts, and many don't. A way around this is to use [AutoHotkey](http://ahkscript.org/) to set up your own keyboard shortcut for any program you want [^ahk]. To be honest, I haven't even begun to scratch the surface of what AutoHotkey is capable of. You can do anything from remapping keys to increase productivity, to launching GUIs to run much more complicated applications. I have a shortcut that just launches my favorite terminal emulator. I also have a shortcut to change my wallpaper to a random image in a folder I've designated. The others that I have made work in conjunction with the Logitech Gaming Software to enter more complicated streams of text, even prompting for user input occasionally.

### Other remarks

I recommend having some macros or shortcuts to anyone that does a lot of repetitive tasks on their computer and want to optimize their workflow. I know that the above isn't much of an introduction, but as I learn more, I will add more to this post (so we can learn together!).

[^keys]: You can have three preset profiles on the keyboard. So, if you utilize all of the available shortcut power, you have access to 27 macros.

[^ahk]: AutoHotkey is an extremely robust tool. It is far from limited to just opening programs. You can script it to do just about anything and assign that script to a keyboard shortcut.

[^Orion]: This is a really nice keyboard. At first I thought it looked a little excessive; the little stand for your smart phone seemed like a silly gimmick (and still does). However, the ease of use of the software and the build quality outweighed my initial trepidation.
