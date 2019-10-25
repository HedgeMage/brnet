+++
title = "Intro to IRC"
author = "Susan Sons"
date = "2017-01-02T18:33:31-04:00"
draft = false
slug = ["irc"]
+++


*N.B., this guide is specifically for new and future hackers interested in finding community via IRC. Not all advice applies if you are only interested in non-hacker communities such as Nerdfitness or gamer stuff.*

## What is IRC?

IRC, or *Internet Relay Chat*,  has been the place to get hacking of the network and software engineering kinds done since the 1980s, with information security soon on its heels. It remains so, because:

- IRC makes it equally easy to chat with someone down the hall and someone miles away.

- IRC chatter can easily be logged and searched to find that thing you forgot.

- IRC clients come in many shapes and sizes, so it’s generally easy to find one that fits your workflow well, and is accessible to you regardless of operating system or disability.[^1]

- IRC lets live conversations happen as easily as it lets messages sit around for later, so it bends to your schedule instead of the other way around.

## Choosing a client

HexChat is a popular GUI client available for Windows[^2], Mac OSX, Linux and UNIX.  It is easy to use, and has most of the popular networks preconfigured.  On Linux or UNIX you should get it from your package manager if possible. Mac OSX and Windows users should download from http://hexchat.github.io/downloads.html.

weechat and irssi are popular text-mode clients available for Linux, Mac, and UNIX. Both require considerably more configuration than Hexchat or Xchat to get started, and have more of a learning curve in general. However, the payoff is a very clean text-mode chat experience that is extremely configurable and handles complex filters, dozens of channels across multiple networks, and custom behaviors very very well. If you have a preference to avoid ncurses, irssi may suit you better, but in all other cases I’d recommend trying weechat first, as it is more actively developed and slightly easier to ramp up on than irssi.

There are at least a hundred other clients out there – clients that live inside Emacs, clients that run on your phone, clients that integrate with your email client, XMPP (Jabber) client, and more – just look around.

## IRC basics

### Networks

