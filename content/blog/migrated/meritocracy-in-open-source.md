+++
author = "Susan Sons"
categories = ["OSS", "meritocracy", "community"]
date = 2017-05-11T22:26:00Z
description = ""
draft = false
slug = "meritocracy-in-open-source"
tags = ["OSS", "meritocracy", "community"]
title = "Meritocracy in Open Source"

+++

I sat it on a great talk at [OSCON](https://conferences.oreilly.com/oscon/oscon-tx) today by [VM Brasseur](https://twitter.com/@vmbrasseur) about succession planning in Open Source projects and communities.  There was a point where she called out the weaknesses in claims of meritocracy in open source projects: At first, I expected the worst: another tirade about putting the goal of selecting contributors who look different from one another ahead of selecting for competence, differences in thinking, or complementary skill sets.  What I actually got was something very different: a real assessment of where attempts at meritocracy usually fall apart.

Specifically:

* The "I know it when I see it" failure mode: no one defines what merits a project or role needs, leaving new contributors flailing to figure out how to fit in, and established contributors blind to how to select and encourage others to eventually succeed their roles. (Fun fact: this blindness usually leads to a high attrition rate among new contributors and selection that corresponds more to individual biases than what the project needs.)

* The "the role is the person" failure mode...succession planning is put off again and again until it never happens, because project leadership never look at what the key roles are that they need to fill, being stuck in the "so-and-so does this" mode of thinking.

* The "I'm waiting for someone competent to show up" failure mode.  I've renamed this from the presentation, to reflect a bias I see in senior contributors time and again.  Rather than *building* competence in new contributors, some senior contributors wait for it to magically appear.  This doesn't actually happen.

There were others, but the list went by quickly.  I was very happy to see that my projects--those I run, at least--have carefully dodged these failure modes, at least for the projects in which I was in a leadership position.  I've always pushed hard on mentoring, on defining roles, and on defining what meritocracy means in the context of my projects and for those who want mentorship from me.

However, while I've passed this on time and time again, I'm not sure I've written it down somewhere linkable and searchable.  So, here it is:

## Show up, be polite, do work.

It's a pretty simple, yet it's surprisingly often the last thing on new contributors minds when they show up to an open source project I run.  There's often a fear among new contributors that they don't have enough technical skill and experience (if you're a good worker, we'll help you build it), or that they don't understand the problem well enough (we'll point you at things to work on).  Worse, some come in with the idea that the project should invest in them on the promise of maybe doing work later.

Let's talk a bit about how and why this works in practice in my projects.

### The importance of showing up.

Most open source projects suck at recruiting and mentoring.  These are learned skills, which too few OSS leaders get any training in.  Even projects that have skill in recruiting and mentoring have limited resources.  It is crucial that these projects spend their resources wisely.  One of the most important things you can do to demonstrate your worth in the context of my projects is to be reliable in showing up.  This means:

1. Make the time you spend on the project predictable: your colleagues should know when to expect to see you again, and if you get too busy for something, you should communicate to the team instead of going silent.
2. Make sure to cleanly hand off any responsibilities you can't carry out on your own, so that they don't get dropped.
3. Make good use of the project's communication channels, so that others know what you are working on and you know what's happening on the project.
4. If you take on a critical role, such as lead developer, a component owner, information security officer, or such you should make it easy for project members to contact you in an emergency, even if you are offline.

Showing up means that the project knows it will get back its investment in mentoring you, it means that you won't randomly become a blocker on progress being made, and and it means that you are generally respectful of others' time and the need to be reliable to advance from drive-by contributor to more senior roles.

### On being polite...

Projects are made up of people.  A toxic social environment can and will kill a project's ability to forward technical goals.  Unfortunately, some projects' response to the real threat of toxic social environments is to create a *more* toxic environment, by defining correct behavior as behavior that doesn't bother anyone (i.e. "the most aggrieved person wins").  This simply predisposes insecure people to take offense more often, because it's an easy power grab that needn't be backed up with facts, offensiveness being a subjective matter.

Taking offense will get you nothing on my projects.  As a matter of fact, part of our social code is to **be generous in the inputs we accept, and careful in the outputs we produce.**  Mistakes and miscommunication happen; and this precept helps to minimize them.

Another piece of our definition of politeness is to **assume right intent until absolutely proven otherwise**.  Mistakes come in many forms, but assuming ill intent can quickly escalate a mistake to a disruptive community schism.  In any case, most people mean well most of the time.  Acting on this assumption tends to bring out the best in people.

