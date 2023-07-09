<h1 align=center>idnOS</h1>

<p align=center>A project to create an immutable remotely-controllable locked-in debian-based distro.</p>
<p align=center><i>Planned to be renamed to <code>pandanOS</code> soon after</i></p>

> I wanted to say that I have not taken a look into this project for a while as I am getting busy lately and my project partner is also busy on his own stuff. Sorry.

## Vision

idnOS is a whole full-blown linux distribution that is immutable, locked-in, and controllable. It features two variants of the distro: the Nucleus and the Ribosome (both are inspired from the plant's cell strucutre). Basically the Nucleus is the server that controls the Ribosomes (not very accurate in biological terms, but I can't find other better names). It could do things like instant updates to them (one click updates all the ribosomes), get a live feed from their logs, screen, inputs; basically spy on them...

<p align=center><img src="https://github.com/idnOS/.github/assets/31884435/ac1ea143-e1aa-4750-8acb-b58cb0b1dc49" /></p>

### Where the idea came from

To address the angry forks of libre software idealists, I would like to share a bit of the fuzz that's going in our school. Our school is an IT school, where students are pretty much required to bring their own laptop to class to, well, learn to code. Since everyone is able to access the internet freely, of course someone (and I mean everyone) is going to make use of that privilige to do some, not good things (to put it lightly).

So I thought maybe if I could pledge to my school to force everyone to install linux (lol), and a distro that can spy on them (lmao), that'd wreck them. I know, I know it sounds bad, but if you're dealing with those thugs, you gotta get geared up.

<img align=right src="https://github.com/idnOS/.github/assets/31884435/d651da1a-f5f2-42df-988e-3114377b90c8" />

Aside from this weird story, I could see some real-world usage in like CBT (computer-based tests) exams, where of course it is needed for us to be able to track what they're doing. Where I'm starting to think that, this is a good solution to my previous problem lol. I would never want something like that myself, so I decided to change its course for these specific uses.

## Details

To run idnOS, you'd require at least two computers running two different variants connected to each other. It is modeled by the good old client-server architecture. The server is called the Nucleus, and the clients are called the Ribosomes. Ideally, ribosomes connect to nucleuses through a fast LAN connection, because both sides will be transcieving a lot of data to each other.

Ribosomes are required to connect to their Nucleus, at first install of Ribosome, the user is prompted to give an address that would resolve to a Nucleus, and it will register itself to the Nucleus. If a Ribosome is disconnected from the LAN or its connection between the Nucleus gets interrupted, the Ribosome will stop working.

<img align=left src="https://github.com/idnOS/.github/assets/31884435/85759703-b829-4a7f-a47b-fa2031275697" />

To guarantee immutability, we're planning to use ostree to mount the root structure of either variants, and make them read-only. The only difference being that the Nucleus has admin powers to control over it, and the Ribosomes' ostree instance isn't actually connected to the outside world, it's connected to the locally-run ostree instance in the Nucleus, so everything can be controlled from the Nucleus. This makes updating more reliable, faster, and easier; we can be sure that every Ribosome have the same system no matter what.

The connecting, and controlling aspect of this distro is provided through some custom-built software, and (very) possibly kernel modules.

## The Main Character

Couldn't express much gratitude to my code partner, @fathonix who studies in the same school as I do (but he's actually one class ahead of me lol). He has put so much effort and thinking to this weird project that came up to our minds as we were strolling around the woods of the rainforest. We had a lot of fun discussing aspects from booting, initramfs, to the desktop and UX experiences. Sadly he's getting a bit busy and is unable to assist in this project anymore, and so as I do.

## Looking forward

To these days, we've been thinking and planning every flaws or steps we need to look out for to build idnOS. idnOS is not in a stage where you could use, heck or even see any bits of code of it. We've been experimenting with things here and there to make a some kind of proof-of-concept. We've been considering things like drivers, printers, connection model, and etc, but haven't got the time to actually realise them.

For now, we'll be leaving this scrap of idea floating in the void of space, waiting for someone like You <3 who might care enough to help its development. Soon enough we might try revisiting this project once we're done with our other funs, sorry and thanks :)