There are two IRC networks that you probably care about if you are just starting out: [OFTC](http://www.oftc.net/) and [freenode](http://freenode.net/). Both of these networks are preconfigured in Hexchat, so you need merely select them and give yourself a nickname.  If you’re trying to configure something else, see the networks’ respective home pages for connection details.

Freenode is the network where the bulk of open source projects host their development, support, and social channels.

OFTC is a spinoff of freenode, with a small but significant number of open source channels, plus a number of privacy and security channels.

Each of the clients I mentioned is capable of simultaneously connecting to both (or more!) networks so that you may enjoy channels on each.

### Nicknames

You’ll find me on both freenode and OFTC as "HedgeMage" when on my personal machines or "HedgeWork" from a work machine. The separation is arbitrary, it’s just a result of how I manage my bouncer accounts.

You should find a unique, unregistered nickname and register it so others can get to know you.  While some people use their initials or some form of their legal name as an IRC nick, this is by no means required. Nicknames that are easy to remember are preferred, and this often leads to seemingly outlandish ones. Being HedgeMage certainly doesn’t keep me from being taken seriously. Similarly, bonsaikitten, Isky, micrypt, and CaptainPlatypus are all quite serious individuals whom you should probably get to know at some point.

In order to “own” a nickname on an IRC network, you must register with nickserv. This has the advantage both of reserving that nickname for your use only, and of giving channel owners the ability to give you invitations to invite-only channels, chanop (channel operator) privileges, or other special permissions if they so choose.

Registration is simple. Do `/query nickserv info foo`, where “foo” is a nickname that interests you, until you find something that you like which has not been registered by someone else. Then do `/nick foo` to change your nickname to “foo”. `/query nickserv help register` will provide you with registration instructions.

Authentication in IRC is often referred to as “identifying to nickserv”, because it’s an apt description of the usual command (where “MYPASSWORD” is the password set during registration):

    /msg nickserv identify MYPASSWORD
If you get sick of typing that every time you connect, before joining any private channels, you can tell your client to identify for you on connection. The mechanism varies, but if you can’t find specifics in your client’s documentation, feel free to ask for help via your client's IRC channel.

### Channels

There are channels out there for nearly every interest.  Since most of my readers are focused on open source software development or information security, I'll suggest a few in this arena:

#### On OFTC:

- `#grokmenot` is a beginner-friendly channel for current and future infosec professionals.

#### On Freenode:

- `#icei` belongs to my nonprofit org, the [Internet Civil Engineering Institute](https://icei.org).  Stop by, and help us save the internet.
- `#friendly-coders` is a good place to ask questions about programming in any language.
- Most programming languages have their own channels on freenode: e.g. `#python`
- `#startups` is for founders and employees of early-stage startups, and others interested in what is happening in startup-land.
- The best places to start are usually support and development channels for software you use and are interested in.

#### Other Networks:

Mozilla has their own network, plus there are some older networks like DALnet and EFnet out there.  Feel free to explore, but before you do, read on to understand IRC culture a bit so that you make friends instead of enemies.

### IRC social memes

Like any other community, IRC networks have their own social standards. For the most part, you’ll pick these up as you go, but there are a few points worthy of special attention:

On freenode, it is considered stalkerish to pm (private message) someone without their express permission. Other networks don’t care that much, but when in doubt ask before pm’ing.

It is 100% normal and expected IRC behavior to “idle” in channels, or leave a client connected to a channel in which one is not active. This lets users peek in between other tasks and become active if something interests them, see what they missed while gone, or just plain not create a bunch of join/part messages by entering/leaving frequently. It’s often useful to idle in a channel for a while when one first joins to get an idea of how people there interact.  Every channel has a social code of their own.

Almost every IRC client will “hilight” lines that contain the user’s IRC nick. This is a useful way to help others follow a conversation when other conversations are happening in the same channel. So, if I’m supposed to notice something in a busy channel, you probably want to preface it with `HedgeWork:`. It’s not very nice to gratuitously hilight someone who is obviously idle or away, as that would leave them with a huge backlog of notifications to return to.

Almost every IRC client offers tab-completion of nicknames. This is really useful when trying to hilight someone or send a pm.

Before trying to get help in a support channel, please read [How To Ask Questions the Smart Way](http://catb.org/~esr/faqs/smart-questions.html) and [The Anatomy and Habits Of the Common Support Leech](http://binary-redneck.net/2010/06/23/support-leech). Everyone reading this is likely smart enough that if we need support, it’s going to be from someone bright and skilled enough that they are likely to also be curmudgeonly about IRC behavior.

Know where you are before you talk about working in or being interested in security. IRC has good neighborhoods and bad. On EFnet, for example, or in #defocus on freenode, stating that you’re in the security field has about a 1-in–5 chance of making some teenage twit with a botnet very interested in you.

### Commands

IRC has a lot of commands. Standard commands, commands specific to the IRCd or services daemons running, commands specific to the client used or commands custom-configured by the user. Here are a few very basic, very universal ones that you may find useful.

`/join` and `/part`

This is how you join and leave channels. `/join #foo` will let you join the foo channel, and `/part` while focused on that channel will cause you to leave.

`/topic`

You should always issue the `/topic` command upon entering a channel you haven’t been to before to find out what it’s about or if there are any channel rules they want newbies to be aware of. Many clients also display the channel topic somewhere above where the channel’s traffic is displayed.

`/query` and `/msg`

The `/query` and `/msg` commands allow you to send a private[^3] message, or pm, to another user. In some clients, these behave identically. In other clients, `/query` will start the private conversation in a separate window or buffer but `/msg` will not.

Example:

    /query HedgeWork Hey, are you going to be posting your Penguicon slides any
time soon?

`/me`

The `/me` command is used to sort of narrate yourself, for example, if I type /me fires her Nerf gun in Craig's direction., others will see:

    * HedgeMage fires her Nerf gun in Craig's direction.

`/away`

The `/away` command is used to set a status message so people know you are not paying attention to IRC. The syntax is `/away At lunch, back around 1pm.`. To unset your away, just use `/away` with no message or arguments.

N.B. to weechat users: weechat defaults to only applying away commands to the network currently focused. To set or unset your status on all currently connected networks in weechat, use `/aaway` instead.

Some clients will set you away automatically after you have been idle for some time, and remove it when you next type something in the client. This can be very helpful.

Some clients will announce to every channel you are in and every person you’ve recently pm’ed that you are going away, and when you return. This is obnoxious, and should be turned off.

`/names`

The `/names` command will display a list of the nicks currently joined to the current channel. This is superfluous in Hexchat, Xchat, and weechat – all of which present a nicklist next to the traffic for each buffer – but irssi users may find themselves using `/names` more often.

`/whois`

`/whois` allows you to get some basic information about a user. The exact information presented varies from server to server, but their nick, hostmask, real name (if set), and idle time are typically included. The syntax is `/whois HedgeWork` to get info on the user HedgeWork.

`nickserv` and `chanserv`

Nickserv and chanserv exist to register and manage nicknames (nickserv) and channels (chanserv). Both are well-documented on the server (and their usage can differ from network to network depending on which server daemons are being used). You can `/msg` or `/query` either to get a list of commands and additional documentation, e.g. `/query nickserv help` or `/query chanserv help`.

### Things to avoid

The following are either insecure, obnoxious, or outmoded, and should not generally be used:

Anything containing “DCC” or “CTCP” other than the CTCP “version” and “ping” commands (and those only if you really must).

`/notice`

Any command that sends coloration to the channel (though many clients and channels now strip colors, blinking, and other weird text effects).

Pasting more than 2–3 lines at a time to a channel. Instead, use a [pastebin](http://pastebin.com/) and give the channel a link to your paste.

### Advanced (Optional)

#### SSL

Many IRC servers are capable of SSL-encrypting client<->server connections and/or accepting client auth via SSL certificate. The specfics vary per network, but if you are interested you can look up connection info on the network’s web page. I’m currently less than impressed with this capability as almost every client available uses GnuTLS to handle SSL. Hopefully, that will be phased out soon.

#### Screen and tmux vs. bouncers

Often, it is useful to maintain a connection to IRC even when your computer isn’t on or isn’t connected. This can allow you to read backscroll of conversations you missed, get messages from folks, or just reboot without annoying anybody with needless join and part notices.

Some people accomplish that ongoing connection by running a command-line IRC client on a server or other high-uptime machine inside a screen or tmux session that they attach to from their workstation or laptop. Others, like me, prefer to run an IRC bouncer.

A bouncer is a daemon that runs on a server, but connects to your various IRC networks like a client. Then, you connect your local client to the bouncer as if it were the IRC server. The bouncer is always connected, so nobody sees your client disconnects, and traffic you missed is sent to your client when you reconnect to the bouncer.

Pros:

- You don’t have to miss what happens when you log off.
- You won’t annoy anyone if your connection is flaky.
- A bouncer can be configured to remember the channels you join or leave, so that you don’t have to manually maintain your autojoin list.
- The IRC networks you connect to will see your bouncer instead of your local machine.

Cons:

- It’s another thing to maintain.
- The IRC networks you connect to will see your bouncer instead of your local machine.

If you feel like trying a bouncer, I highly recommend [ZNC](http://wiki.znc.in/ZNC).

------

[^1]: This is my biggest beef with "modern" alternatives such as Slack: they fall down on both support across operating systems and support for the blind, and break hackers' workflows by requiring separate tabs, identities, or clients for each project one interacts with.

[^2]: Some people will hear you are on Windows and recommend a client called mIRC. **DO NOT** use mIRC. In addition to the fact that it has security issues and violates the IRC spec in ways that create extra work for network staff, mIRC is a favorite of script kiddies, and that’s really not the message you want to send about yourself.

[^3]: For some value of “private”. Pm’s are not broadcast to the channel like regular messages, but they aren’t encrypted, either. Some clients are capable of using OTR or GPG to perform end-to-end encryption for private messages, but the implementations are hellishly buggy.
