+++
author = "Susan Sons"
date = 2016-12-26T20:06:43Z
description = ""
draft = true
slug = "basic-security-for-oss-hackers"
title = "Basic Security For OSS Hackers"

+++

Here's the deal: you're an open source hacker.  You have the keys to the kingdom -- probably more than one kingdom -- and [you may not know][tankyou] which or how many kingdoms you really have keys to.  Bad guys [want the access you have][NSA-and-sysadmins].

To recap: If you're a sysadmin, compromising your systems provides an attacker with your access to every system you are responsible for, and probably a few others you interact closely with.  At least sysadmins generally know what systems they have administrative access to.  If you are an open source coder, you have *no idea* where your code is being deployed, or what lives may depend on it.

**If your information security practices suck, you are putting others at risk, period.**

I've found that too many otherwise-responsible hackers fail to put thought or effort into their personal security practices.  Some just seem set in their ways; others don't seem to think that they are attractive targets.  I suspect a large number aren't sure where to start and just keep putting the subject off for another day, never to get around to learning.

Good news!  I've done most of the work for you.  What follows is a basic guide to information security practices for the open source hacker.  This won't make you a top-notch infosec geek in a day, but adopting these practices will get you definitively out of "irresponsible bastard" territory.  *Your users trust you; don't let them down!*

----

# 0 - Introduction

I assume, if you're still reading this post, that you're convinced of the need to have reasonable security measures in place to protect not just you, but everyone who relies on a system or a piece of code you are responsible for.  Now it's time to talk about what's reasonable.

The sections below will outline specific behavioral and technologcal concerns, but since this is a technical audience, I'm going to spend a few bytes talking about theory.  Don't worry, we won't be working out a Diffie-Hellman key exchange on the back of a napkin, but I do want you to grasp the goals of security and when each is important.  That way, I can trust you to make good decisions on things not covered here.

Generally, when we talk about information security, we are talking about some subset of the following list:

* **Integrity** -- Knowing that we have a complete, intact, untampered-with copy of some data.
    
* **Secrecy** -- Keeping information out of the "wrong" hands.
    
* **Non-Repudiation** -- Proving who sent a message or command.

* **Availability** -- Keeping information or some service up and reachable for its target audience.

Given the very public nature of open source software development and related activities, it is likely that secrecy will only be important in very specific contexts, e.g. login credentials, secret keys, reports of vulnerabilities not yet patched.

Integrity and non-repudiation are much bigger concerns.  OSS works because of reputation.  Nobody I know of has the manpower to audit every piece of code that they ever run, every time it changes.  There's just too much of the stuff these days.  However, I trust that my gpsd install is rock solid because I trust Eric's and his team's coding practices and ethics. That doesn't work if Eric loses an unencrypted laptop containing a copy of the secret key he signs code with.  Under those conditions, an attacker has infinite time to brute-force his passphrase and start signing compromised copies of gpsd.  That's a pretty effective way to get malware onto the US Army's mechanized cavalry: put it in something they already know, use, and trust.  As developers, we don't always know who is running our code or where, so it is paramount that we *all* have decent security, all the time, just in case.

Availability is somewhere in between.  It's usually not the end of the world if an OSS project's web site goes down for a few hours, or someone can't reach a developer over a long weekend.  However, things can and do go insanely wrong.  I once knew a Linux distribution that had a dispute with their hosting provider...a dispute which resulted in the project losing their hosted data, most of which hadn't been backed up except in storage at that same provider. The distribution's community went a couple of days without package repos (or the
security updates the repos normally provide), and had to rebuild tons of documentation and other data from scratch.

Each time you do something new, ask yourself if data integrity, secrecy, non-repudiation, and/or availability are important and what you are doing about it.

# 1 - Device Management

## 1.1 - Full-disk encryption everywhere

## 1.2 - Never trust biometrics

## 1.3 - Physical security

### 1.3.1 - Keep an eye on your devices

### 1.3.2 - Know when to power down

### 1.3.3 - Lock your @#$% screen

# 2 - Credential Management

## 2.1 - Passphrase quality

## 2.2 - Passphrase management

## 2.3 - Seperate SSH keys per machine

## 2.4 - When to trust keys

## 2.5 - When to expire or revoke keys

# 3 - Data Management

## 3.1 - Primary storage

## 3.2 - Backup storage

## 3.3 - Access

# 4 - Network Management

## 4.1 - Firewall

## 4.2 - Segmented Network

# 5 - Code Management

## 5.1 - DVCs or die

## 5.2 - Sign your patches and releases

## 5.3 - Use static analysis tools

## 5.4 - Write tests

## 5.5 - Handle vulnerablity reports

### 5.5.1 - Be approachable

### 5.5.2 - Engage with the reporter

### 5.5.3 - Communicate securely with your team

### 5.5.4 - Fix it fast

### 5.5.5 - Regression test

### 5.5.6 - Differentiate security updates from feature or bugfix updates

### 5.5.7 - Write clear, comprehensive documentation
    
# 6 - Social Stuff

## 6.1 - Put someone in charge

## 6.2 - Have multiple, secure communication channels

## 6.3 - Seperation of concerns

## 6.4 - Least permissions possible





[tankyou]: http://esr.ibiblio.org/?p=3818

[NSA-and-sysadmins]: http://www.zdnet.com/nsa-targets-sysadmin-personal-accounts-to-exploit-networks-7000027553/

