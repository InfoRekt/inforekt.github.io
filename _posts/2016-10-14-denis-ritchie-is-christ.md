---
layout: post
title: Dennis Ritchie is Christ?
description: learn to factcheck, seriously
author: genIgnorance
src: http://www.reportsafrique.com/2016/10/dennis-ritchie-father-c-programming-language-unix-dies-70/
srcshort: http://www.reportsafrique.com
tag: reaction
rekt: 10
---
<blockquote>
Dennis Ritchie, Father Of C Programming Language And Unix, Dies At 70
</blockquote>

Wait what?


Well, thats really interesting news; considering he's been dead since <a href="https://en.wikipedia.org/wiki/Dennis_Ritchie">October 2011</a>. Obviously fact checking is only something that uncertain and insecure news sites do, right?
<p>
Considering how well they do their fact-checking, I got curious as to how their website was secured. It was obviously not using any form of HTTPS; not even on the WordPress (yes!) admin login page:
<img src="/static/img/no_https.jpg"><br>
Wondering what kind of serious news website would actually use Wordpress for their website, I gave it a good lookover and noticed something odd on top of my screen:
<img src="/static/img/push_notif.jpg">

Seriously? Why would a website like this want to enable push notifications? I have no idea.

A wpscan didn't reveal anything really serious:
<img src="/static/img/directory_listing.jpg">
<p>
Well,nothing too bad there; they do run a very recent version of Wordpress and seemed to have updated their plugins. Not as bad as it might have been. 
<p>

<h2>Tips</h2>
Being a news website they should know better:
<li>Wordpress is very popular, which also means it gets targetted a lot by hackers. You might want to switch to a more professional and comercial CMS if you are a professional news organisation.
<li>It's not that hard to get a free SSL certificate nowadays; <a href="https://www.letsencrypt.org">LetsEncrypt</a> even has scripts to make the renewal automatic for you. Hell, CloudFlare; which you use, also has free SSL certificates.
<li>You might want to disable directory listing, it just gives too much information; considering the server runs Apache a <i>Options -Indexes</i> is enough.
<li>Fact-check. It looks stupid if you get basic news like this wrong; not really an inforekt but it makes your new site unbelievable; and because you run ads on the site I assume some form of income is appreciated.
<li>Don't ask for push permissions. You run ads from an ad network which you have no control over; asking vistors for persmissions you don't really need is just needlessly exposing your visitors to risks.
<li>Check your plugin configuration; some error logging reveals your local directory structure. Not a huge fail, but again you give away too much information.
<li>Consider hiding your wp-admin behind an IP list; why would someone from China need to be able to log into your admin panel?

