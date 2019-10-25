+++
author = "Susan Sons"
categories = ["tools", "Getting Started", "hacker", "infosec"]
date = 2018-04-01T16:26:41Z
description = ""
draft = true
image = "https://images.unsplash.com/photo-1496243975092-6ec259c776e2?ixlib=rb-0.3.5&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max&ixid=eyJhcHBfaWQiOjExNzczfQ&s=7e09d3d808735d7f57025b466e49050f"
slug = "quick-thoughts-on-a-newbie-hackers-laptop"
tags = ["tools", "Getting Started", "hacker", "infosec"]
title = "Quick Thoughts on a Newbie Hacker's Laptop"

+++

I started talking to one of the newbies I mentor yesterday about getting a laptop for infosec learning and experimentation.  I realized that there are a few general guidelines one can follow to make this easy and wanted to share them.

## The Goal In Mind

This list is designed to help a newbie interested in web pentesting, network security, IR (incident response), DFIR(digital forensics), threat modeling/tracking, and several other areas get a foot in the door with minimal initial investment.  It is not meant to provide a full lab or even a professional workstation.  It is not meant to address every possible security specialty.  It is meant to provide an easy bootstrapping platform for someone who doesn't really know what they want to do yet, and who has a typical American teenager budget (the ability to save up $150-$250 from part-time work).

## The Case For a Laptop

Many of us who do this professionally work primarily from laptops.  Others work primarily from desktop systems and carry lightweight laptops or even tablets for information capture on the go.  There are many possible permutations of infosec workstation hardware.  However, I believe that a single laptop is the best investment for the complete newbie who doesn't really understand their use case yet, for the following reasons:

1) A laptop is not dependent on a single vendor for OS updates like a tablet.  You can find up-to-date open source operating systems for even very old laptop and desktop hardware.
2) A laptop is highly mobile, unlike a desktop computer.  When you are a newbie, you will be looking to more experienced people for help.  Go to them, don't ask them to come to you.
3) A laptop is extremely flexible: while this is becoming more true of tablets, there's a much wider array of software and hardware available for a laptop than any other portable platform.
4) A laptop is generally more powerful than a tablet:  there are certainly exceptions these days, but if we're sticking to the most affordable hardware, you will get more bang for your buck in a laptop in terms of processing power, storage, and memory.

## The Right Laptop

Start checking out pawn shops, local resellers, and online stores (ebay, Amazon, anywhere else), for **used T-series Thinkpads that have the Intel on-board video only** (no NVIDIA).  These Thinkpads are so widely used among hackers that their hardware is thoroughly well-supported with the tools we are going to care about for your learning journey, and there is a huge array of cheap aftermarket parts available.  Batteries wear out, hinges break, you don't want a $200 used laptop that dies in six months when you could have a $200 laptop that needs at most a $30 battery replacement.

I can already hear the cries of "well a Mac is perfectly good because...".  I hear this a lot, and I know plenty of professionals who use Macs to good effect.  However, one of my constraints is hardware that can be reliably obtained around $250 or less, and Mac laptops don't meet this criterion.  Additionally, if you plan to learn on a Mac, you had better be *extremely* familiar with Homebrew and able to debug your own system.

How much power you are going to get depends on how much you have to spend, but you can probably find a good candidate around 200 USD in most markets, sometimes less.  Battery replacements and additional RAM are fairly inexpensive, as are hard drives, so focus on getting a reasonably modern processor in something with reasonable body wear and the right video chipset.  If you are part of a local Linux User Group (LUG) or infosec interest group, there are probably enough of these floating around that a more experienced person can help you out with spare parts to some degree.

Again, this is aimed at the easiest platform to bootstrap yourself on as a newbie if you are starting from nothing.  It is not the only platform: if you have a different laptop already in hand, try an install on it and see how frustrated you get before deciding you need to start shopping.

A minimum of 4G of RAM should be your target.  Go for 8G or more if you are buying a new machine you expect to last a long time, or are short on patience.  As of this writing in April of 2018, my primary laptop has 16G and I'm quite pleased with that.  If I need more, I'm probably moving relevant tasks to a desktop or cluster.  Storage needs can vary wildly depending on your habits, so just do what's in your budget and plan to upgrade later (or modify your data management habits) if needed.

## The Right OS

**You'll be best served by starting with Linux, period.**

A number of people will complain about this dictat, and they'll have many use cases for which Linux isn't the absolute best choice.  Please go back to the beginning of my post where I stated that the goal here, for this particplar article, is to produce a cheap, easy path for folks trying to learn infosec who don't yet understand what specialty they will pursue or what their use case will ultimately be.

Too often, I see newbies stick to Windows or Mac OS because they have used it before and are most comfortable with those OSes.  One problem is that only a select few infosec subspecialties use Windows at all, so the tools available there are limited for other subspecialties.  Sticking with Windows locks you out of a great number of exploratory paths.  Another is that there are a great deal more free, pro-grade tools available for Linux right now than any other OS.  A newbie doesn't need to invest in hundreds of dollars in software licensing to try out this skill tree or that before they've decided what they really want to do.  Many of those tools *are* being ported to Mac OS lately, but because they were originally developed for Linux, they are easier to build and debug on Linux, and you'll find more support when things go wrong.  For trying to do almost everything well, or at least okay-ish, on the cheap, Linux is the optimal choice.

