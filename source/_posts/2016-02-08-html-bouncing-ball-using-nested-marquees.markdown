---
layout: post
title: "HTML Bouncing Ball Using Nested Marquees"
date: 2016-02-08 12:14:41 -0400
comments: true
categories: html marquee
---

## Introduction

Marquee tags used to be quite the popular party guests at HTML cocktail parties. They would enter from the front door, head over to the drinks, keep walking, jump out the window, only to re-enter from the front door. Oh! those crazy tricksters.

Still not jogging your memory? Marquees look like this:

<iframe height="70" width="400" src="https://kthffmn.github.io/marquee/js_mimic"></iframe>

If you want a more immersive experience, visit Evan Goer's [Page of the Damned](http://www.goer.org/htmlhorror/htmlhorror1.html). It's simply spectacular.

## History

The marquee element was invented by Internet Explorer to try and get an edge on Netscape Navigator. For the babies out there, Netscape was a web browser that dominated the market up until the [First Browser War](http://en.wikipedia.org/wiki/Browser_wars#First_browser_war) and it had its own proprietary tag, [blink](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blink). The battle was epic, it was like [Ali versus Frazier III](https://kthffmn.github.io/marquee/public/img/netscape-vs-ie.png) but instead of boxing gloves, they had proprietary, equally obnoxious tags.

The marqee tag was pretty popular—look at basically any GeoCities page—but it had some fierce critics. Vicious haters and cowards claimed that [the marquee tag was distracting](http://www.usabilityfirst.com/glossary/marquee/) and that it [caused issues for users of assistive technology](https://www.webaccessibility.com/best_practices.php?best_practice_id=441). On both these counts they were right. Haters also said that [it was difficult to print out webpages with marquee elements](http://en.wikipedia.org/wiki/Marquee_element#Usability_problems). But really who does that? NOT A PROBLEM. Other two complaints: problem. Printing webpages: not problem.

Due to these complaints, the W3C decided that the marquee tag is not valid HTML, declaring it non-compliant. However, many browsers such as Chrome, Firefox, and Safari continue to support it.

In fact, Firefox and now Chrome support a wide array of attributes. For instance, in addition to rendering marquee tags that scroll horizontally, these browsers allow marquee tags to scroll from top to bottom. Another attribute allows you to reverse the content's direction once it hits the side of the marquee. These browsers also allow marquee tags to be nested (though [Evan Goer does not recommend it](http://goer.org/Journal/2003/10/html_house_of_horror_things_that_go_blink_in_the_n.html))—that is, having one marquee tag inside of another. Put the two and two together, and you get a div that 'bounces'. In other words, the effect of a ball hitting walls can be achieved with just HTML and some old school CSS.

<iframe width="400" height="300" src="https://kthffmn.github.io/marquee/ball_mimic"></iframe>

## Creating a Bouncing Ball Using Marquees

**Please read the rest of this post in [Firefox](https://www.mozilla.org/en-US/firefox/new/) or [Chrome](https://www.google.com/chrome/browser/desktop/) as most other browsers can't support the marqee tags below.**

There are five steps. They are simple. So simple.

**Step 1:** Create the markup

To start out, we're gonna nest some divs like they're dreams and we're in *Inception*. Okay so create a container. Inside this container, create a bar-like div. Inside this bar, nest a green square. Ta-da!

<iframe width="400" height="300" src="https://kthffmn.github.io/marquee/ball-0.html"></iframe>

```html
<div class="container">
  <div class="bar">
    <div class="square"></div>
  </div>
</div>
```

**Step 2:** Move the square from left to right

Wrap the `.square` div in a marquee tag and give this marquee tag a behavior attribute of `alternate`.

```html
<marquee behavior="alternate">
  <div class="square"></div>
</marquee>
```

<iframe width="400" height="300" src="https://kthffmn.github.io/marquee/ball-1.html"></iframe>

**Step 3:** Move the bar from top to bottom

Repeat step 2 but for the `.bar` div: wrap it in a marquee tag with the `alternate` behavior. Add two more attributes: give it a direction of `up` and give it the `height` of the container in which it's nested.

```html
<marquee behavior="alternate" direction="up" height="300">
  <div class="bar">
    <marquee>...</marquee>
  </div>
</marquee>
```

<iframe width="400" height="300" src="https://kthffmn.github.io/marquee/ball-2.html"></iframe>

**Step 4:** Nest a circle div inside the square div

Take a look at CSS Trick's [shapes article](https://css-tricks.com/examples/ShapesOfCSS/) if you need help styling a circle-shaped div.

```html
<div class="square">
  <div class="circle"></div>
</div>
```

<iframe width="400" height="310" src="https://kthffmn.github.io/marquee/ball-3.html"></iframe>

**Step 5:**&nbsp;&nbsp;\*lowers glasses like Tim Gun\*&nbsp;&nbsp;Make it work.

<iframe width="400" height="320" src="https://kthffmn.github.io/marquee/ball-4.html"></iframe>

Don't want to write any of this? I get it. Here's the [Codepen](https://codepen.io/anon/pen/KVrWmr).

## Conclusion

Using nested marquee tags is an easy way to create the appearance of a bouncing ball that requires no JavaScript or fancy new CSS and it renders in almost [50%](https://en.wikipedia.org/wiki/Usage_share_of_web_browsers#Summary_tables) of viewers' browsers! Yay!

To learn more about the marquee tag, check out [Evan Goer's blog](http://goer.org/Journal/2003/11/the_marquee_element_revolutions.html), [Zach Holman's blog](http://zachholman.com/posts/only-90s-developers/), or [David Walsh's letter to the webmaster](http://davidwalsh.name/open-letter-webmaster).
