---
layout: post
title: "Filtering the Static"
date: 2015-12-02T19:55:00-05:00
feature_image: static
---

## A brief history of signals

Humans communicate in so many ways: a wry smile, a business email, a loud conversation at a bar, a light brush of the shoulder, the list goes on indefinitely. There are nearly infinite combinations and permutations of ways through which we convey our thoughts and ideas. In the past, we were limited to shouting distance; then through advances land, sea, and air transportation, we extended and expedited our means of communication. Until the 20th century, we were limited to *physically* transferring our information from point A to point B through a series of intermediaries.

Then, in a scientific and technological revolution of unequaled scope, humanity extended its reach effectively to infinity: we learned to use electromagnetic radiation to send our messages. We could transmit and receive messages anywhere almost instantaneously. And we did. A lot. However, in the hubris of our innovation, we neglected to think ahead to an age where the air was so permeated with information, that an individual or group could just reach out and grab that information at will.

Only recently has the idea of protecting this flood of information about ourselves become mainstream. Every day we are inundated with words like 'encryption', 'metadata', 'hacking', and 'mass surveillance', yet most of us have no idea what some or any of them mean.

I am not going to delve into the deep end of the pool and try to discuss all of these topics in depth—or even topically—because it would take too long and there are better people to do so than me. Yet I still want to say *something* about all of this noise, to do my part to help reveal the signal buried within.

----

## Boxes and keys?

The goal of encryption is-in a grossly oversimplified way-to allow for communication between two parties without worrying about a third (often nefarious) party being able to know what the two parties are saying to one another. There are two big flavors of encryption: *symmetric* and *asymmetric*. The best way of describing them that I have ever encountered comes (perhaps ironically) from a conversation between Neil deGrasse Tyson and Edward Snowden on the podcast[^3],[^4] *Star Talk Radio*: 

* **Symmetric encryption** is when I have a box, I lock it with key A and send it to you, who then unlocks it with that same key A. Simply, the same key can lock and unlock the box.

* **Asymmetric encryption** is when there are two keys, A and B, to the box. A can only lock the box, while B can only unlock it. A useful feature of this is that if you have key B, you can't lock the box and give it to someone else while pretending that I put everything in it.

To paraphrase Tyson and Snowden again: Ideally, a third party won't even know they are looking at a communication because it's so well encrypted, it looks like noise.

If you've ever sent an encrypted email, or at least heard of folks doing so, they're *probably* utilizing asymmetric encryption. 

----

## Because why not get political?

<iframe width="420" height="315" src="https://www.youtube.com/embed/OMOGaugKpzs" frameborder="0" allowfullscreen></iframe>

The reason I mention this (other than to educate) is to say that some folks (mostly governments and hackers, you decide which is more scary) want a master key that unlocks and locks all of the boxes. Governments want cryptographic protocols to implement a "back door" that only they can access, "hackers" just want there to be a mistake or bug to exploit (again, you decide which is scarier) in order to forge a key. Governments wanting a "back door" into encrypted messages may seem fine at first glance. One might think, "Well of course, can't have the baddies talking all sneaky to each other!" Or "Well of course the government needs this for national security!" Or (my personal favorite), "Well *I* have nothing to hide, so what if they know everything about me?" 

While with the first two I could *almost* see your point, that last one is addressed by none other than the aforementioned whistleblower/traitor/patriot/criminal in the aforementioned conversation in the following way (excuse my paraphrasing): Saying that mass surveillance should be allowed because you have nothing to hide, is like saying the First Amendment is unnecessary because you have nothing to say. That may be a misappropriation of Snowden's comment in the interview, but I did my best to get the point. 

And in case you thought you were going to get away with thinking one or both of the first two, I have one phrase for you: "Who will guard the guards?"[^2] You're putting an awful lot of trust in a government that is supposed to *serve* the people, not spy on them with impunity [^5],[^6],[^7]. This is a country where free and open discourse is not only encouraged, but protected by the highest law. Then again, this is also the same country that has Donald Trump as a front-runner for President and where doctors won't stand up to a bully that cites anecdotal evidence and discredited research to claim that vaccines cause autism [^1], so maybe I'm barking up the wrong tree.

What started out as a short PSA on encryption has (surprisingly enough to me) ended up as a treatise advocating privacy. For that, dear reader, I apologize.

Then again, as us youngsters say these days, "Sorry I'm not sorry."

![](https://media.giphy.com/media/h52b5GULWNVRe/giphy.gif)

[^3]: [Star Talk Radio: A Conversation with Edward Snowden, Part 1](http://www.startalkradio.net/show/a-conversation-with-edward-snowden-part-1/)

[^4]: [Star Talk Radio: A Conversation with Edward Snowden, Part 2](http://www.startalkradio.net/show/a-conversation-with-edward-snowden-part-2/)

[^2]: *"Quis custodiet ipsos custodes?"* [Wikipedia](https://en.m.wikipedia.org/wiki/Quis_custodiet_ipsos_custodes%3F)

[^5]: [The Verge: The US government is already lying like crazy about surveillance after the Paris attacks](http://www.theverge.com/2015/11/16/9745932/paris-attack-terrorism-surveillance-cia-brennan)

[^6]: [Ars Technica: It’s official—NSA did keep its e-mail metadata program after it “ended” in 2011](http://arstechnica.com/tech-policy/2015/11/nsa-replaced-secret-e-mail-metadata-program-with-more-expansive-tools/)

[^7]: I would be remiss for not mentioning that there are *hundreds* (if not thousands) of articles describing ways in which many governments engage in rampant mass surveillance on their citizens.

[^1]: I am referring to presidential hopeful Ben Carson (a surgeon) all but *agreeing* with Trump after the latter defecated loudly all over one of the pinnacles of modern medicine. Sorry, I've no tolerance for pseudo-scientific smoke-blowing.