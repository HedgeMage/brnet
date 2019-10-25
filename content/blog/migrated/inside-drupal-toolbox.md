+++
author = "Susan Sons"
categories = ["drupal", "OSS", "tools"]
date = 2010-04-21T05:00:00Z
description = ""
draft = false
slug = "inside-drupal-toolbox"
tags = ["drupal", "OSS", "tools"]
title = "Inside the Drupal toolbox."

+++

Today's BoF for new Drupal contributors went better than I could have hoped. I've seen three of the participants in the issue queue already! One thing that came up at the BoF session was taht new contributors aren't always sure how to set up their dev environment and choose tools that will make playing in the issue queue easier

*chx*\* nano, komodo, bzr, kubuntu  
*chx*\* lots and lots of good music is very important to get you in the groove (see my blog post on flow)  
*wonder95*\* MAc Book Pro, AMP setup using MacPorts, Komodo IDE with xdebug and FF Xdebug Helper extensions, prefer Git  
*jcfiala*\* komodo, mercurial. Either wamp or virtualbox to work in ubuntu.  
*sepeck*\* notepad++  
*joshuarogers*\* Geany  
*scyrma*\* debian, vim (and cgvg package), xdebug .. local lamp stack.  
*merlinofchaos*\* all my servers are CentOS 5 servers running apache/php etc. I use EditPlus as my editor and samba so that I can use my windows tools on the files. Most other stuff I do via putty to ssh to the linux server.  
*webchick*\* I use vim for most hacking, then Komodo when I need to deal with, like, Form API or node access. CVS for Drupal.org, Subversion for personal projects (probably eventually Git), Mac OSX, Skitch for visual patch reviews  
*mikey_p*\* XDEBUG  
*dmitrig01*\* oh yeah I use skitch a lot  
*webchick*\* XDEBUG!  
*ksenzee*\* Ubuntu, NetBeans, xdebug  
*cwgordon7*\* I run windows xp with wampserver set up. I have xdebug there which helps. I sometimes use eclipse, but mostly I use notepad++ for more lightweight code editing  

I run a LAMP stack on my local machine, do my revision control with git, edit in nano or gedit, and do my diffing, patching, etc on the command line. I use irssi to keep up on Drupal IRC. If I'm looking at a very large or complex diff that's hard to follow in the terminal (command line interface), I throw it in meld.

I have a couple of little configuration items that help my work go a little smoother. For example, I use my /etc/hosts file to direct traffic for example.com to my localhost (and configure example.com in apache). It makes my dev environment look a little friendlier, and when taking screenshots or doing a demo on my laptop, I'm already showing a nice standards-compliant example.com.

The big thing is to do what works best for you. Try any or all of the combinations above, or make some of your own.

