---
layout: post
title: "I'm All About that Base...line"
date: 2014-09-29 14:41:14 -0400
comments: true
categories: html css img vertical-align
---

## Background

From [Google Now](http://www.google.com/landing/now/#whatisit) to [Pintrest](http://www.pinterest.com/ruth77rn/ui-patterns-cards/), the [card UI pattern](http://blog.intercom.io/why-cards-are-the-future-of-the-web/) is gaining traction. 

## Wha?

A while back, I implemented this design:

```css
.card {
  display: inline-block;
  background-color: #89b1b5;
  padding: 10px;
  margin: 5px;
}
```

```html
<div class="card">
  <img src="picture.jpeg" />
</div>

<div class="card">
  <p>Lorem ipsum</p>
</div>
```
I imagined that this would look okay. Instead, it looked like this:

<iframe width="330" height="235" src="http://kthffmn.github.io/baseline-examples/default">

RUN FOR YOUR LIFE I WON'T MAKE IT!

Q: Why do bad things happen to good HTML elements?"

A: Because we live in a cruel world where there is no god.

## Why?

So it turns out that images have a veritical-align property that defaults to baseline. You might be asking, "What the hell is baseline?" 

Do you remember writing on college-ruled paper in school or are you reading this in the future where everyone comminucates via brain chips and Kanye West is worshipped as a god? Well, for those of you who remember ruled paper, those blue lines are perfect examples of baselines. Letters like p, q, and y have appendages that exend below the baseline but most letters sit on it. 

For instance, the teal line in this image is the baseline:

![baseline image example](http://kthffmn.github.io/baseline-examples/baseline.png)

The vertical-align property does not affect the positioning of the element's contents. Rather, it affects the element's alignment on the page.

For my demo card example, the image's default alignment of baseline was causing the strange behaviour. It was trying to line up with the baseline of the text in the div to its right, causing the left-hand div to be higher than the right-hand div.

![baseline drawn in example above](http://kthffmn.github.io/baseline-examples/explicit-baseline.png)

## Solution

A quick way to solve this is to override the image default:

```css
.card img {
  vertical-align: middle;
}
```

<iframe width="330" height="235" src="http://kthffmn.github.io/baseline-examples/custom">

To learn more about the vertical-align property, visit [Impressive Web's blog about it](http://www.impressivewebs.com/css-vertical-align/) or [CSS-Trick's vertical-align article](http://css-tricks.com/almanac/properties/v/vertical-align/).