We **limit our areas of concern to behavior within the confines of the project**.  We accept contributors from many cultures and walks of life.  To truly do this, they must be free to have whatever personal life they want, while responsible enough to behave with a certain level of pro-hackerism in project venues and when speaking for the project elsewhere.

The above guidelines are mostly concerned with preventing the wrong kinds of conflict, and avoiding escalation of conflict, within the project.  We also have expectations for managing constructive conflict, and for a few other matters of concern.

**Responsibility is considered greater with more-senior contributors.**  As individuals rise to more senior roles, they get coaching on social and leadership skills.

We do our best to **avoid, when possible, and otherwise clearly disclose potential conflicts of interest or appearances thereof**.

When arguments arise, as is inevitable, it is expected that **all parties confine the discussion to the technical merits of an issue**, leaving aside any commentary about the parties as individuals, especially avoiding any ad hominems or characterizations of others' motives.  It is also expected that, once the issue is closed (if necessary by a decree of the appropriate project lead), the issue is dropped from debate.  Questions about the origin of the decision are then referred back to issue queue or mailing list logs rather than a re-hashing of the debate.  To enable this, we try to summarize various sides of an issue when the final decision is made including, if possible, a statement of the conditions under which this may be revisited.

When it comes to social or process issues, there is a general preference for **enabling efficient and effective technical work** over other concerns.  This is especially important where opportunities for fault tolerance exist.  That is, we expect humans to make mistakes with some frequency and thus design our processes to offer some safety net for that.

We endeavor to **make role definitions and succession planning** explicit rather than implicit wherever possible.  Oftentimes, power games within a project arise because there isn't a clear definition of boundaries of authority.

We accept that usually, **a sub-optimal decision executed now, and executed consistently, is better than a taxing, long-running process or a breakdown in the conceptual integrity of a code base or document**.  That is, don't let the perfect, or a search for consensus, get in the way of work being done.  In the end, a project or component "owner" is justified in making an arbitrary decision as well as they can when a debate is dragging on to the point of repetition.

We expect all project members to generally treat one another as colleagues (and, occasionally, friendly competitors) rather than as combatants.  This includes an expectation that feedback will be given soon and often, rather than expecting others to intuit boundaries and social standards that should have been communicated.

### It's all about the work.

Each of my projects is arranged around a mission.  Furtherance of that mission is our primary objective.  This is very important, because "does this further the mission?" is a great check when making decisions.  It takes a lot of ego out of things, and also gives us a way to bring people together: it's about the mission, not about individuals identities, beliefs, demographics, or personal lives.

Doing the work well means maintaining the the product (usually, but not always, code and documentation) quality standards of the project, following our process, and being honest with project colleagues about the project (including saying "I don't know" rather than trying to cover with a guess and possibly leading others astray).  It means finding a niche and fitting in to it.  It means taking direction or giving direction well, when appropriate.

Generally, I've found that once the project mission is clear, and security/coding/documentation standards are made explicit, the rest straightforward enough to give junior and mid-level contributors the guidance they need to function within the project.  Being a senior contributor or lead is, by nature, different: these people need the maturity to *set* the standards, and to ask the tough questions.  Balancing that takes experience, ethics, and skill, none of which will come from a set of project guidelines and thus are out of scope here.

## Is it really this simple?

It's certainly *straightforward* to run and participate in a project with this standard, but it is by no means *simple*.  It's actually a lot more work than the "Code of Conduct" guided projects are, but in my opinion the effort is worth it.

### Communication is a responsibility.

In projects run according to my meritocratic rule set, we accept that people won't know what is expected of them unless it is communicated.  This is part of assuming good intent until proven otherwise.  By nature, it confers a responsibility upon senior contributors and long-time community members: the responsibility to constantly and consistently communicate expectations to others.  There's no "you should have found, read, and interpreted my document as well as the mental states of other contributors" out here.

If you have a boundary, it is your responsibility to communicate it.

If you see a problem, especially involving a more-junior contributor, it is your responsibility to see that the problem is communicated to those involved, *clearly, promptly, and without escalating the situation*.

If you find that something is unclear, it is your responsibility to ask, though we understand that very inexperienced contributors may have trouble realizing what is unclear and asking, and do our best to provide active guidance before a serious problem happens.

### Leadership training is part of moving up.

Everyone moving into a senior position for the first time, and many people whose leadership or management experience is in organizations markedly different from these communities, needs coaching or mentorship in leadership skills.  It's not fair to expect someone to deal with their first cult-of-personality situation, their first underperforming subordinate, their first big decision as a component owner, and so on without the support of more experienced colleagues.  Leadership isn't about being the smartest or the most technical: it's about keeping the team moving forward toward a goal, and conducting oneself ethically.

