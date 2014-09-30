---
layout: post
title: "Marquee Element"
date: 2014-09-23 12:14:41 -0400
comments: true
categories: html marquee
---

## Introduction

Marquee tags used to be quite the popular party guests at HTML cocktail parties. They would enter from the front door, head over to the drinks, keep walking, jump out the window, only to re-enter from the front door. Oh! those crazy tricksters.

Still not jogging your memory? Marquees look like this:

<iframe height="70" width="400" src="http://kthffmn.github.io/marquee/js_mimic"></iframe>

If you want a more immersive experience, visit Evan Goer's [Page of the Damned](http://www.goer.org/htmlhorror/htmlhorror1.html). It's simply spectacular.

## History

The marquee element was invented by Internet Explorer to try and get an edge on Netscape Navigator. For the babies out there, Netscape was a web browser that dominated the market up until the [First Browser War](http://en.wikipedia.org/wiki/Browser_wars#First_browser_war) and it had its own proprietary tag, [blink](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blink). The battle was epic, it was like [Ali versus Frazier III](http://youtu.be/VkOQW-Y-PYA) but instead of boxing gloves, they had proprietary, equally obnoxious tags.

The marqee tag was pretty popular, take any GeoCities page from that era, but it had some fierce critics.
Vicious haters and cowards claimed that [the marquee tag was distracting](http://www.usabilityfirst.com/glossary/marquee/) and that it [caused issues for users of assistive technology](https://www.webaccessibility.com/best_practices.php?best_practice_id=441). On both these counts they were right.

Haters also said that [it was difficult to print out webpages with marquee elements](http://en.wikipedia.org/wiki/Marquee_element#Usability_problems). But really who does that? NOT A PROBLEM. Other two complaints: problem. Printing webpages: not problem.

Due to these complaints, the W3C decided that the marquee tag is not valid HTML. However, many browsers such as Chrome, Firefox, and Safari continue to support it.

In fact, Firefox supports a wide array of attributes. For instance, in addition to rendering marquee tags that scroll horizontally, it allows marquee tags to scroll from top to bottom. Another attribute allows you to reverse the markup's direction once it hits the side of the marquee. Firefox also allows marquee tags to be nested (though [Evan Goer does not recommend it](http://goer.org/Journal/2003/10/html_house_of_horror_things_that_go_blink_in_the_n.html)): that is, having on marquee tag inside of another. Put the two and two together, and you get a div that 'bounces'. In other words, the effect of a ball hitting walls below, acheived via JavaScript, can be mimicked with HTML and some old school CSS. 

<iframe width="400" height="305" src="http://kthffmn.github.io/marquee/ball_mimic"></iframe>

## Creating Bouncing Ball using Marquees

**Please read the rest of this post in [Firefox](https://www.mozilla.org/en-US/firefox/new/) as it is the only browser that will support the marqee tags below.**

There are four steps. They are simple. So simple.

**Step 1:** Small div that moves from left to right

```html
<div class="box">
  <marquee class="bar" behavior="alternate">
    <div class="ball">○</div>
  </marquee>
</div>
```

<iframe width="400" height="300" src="http://kthffmn.github.io/marquee/ball-1"></iframe>

**Step 2:** Large div that moves from top to bottom

```html
<marquee class="box" behavior="alternate" direction="up" height="300">
  <div class="ball">○</div>
</marquee>
```

<iframe width="400" height="310" src="http://kthffmn.github.io/marquee/ball-2"></iframe>

**Step 3:** Nest the small div in the large div

```html
<marquee class="box" behavior="alternate" direction="up" height="300">
  <marquee class="bar" behavior="alternate">
    <div class="ball">○</div>
  </marquee>
</marquee>
```

<iframe width="400" height="310" src="http://kthffmn.github.io/marquee/ball-3"></iframe>

**Step 4:**&nbsp;&nbsp;\*lowers glasses like Tim Gun\*&nbsp;&nbsp;Make it work.
<iframe width="400" height="320" src="http://kthffmn.github.io/marquee/ball-4"></iframe>

It's an easy way to create the appearance of a bouncing ball that requires no JavaScript or fancy new CSS and it only renders in [1 out of 10](http://thenextweb.com/insider/2014/05/16/chrome-still-used-across-desktop-mobile-firefox-falls-safari-ie/) viewer's browsers! Yay!

## Throwback
The [SpaceJam website](http://www2.warnerbros.com/spacejam/movie/jam.htm) is still alive and thriving.