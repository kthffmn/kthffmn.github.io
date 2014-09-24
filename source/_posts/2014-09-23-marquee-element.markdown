---
layout: post
title: "Marquee Element"
date: 2014-09-23 12:14:41 -0400
comments: true
categories: html, marquee
---

# Marquee Element

## Introduction

Marquee tags used to be quite the popular party guests at HTML cocktail parties. They would enter from the front door, head over to the drinks, keep walking, jump out the window, only to re-enter from the front door. Oh! those crazy tricksters.

Still not jogging your memory? Marquee tags look like this:

<iframe src="http://kthffmn.github.io/marquee/js_mimic"></iframe>

If you want a more immersive experience, visit Evan Goer's [Page of the Damned](http://www.goer.org/htmlhorror/htmlhorror1.html). It's simply spectacular.

## History

The marquee tag was invented by Internet Explorer to try and get an edge on Netscape Navigator. For the babies out there, Netscape was a web browser that dominated the market up until the [First Browser War](http://en.wikipedia.org/wiki/Browser_wars#First_browser_war) and it had its own proprietary tag, [<blink>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blink).

Vicious haters and cowards claimed that [the marquee tag was distracting](http://www.usabilityfirst.com/glossary/marquee/) and that it[caused issues for users of assistive technology](https://www.webaccessibility.com/best_practices.php?best_practice_id=441). On both these counts they were right.

Haters also said that [it was difficult to print out webpages with marquee elements](http://en.wikipedia.org/wiki/Marquee_element#Usability_problems). But really who does that? NOT A PROBLEM. Other two complaints: problems. Printing webpages: not problems.

Due to these complaints, the W3C decided that the marquee tag is not valid HTML. However, many browsers such as Chrome, Firefox, and Safari, continue to support it.

In fact, Firefox supports a wide array of features. For instance, in addition to rendering marquee tags that scroll horizontally, it allows marquee tags to scroll from top to bottom and to alternate from side to side. It also allows marquee tags to be nested: that is, having on marquee tag inside of another. Put the two and two together, and you get a div that 'bounces', like this:

<iframe src="http://kthffmn.github.io/marquee/ball_mimic"></iframe>

## Bouncing Ball

Note: Firefox is the only browser that will support the marqee tags below. To get the full effect of this post, please open it in [Firefox](https://www.mozilla.org/en-US/firefox/new/).

The first step is to have a horizontal div move from left to right:

<iframe src="http://kthffmn.github.io/marquee/ball-1"></iframe>

The second step is to make a div that moves from top to bottom:

<iframe src="http://kthffmn.github.io/marquee/ball-2"></iframe>

The third step is to nest them:

<iframe src="http://kthffmn.github.io/marquee/ball-3"></iframe>

The fourth step is to style it:

<iframe src="http://kthffmn.github.io/marquee/ball-4"></iframe>

## Throwback
I present to you the [SpaceJam website](http://www2.warnerbros.com/spacejam/movie/jam.htm).