Additionally, both Microsoft and Apple make a great deal of their profit by ensuring that users don't have to think about what's going on "under the hood".  Both UIs obfuscate an incredible amount of information about the system being used.  This is fine for many usage patterns, but to get good at information security one has to begin to engage with the mechanisms by which things happen.  It's possible for Linux usage to be equally obfuscated--just look at the default Red Hat or Ubuntu install--but the path I will nudge you toward is not.  You'll have a slightly (only slightly, I promise) higher learning curve, but in exchange you'll receive useful insights to the systems you need to understand in order to practice most subspecialties[^1] of information security successfully.

**Which Linux You Choose Matters.**

Linux comes in many flavors or variants which we call "distributions" or "distros" for short.  The distro you choose will determine, in large part, which applications are available to you via automated channels vs. which you must build from source and update by hand, as well as what the default set-up is for your computer and how hard it is to maintain customizations over time.  Here is a short breakdown of some distributions to consider as an infosec newbie and why you might consider them:

**[Redhat](https://www.redhat.com), or its derivatives:**  Avoid these if this will be your first Linux distribution.  There are several "Redhat-isms" which are very different from the rest of the Linux world.  While using these systems isn't bad per se, if you don't have any context from having previously worked on other Linux distros, you will find interfacing with most types of Linux confusing if you first learn on Redhat.  Examples of Redhat derivatives are [CentOS](https://www.centos.org), [Scientific Linux](https://www.scientificlinux.org), [Fedora](https://getfedora.org), and anything that distributes packages in RPM format.

**[Devuan](https://devuan.org/) or [Xubuntu](https://xubuntu.org):**  If one is going to start with a system that distributes packages in .deb format (which is great for package availability), these are the way to go.  Devuan is slightly more secure in a Linux-y separation-of-concerns way, but Xubuntu inherited a more polished install from its Ubuntu parentage, so it may be easier to get your first system up and running, plus you may find more community support outside the infosec community.

**[Debian](https://www.debian.org), [Ubuntu](https://www.ubuntu.com), and other Debian derivatives:**  Avoid these.  Ubuntu offers an extremely bloated and cumbersome UI aimed at extremely non-technical users, and is less tolerant to major UI changes than Xubuntu.  Meanwhile, Xubuntu gives you access to all of the software from the Ubuntu repos and benefits from the Ubuntu packaging and security teams' efforts.  Debian has suffered major brain drain thanks to multiple forks, and no longer keeps up well enough to be a reasonable infosec platform for an inexperienced newbie.

**[Slackware](http://www.slackware.com):** The oldest living Linux distro, Slackware gives you the best view of what Linux software behaves like "by default" as the maintainers are almost religiously opposed to customizing software for distribution apart from extremely well-commented example configs.  Slackware has a small but active support community, but they are generally intolerant of newbies who are unwilling to do their own legwork.  Read [How To Ask Questions the Smart Way](http://catb.org/~esr/faqs/smart-questions.html) before seeking help.  Also, expect package availability to be less comprehensive than .deb based systems.

**[Gentoo](https://www.gentoo.org):**  This is a source-based distro that I rarely recommend to newbies.  However, it's what I run on my workstations and I've recently had a couple of new mentees pick it up as their first distro and run with it.  Package availability is great, and packages are easy to write when you need to roll your own.  **Gentoo has a massive learning curve**, and is *not* quick to get running, as you'll be configuring and building most of the system from scratch.  In exchange, you get an incredible amount of control and unparallelled ease among Linux distros in maintaining any array of customizations.  You also get an intimate view of all the moving parts in an operating system.

**[Kali](https://www.kali.org):**  Many infosec newbs install Kali Linux as their first distro because it is so often used in infosec workshops.  Please don't hamstring yourself like this!  Kali is optimized to run well from LiveCD or LiveUSB, and doesn't make a great daily driver.  This distro exists to solve the problem of getting a uniform system across a workshop or class very quickly, but it falls short once you try to maintain a system over the long term or customize it too far.  Kali is Debian-based, so you can get the good points (including the full range of tools available with Kali) without the drawbacks in a Devuan or Xubuntu install.

**[Arch Linux](https://www.archlinux.org/):**  I've got mixed feelings on this one.  Arch tries to remain fairly lightweight, and stay at the bleeding edge despite the overhead of being a binary distribution.  This can leave you with some risks around instability, bad packages, and incompatibilities with other things you want to run.  On the other hand, I know folks who love Arch and the support community is exceedingly active.  Adopt with care.

**If this entire section has left you intimidated and confused, install Xubuntu.  You'll feel better soon, I promise.**

## The OS Install

h


[^1]: "Most" is not a typo here.  There are definitely areas of information security practice that require very little technical knowledge.  For example, one of the best infosec practitioners I work with comes in from a legal background, and specializes in the law and policy aspects of keeping information systems and data secure.

