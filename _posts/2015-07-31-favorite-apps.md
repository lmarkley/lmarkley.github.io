---
layout: post
title: "My favorite iOS applications"
date: 2015-07-31T18:15:00-04:00
---

Below I have collected my favorite iOS applications. I have spent a long time vetting the applications in this post, and I plan to add and subtract from it as necessary.

### Email client: Dispatch

I haven't been able to find an email client application that can replace Dispatch on iOS. And that's saying something because I have tried, just to prove a point.

This "app" (one of the most overused words anymore) is a productivity powerhouse. You can export messages in a variety of formats (PDF, PNG, text, etc.) and send emails to a variety of third-party applications for parsing or storing. For example, when I get an important email with a timeframe, I can send it to Todoist (more on Todoist later) and create a task with a due date, reminders, a specific priority, and keep things organized by putting it in the proper "project".

Another wonderful thing about Dispatch is the overall UI/UX. It's a beautiful app; simple, clean, and easy to use. I have a lot of folders in my email accounts, and I can pick the most used ones to be pinned to a side bar.

Finally, the swipes: they are customizable and easy to use.

I recommend Dispatch to people who like combining the use of other services with their email workflow, and who might be considered "power users". It is a powerful tool if you know how to use it.

[Dispatch: Action-based email](http://www.dispatchapp.net)

### Task manager: Todoist

I hate to sound like a shameless fanboy, but Todoist *made me more productive*. It is an intuitive program with a gentle learning curve. The UI is simple. You add tasks, you complete them. You can make it as robust as you want by adding projects, sub-tasks, tags, and reminders.

My favorite feature, however, is "Karma". You earn Karma for finishing tasks. I use it to compete with myself; to see if I can get more done this week than last.

I recommend Todoist to people who like keeping track of what they get done, a good system of self-reinforcement, and a simple interface but powerful interface.

[Todoist website](http://www.todoist.com)

### For editing code on the go: Textastic

I have tried a few applications for editing code on my iPhone (it seems silly, but a little necessary change here or there happens so often that it becomes justified quickly), but the best that I've come across is Textastic. It has support for nearly any programming language you can throw at it and has good syntax highlighting themes. It also has the ability to link to cloud storage and SFTP servers, which is useful for working remotely.

The interface is very simple: you can add remote sites, download files, edit files, create new ones, etc. all with a few swipes of the thumb. It really doesn't get any more straightforward, and the utility speaks for itself. I recommend this application to anyone who needs to edit a variety of files on the go, or even just write ideas down in plain text or markdown.

[Textastic website](http://www.textasticapp.com)

### Writing on the go: Editorial

To say that Editorial is *just* a writing app would be do it a great disservice; it is a very flexible, customizable text editor with the ability to create workflows and scripting to increase productivity and generally just do some really neat stuff.

For example, most of the first iteration of this post was written in and published from Editorial using user-created and submitted workflows. Workflows can be as simple as copying all of the text as plain text or HTML, to interacting with APIs and uploading a blog post to GitHub (as was done here).

Not only is Editorial useful, it is also very clean, well-crafted, and a pleasure to use.

[Editorial for iOS](http://omz-software.com/editorial/)

### Notes (and then some): Drafts 4

Drafts 4 is one of those apps that you may see and say, "$10 for a note-taking app?!". However, let me say that, much like with Editorial, saying that this is just a note-taking app is doing it a disservice. Drafts 4 is great for jotting down a quick note, no two ways about it. But what do you do with that note once you've written it down? With Drafts, you can do any number of things like searching for an address you've written down, adding a task in Todoist (or another app with a **URL Scheme**[^schemes]), or adding links to a read-it-later app; it uses short "actions" to do these things with the text you supply.

[Drafts 4](http://agiletortise.com/drafts/)

### Swiss army knife: Pythonista

I've been waiting to write about Pythonista because I wasn't sure how to categorize it. What category do you put an application that can do almost anything? So I decided to make one up.

Pythonista is nominally an IDE (Integrated Development Environment) for Python 2.7. As I'm writing this (on 1 August 2015), Pythonista is in version 1.5 with version 1.6 being actively vetted by the developer and a lively (and friendly) community of contributors. As an IDE, you are able to write and run code written in Python 2.7 in a sort of "sandbox" in the app, natively on iOS. This opens a multitude of potential uses. A few functions that I know of are:

* an integrated web browser,
* interactions with various sensor in your device,
* access to the clipboard,
* static website creation (made possible by an integrated HTTP server),
* an extremely robust and flexible math library (numpy) and graphing library (matplotlib) that make a very powerful graphing calculator,
* ways to interact with APIs, such as that of Dropbox or Philips Hue,
* and even access to new modules and scripts from the vast frontier of the Internet.

These are just what I've encountered; they barely scratch the *current* capabilities of the application. Capabilities that are bound to expand in the next iteration.

I started off using Python to prototype algorithms for my research in computational physics (yes, it's that good) and have even used it for experimenting in my graduate-level computer science classes. I'll include some code I wrote *entirely* in Pythonista below (part of a proof-of-concept RSA algorithm implementation).

*Note* this is an implementation of Fermat's Little Theorem, a test of primality. I can't really vouch for how well it works, but it worked for my very basic purposes. I just wanted to show how easy writing code is in Pythonista.

	def fermat ( prime_length ):
		if prime_length <= 0:
			return 0;
		N = random.randrange(mod_pow(10,prime_length-1), mod_pow(10,prime_length))
		if (N%2) == 0:
			N += 1
		correct = 0
		for i in xrange(0,20):
			test_num = random.randint(1,N-1)
			if mod_pow(test_num,N-1,N) == 1:
				correct = correct + 1
		if correct >= 19:
			return N;
		else:
			return 0;

My personal opinion is that Pythonista is the most useful, most well-crafted application I have ever used or heard of. The developer is an artist as much as he is a gifted programmer. I recommend it to beginning and advanced programmers alike.

### The ultimate remote access utility bundle: Prompt 2, Transmit, and Coda

All of these applications are made by a company called Panic. They make apps of superior quality, so I recommend them as an entity to programmers and especially web designers/programmers.

#### Prompt 2

Prompt 2 is a well-designed and easy to use SSH client. Have RSA keys for password-less authentication? Great. Prompt has you covered with a sort of "keychain" for them. It also has a repository for snippets, commonly used commands or sequences of commands, that can be global or site specific. You can also group your sites into folders to stay organized.

#### Transmit

Transmit is a remote file access client that can use a variety of protocols. To reiterate my description of Prompt, it is well-designed. It has a local file manager also, so that you can create and upload or download and edit files right on your device.

#### Coda (for iOS)

I purchased "Diet Coda" for the iPad about two years ago (the spiritual predecessor to Coda for iOS) and was elated to see it had been updated. Of course, by "updated" I mean completely rewritten and redesigned. The only minor annoyance is that it had been rewritten to encompass the functionality of Prompt 2 and Transmit, so I wish I could have just bought it first. However, all things considered, I have gotten my money's worth out of all three, so no hard feelings, Panic. Thanks for writing great apps.

Back to the functionality of the app. Remote sites can be organized into folders, keys can still be added and saved, and snippets can also be saved for use globally and site-specifically. One little detail that I absolutely love is that I can load a custom font and use it in the editor. Which is nice because I really like this font, [Monoid](https://github.com/larsenwork/monoid), on GitHub. As a matter of fact, so much attention to detail has been put into this app that there are lots of neat little bonuses hidden throughout the application.

This is the link to the [Panic Inc. website](https://panic.com/).

----

### Further apps to add

1. Pythonista -- check
2. Coda for iOS -- check
3. Prompt 2 -- check
4. Transmit -- check
5. Workflow
6. 1Password
7. ProCamera 8

[^schemes]: URL schemes are ways of passing data between applications on iOS. They are basically special URLs that call applications rather than websites (i.e. `editorial://` as opposed to `https://`). They can be extremely useful for automating certain tasks, like adding an email to a note or converting markdown to HTML in another app. If you are looking for more information on URL schemes, check [HandleOpenURL](http://handleopenurl.com/about-handleopenurl) and the [Apple Developer page on URL Schemes](https://developer.apple.com/library/ios/featuredarticles/iPhoneURLScheme_Reference/Introduction/Introduction.html).