### Everyone has something to prove.

When some people talk about being treated with respect, they mean "treat me like a person".  When others use the word respect, they mean "treat me like you are my subordinate".  We expect *everyone* on my projects to be treated like a person, with reasonable courtesy.  Beyond that, respect must be earned.

Too often, in today's society, people expect to be accorded some amount of deference merely for showing up, or for having some credential or membership in some pointless demographic.  Introducing people accustomed to such a culture to the idea that they must earn the respect of others in order to be treated as a valued colleague, let alone as an authority, can be jarring for them.  However, requiring people to prove themselves by showing up, being polite, and doing work is a *positive* for an open source project.

On my projects, we encourage people to see the chance to prove themselves in every interaction.  Be the bigger person in a conflict.  Quietly plug away at a problem no one else is attending to.  Spend your time and effort to get better at something that can help the team.  Help those less experienced than yourself.

This means both that people have to *work* to become part of our core team, but also that membership in the team *means something*.  It's worth being proud of, and each of us can trust other members of the team to show up, be polite, and do work.

### Embracing similarities among differences

This is a truly hard thing for most humans.  There's a tendency to surround oneself only with like-minded individuals.  It feels safe and productive, and doesn't tend toward high levels of disagreement.  It's also beneath the dignity of a great mind.

Like groups tend to fall to [the narcissism of small differences](http://en.wikipedia.org/wiki/Narcissism_of_small_differences), constantly narrowing the in-group by carving out outgroups in what could have been a community.  Unlike groups can have a special synergy: when group members have very different perspectives as a result of very different backgrounds, personal beliefs, and methods of operation, they tend to compensate naturally for one another's weaknesses and blind spots.

This works well if the group has a shared mission to rally around, rather than a demand to be all-inclusive (because an all-inclusive group can't *do* anything, as there's no one thing that every human wants to do and can do).  It's important that the mission is *doing* something (as progress toward a goal can be observed) rather than *being* something (as that descends into identity warfare).

A diverse group with a common mission can set aside their differences in the name of the mission, and be a better group for it.  However, it takes a culture where appeals to identity are immediately shut down and not rewarded.

### Leadership doesn't get the luxury...

* of taking things personally
* of not having patience
* of letting people who don't acculturate stick around and poison project culture
* of refraining from comment for the sake of "avoiding conflict"
* of giving feedback only for the negative events
* of not investing time and energy in non-technical leadership skills
* of benefiting from the skills of inadequately socially functional people without doing the work to insulate others from their negative impacts
* of being indispensable
* of avoiding criticism

In short, you don't get to run a community on autopilot, and you don't get to put appearances ahead of accomplishment.  You must make and take responsibility for tough and sometimes unpopular decisions.  You must give feedback early and often.  You must work on your own leadership skills and those of your team.  You must put the long-term health of the community ahead of your own personal comfort.  You must be willing to be controversial at times.

It's hard work.

## But what about biases?

All humans are biased.  No one can make perfect assessments of others: if anyone could, then hiring would be easy, at least at the companies who can afford the best hiring managers.  Trying to eliminate human bias through policy won't work, it just introduces new, harder to combat biases to the environment.

A clear process with a goal of meritocracy can be iterated upon.  Abandoning meritocracy as a concept means deciding that the OSS project's mission is not really its core mission: it is dishonest at its core.

## But what about difficult, high-performing, contributors?

An experienced, competent leader can weigh someone's contributions against the contributions lost due to that person's behavior if they are watching closely enough.  Meritocracy doesn't mean "high producers get to do whatever they want".  The health of the whole project over the long term should be taken into account.

However, going back to the assumption of good intent until proven otherwise: problem contributors are, in most cases, bearing some social dysfunction or inexperience rather than actually malicious.  Certainly, malicious actors should be ejected from a project.  Merely dysfunctional ones, if sufficiently high-producing to merit the effort, should be treated with more creativity.

Often, providing some education and support to, or buffering around, the "problem" contributor can make them a functional part of the team who isn't hampering others' performance.  Try a few different things.  Look upon the problem as a social disability, and create a plan to either resolve or mitigate it.

Most importantly, stop trying workarounds when the overhead of doing so exceeds the contributor's value to the project.  Yes, this means that not everyone gets the same treatment.  That is life: it's a project manager's job to see to the health of the project, not to make life fair.  What is the project's mission?  What is helping or hindering that mission?

