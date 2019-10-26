+++
author = "Susan Sons"
date = 2017-06-27T14:23:50Z
description = ""
draft = true
slug = "care-and-feeding-of-data"
title = "On the Care and Feeding of Research Data"

+++

I just finished taking a survey titled "State of Open Data 2017", which seems primarily targeted at academic researchers and their administration.  There was a question about how I fund data curation that was a bit odd from my perspective.  The choices were something like "funding source, data curation built in to the grant", "funding source, general funds", "institution", "my own funds", or "not funded at all".

It is not multiple-select, and didn't offer an option to state that some of my data curation is essentially no-cost.  Having worked for years with biologists, physicists, geologists, and so on, I'm well aware that data curation seems very burdensome to many of them...to the point that many can't actually come up with the data set that they used to produce research if asked two years after publication.  It's sad and scary that not only can so much knowledge easily be lost, but that it is VERY hard to seriously investigate a study's data and methodology after the fact.

I mention this, because I think that it's something information security research often does right, from which other disciplines could learn.  For context, I work in applied research[^1] in the information security field.  While my research center, [CACR](https://cacr.iu.edu) is attached to Indiana University, we've got some cultural benefits that many research centers don't.  Specifically:

* As an information security (or cybersecurity, if you prefer) researcher, my discipline has its roots in computer technology.  About 80% of my team has some sort of heavy technological background in systems administration, programming, mathematical analysis, networking, or similar.  We have a deep bench with the skills needed to do what we need to do in-house.

* As an *applied* research center, we work very close to the ground.  In other words: we don't live and work in an isolated lab environment, our work is out in the world, on production systems, where interoperability, maintainability, integrity checking, affordability, and fault tolerance don't just matter, but dictate most of our decisions.

* Some of us are closely tied in to the open source software world, where our culture is defined by the sharing and collaborative building of common tools.

Why is this important?  It's important because, thanks to our technologies and data practices, I'd say that fewer than 5% of my projects[^2] require a nontrivial amount of skilled human labor for data curation.  In other words, more than 95% of the time, I get my data curation practically for free.  The low cost of data curation for my purposes makes me more likely to release my data, and certain that my releases of data will be in a format that others can easily use.

If this were true for more disciplines, we might see increased data sharing in general, and better access to data about research we are relying on for decision-making purposes, both individually and as a society.  It's hard to do something across all of science when it is expensive, difficult, and not culturally accepted as an absolute requirement of doing the research.  Like information security, data curation and sharing is often seen by basic researchers not as enabling science, but as competing for resources that should be directed toward doing science.

### Data curation end-goal:

Conversations like this are common in my life.  I want them to become common for other researchers as well.

