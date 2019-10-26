+++
author = "Susan Sons"
date = 2017-12-15T22:39:00Z
description = ""
draft = false
slug = "dns-blocklists-and-fault-tolerance"
tags = ["DNS", "Quad9", "network-protocols"]
title = "DNS, Blocklists, and Fault Tolerance"

+++

My workplace hosts weekly "brown bag" discussions, wherin much of the team and various guests bring our lunches to our larger conference room, or an HTML5 videoconference bridge, and discuss some information security topic over a meal.  It's an informal affair; my stuffed animals may even appear on camera in my stead if I'm under the weather as I was today.

This week's topic was the [Quad9 filtered DNS service](https://quad9.net/#/).  The [slides I used](http://slides.com/hedgemage/quad9-friend-folly) to kick off the discussion are publicly available, with some edits/additions in orange following the discussion.  They give a brief introduction to why we have DNS, Quad9's promise, and some dangers that some of my colleagues and I identified should Quad9 become the ubiquitous DNS service.  However, I wanted to capture more of the discussion than slides easily lend themselves to, so below are some of my notes.

## Notes

- Lots of questions around centralizing DNS to one provider.

    - It took 8.8.8.8 some time to sort out resilience, and they have all of Google's resources behind them.

    - The DynDNS DDoS was a huge disruption to the internet at large, and they are fairly robust.  However, this was in part because so many authoritative nameservers as well as a popular resolving name service were centralized in one place.

    - Why aren't the same concerns raised about 8.8.8.8?  Answer: because 8.8.8.8 can be used with other providers as failover sources for DNS.  In order to receive any protection from Quad9, one must only use Quad9's DNS and no failover provider.

- Main reaction to Quad9's failure modes were "well, it's better than nothing".

- Sustainability is a big concern: encouraging these sorts of system-level changes for naive end-users is dangerous if the service may evaporate.

- I was surprised that the differences in Quad9 response speed for already-cached entries vs. not-cached entries didn't bother more people.

    - I see this as an effective [hellban](https://en.wikipedia.org/w/index.php?title=Hellban&redirect=yes) on niche websites.

    - Others felt that only power users visit anything other than very mainstream websites anyway, and we understand DNS or don't expect reasonable performance from new startups and small operations.

- The transparency issues didn't seem important to most of the group.  I did feel better once I was told that there was, in fact, a search mechanism to find out if one had been banned (but not why) and request removal.  I missed it the first time due to an overzealous blocking mechanism in my browser that thought it was malicious, ironically.  I, personally, would want to know a lot more about how Quad9 determined a site to be a malware source, malware command and control, or other bad actor, before recommending it.  They have promised no content-based censorship, however, there are many grey areas here (such as sites doing legitimate malware research or discussing the topic of malware, IRC networks which inevitably see botnet activity from time to time) which they may not have considered.

- One person did point out that it's an open question as to where Quad9's operators would have learned how to responsibly operate a blocklist.  The three rules I laid out in my slides are widely accepted and easy to learn, but I can't say they are published anywhere in a traditional sense.  Blocklist operation, because of the risks involved, has always been a niche activity and a bit of black magic as viewed from the outside.  You'd have to engage with a blocklist operator's group, NANOG, or have experience consuming DNSBLs in some context to know what to do.  I don't think this is too much to ask, but others felt it sounded too much like "join our secret cabal or else!" and I get how it can seem that way from the outside.

- I learned that some end-user security suites typically run by Windows users already attempt egress filtering to cut down on malware issues.

## My thoughts afterward

- I wish I'd done a better job explaining the failover issue.  I'd made a point of explaining how and why failover is not possible with Quad9, but perhaps people aren't aware that normal operation is that DNS fails over if your server doesn't give you a useful response: that is, when the first one doesn't work, it tries another, then another.  We seemed to go in circles where people kept asking me why I thought Quad9 was categorically more likely to have outages than any other DNS provider, when that wasn't my issue at all.  My issue was that with any other DNS provider, an outage is handled by a failover service.  With Quad9, an outage is an outage.

- I'm still concerned about the lack of transparency on Quad9's part, but I feel that I've been too harsh on them in this regard.  They've made some effort to give people hope that de-listing can work, and it's possible that no one ever introduced them to DNSBL best practices.

- The discussion we had ended up being pretty slanted, because it was inspired by an email thread about a post (brown bags are often us going off on tangents after things like that) in which someone suggested that we advise people and organizations very broadly to use Quad9 as their DNS resolver.  Many of the centralization issues are mitigated if it becomes just one-of-many providers, and especially if organizations with central IT managing their DNS use an unfiltered provider combined with egress filtering instead.

- The question came up as people were leaving that if we've been having an argument about whether it's a good idea for *everyone* to move to Quad9, would a saner question be (paraphrasing) "if we presume that DNS is a good place to filter some malicious activity, what solutions are best for what use cases?"

    - This is a much better question!

    - I feel like we could put together some sort of checklist for this:  

        - If you are a nontechnical user who tends to stick to the mainstream internet *and* you aren't in an organization with centralized IT management, *and* you can tolerate rare multi-hour internet outages, Quad9 would be a good match for you.

        - If you are inside an organization with centralized IT management, they should be doing egress filtering on your behalf.

        - If you are on your own, but non-technical, and just can't tolerate potential outages or not being able to get to sites that were erroneously or overzealously blocked, then depending on your tolerance for failure modes vs. setting up your own router, you might choose between a newer SOHO router with egress filtering that's managed for you and an antivirus suite that includes client-side egress filtering.  The latter may be preferable if you are on a laptop and use a lot of public networks.

        - If you fall into the maybe up to 1% of people who are journalists or journalist cohorts, who are technical researchers (especially in areas around information security), have extremely high uptime needs, or have especially censorship-sensitive usage patterns... then you may just have to pick up some technical expertise, because there isn't a set-it-and-forget-it option at that point.

     - The above is just me riffing off the top of my head, though...there are very likely bits that I haven't thought of in these few minutes.

     - I'd also like to ask how heavily we should rely on DNS blocklisting as malware protection.  It is a very circumventable defense, so while it can be one line of defense, I'm wary of getting too excited about it.  I wonder if the success and usefulness of DNSBLs for e.g. spam mitigation have led to overconfidence in how well they can work for something as general as disrupting malware across the board.

I love our brown bags because it's a casual chance to toss ideas around and hash them out.  Malware is an interesting subject in general because it so often targets our end users, whom we should be here to protect, but who end up in a position of being blamed for something that is way out of scope for their level of knowledge and responsibility.  That's something I'm glad to say we *did not* have in this conversation at all.