> Colleague: Susan, I was looking at your doc from two years ago on repository activity, branching models, and software quality.  I'm wondering if I can get hold of the data you used to come to these conclusions.
>  
> Me: Wow, that was a while back, give me a second...<ten minutes of furious grepping>...okay, I just emailed you a link to the blog post I wrote about the project.  It's a bit more technical and informal than the paper.  From there, you'll find links to:
>  
> * the repo containing the custom scripts I wrote for the project.  It's important that you look at README.md for usage instructions.
> * a tarball of any config files that are NOT part of the scripts but related to this specific data set, as well as checksums for files generated if you use these with the scripts above: this is useful if you want to test your install before using the tools on new data
> * a tarball with all of the original repository dumps I used: if you use these with the other stuff above, you should be able to easily reproduce my results.  However, if you are doing new work, you probably want to pull from the repos (there's a spec file in the config tarball listing them) to get commits that happened since my project ended. Warning: this is large, on the order of many TB.
> * a tarball containing a dump of the final database I ended up with after processing all of the data... this is only a few GB.
>  
> If you use this for anything cool, please let me know!

If you're in the basic research world, this sounds like it was probably very labor-intensive to put together.  However, in my world, the reason that it's a blog post is that I did it quickly and informally.

* I was maintaining the tools in a git repo anyway, so that I could easily roll back mistakes or experiment with different methods without losing my mind.  Publishing that was a matter of a simple "git push".
* Tarring[^4] up my config files is a one-command operation (they were just sitting there in a directory), and they are small enough to post anywhere.
* Tarring up the repo dumps was also one command, but it probably ran overnight due to the size of the data set.  Indiana University provides me with places to host big globs of data like this, but if they didn't, I'd have to find some cheap storage.  Luckily, because it's public rather than sensitive data, I have myriad free or cheap choices.
* I make regular database dumps as a function of my back-up routine, and before cleaning a finished work's work-in-progress files from my working systems.  Tarring one up and sticking it on my blog is a five-minute operation.
* I probably spent an hour or so writing the blog post: instead of being laden with references and stringent formatting requirements like an academic paper, I hammer out blog posts in Markdown so that I can focus on the content.  I expect my data and process to speak for themselves, so I don't need appeals to authority: I only include the references that are needed in order to understand the post.

## Nearly-free data curation is achievable in most disciplines.

There are a few necessary preconditions for this to happen:

### 1. Widely-accepted, formally defined standards for formatting data.

#### Case in point: PCAP
[PCAP](https://en.wikipedia.org/wiki/Pcap) files are how we--meaning, almost everyone in the world--store, process, and exchange raw network dumps.  It's a pervasive standard used everywhere TCIP/IP based networks are used.  It is independent of the language or other characteristics of the data being passed around: PCAP is completely content-agnostic.  It just records raw network traffic in a way that makes it easy and predictable to parse out important metadata from the TCP, IP, UDP, and ARP protocols.

The PCAP format has remained almost unchanged since its advent back in the 1990s, and conversion scripts to move older PCAPs into an up-to-date format do exist in case one needs to work with decades-old packet captures.

This is but one example among many.  Generally speaking, we capture and use data in the same formats we would use to share it.  As a matter of fact, we also have standards for how to handle data for which there isn't a standard!

### 2. Automation should be the rule, not the exception.

In most of the basic sciences, there are one or more points in the data curation where a research assistant is hand-copying something.  Physics seems to be successfully diverging from that, but it's still the way it's done in chemistry, geology, psychology, and so on.

This is not completely avoidable: I can't set up a sensor net to understand, characterize, and record human or animal behavior the same way that I can for environmental observation (temperature, humidity, light levels, wind speed, etc.) or network traffic.  However, there are many places where increased automation would not just be possible, but cheap and beneficial:

* A number of scientific instruments still produce PDF reports when they could have given a far more useful data dump in something like sqlite that is lightweight, easy to support, and easy to process with automated tools.  Researchers should look into instruments' data format capabilities before making purchases.

* Many researchers insist on entering data into Word document or similar, which doesn't age well and is hard to process in an automated way.  Spreadsheet programs are marginally better, in that they can usually export to something like CSV or sqlite, but researchers must be trained to do this rather than saving data in the spreadsheet program's native format, which tends to be messy and not very portable, for the sake of emphasizing text formatting over data processing.  It would be hugely beneficial to teach researchers and their staff how to use more powerful, interoperable, and portable data formats.

* Many researchers write their own software, or have their student assistants write it, without coming together as a community to collaborate on common tools and APIs.  They also tend not to put their software under source control of any kind.  The result of this is that it's hard to know how data was stored and processed if trying to circle back to research a couple of years (or even months) after publication.  Additionally, when something is hard to automate for someone for whom programming is not their primary discipline, researchers often revert to "make a grad student cut-and-paste or manually copy this", which are error-prone, non-auditable steps that usually don't get properly recorded.  There are no standards or too many standards for most types of data.  This is starting to improve with the popularity of R[^3], but it still has a long way to go.

**Any copying, let alone transforming, of data by hand is a threat to data integrity**, because humans make mistakes, especially on large data sets, and while I can reference a piece of code to see what it did (and possibly did wrong) when transforming data, I cannot do so with human data copying and/or transformation.

In order to enable automation of data handling, researchers need automation-friendly data formats, 



----
[^1]: "Applied research", as opposed to "basic research" is the middle world between carefully controlled research labs cut off from real-world practice and the insanity that is what happens in the wild where people practice some discipline every day and have to deal with externalities such as budgets, myriad social pressures, personnel turnover, commercial availability of tools and products, market trends, and so on.  In other words, we  

[^2]: Rough guesstimate of the aggregate of my projects in various venues, not just CACR projects.

[^3]: Interestingly, R didn't fix this by having any data formatting or processing capabilities that previous languages and tools didn't.  R fixed this by putting a tool in the hands of researchers that ties data visualization to how the data is stored and processed.  Researchers' desire to have appealing visualizations for publication has inadvertently led them to store and process data more responsibly.

[^4]: A tarball is a compressed archive of a filesystem heirarchy, kind of like a .zip file, but with more options with regard to compression types.  It is commonly used on Linux and UNIX systems, but can work on other OSes as well.  "Tarring" something up is to store it in a tarball.

