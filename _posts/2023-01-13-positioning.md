---
id: 59658
title: '10. Positioning'
date: '2023-01-13T19:01:04-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=59658'
permalink: /positioning/
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'Learn to Code Now'
---

When making more complex layouts, sometimes we **might have to use styles that don’t fit into the usual floated layout pattern.**

As designers, we want to be able to do more with our designs! We’re going to talk about three different ways to change our design.

Some of this gets a bit complex and weird so don’t worry if you don’t understand it straight away.

### Relative positioning

Sometimes we may want to move a tag based on where it currently is. Let’s say we want to adjust a &lt;header&gt; tag by moving it relative to its normal position, to be down 10 pixels and further right by 20 pixels.

We can use some new CSS rules to achieve this. They are the position rule, the top rule and the left rule. We’re positioning the tag relative to where it would usually be, then moving it from the top by 10 pixels, then moving it from the left by 20 pixels:

```css
header {

position: relative; top: 10px;

left: 20px;

}
```

We can also move it in the opposite direction by using two other rules called “bottom” and “right”:

```css
header {

position: relative; bottom: 10px; right: 20px;

}
```

Moving the tag will leave a “shadow” — basically a gap where the tag would have usually sat — so even if we move it a large distance, there will still be a gap where it was originally.

If we don’t want a shadow, we can use the next type of positioning, called absolute positioning.

### Absolute positioning

Absolute positioning means that we are positioning the tag not based on its normal place but relative to two things: the first is based on whether it’s inside a relatively positioned tag. For example, if we have some HTML that looks like this:

```markup
<header>

<h1>Hi there</h1>

</header>
```

If we have any relative positioning on the &lt;header&gt; tag, any absolute positioning on the &lt;h1&gt; will be based on the internal coordinates of the

&lt;header&gt; tag:

```css
header {

position: relative; top: 0;

left: 0;

}

h1 {

position: absolute; top: 20px;

right: 20px

}
```

Even if we add no movement to the header here, our &lt;h1&gt; will be moved without a shadow of where it once was to the top right corner of the &lt;header&gt; tag.

The second rule of absolute positioning is the absolutely position tag isn’t inside any relative tag, it will be positioned to the whole page itself.

If our CSS was simply:

```css
h1 {

position: absolute; top: 20px;

right: 20px;

}
```

The &lt;h1&gt; would say bye-bye to the &lt;header&gt; tag and attach itself to the whole page to the top right corner, even if the header was nowhere near the top right corner of the page. Crazy, right?

So two rules for absolute positioning, if you want the “co-ordinates” of the tag (the left, right, top or bottom) based on another tag, put that tag as a relatively positioned tag. If you want the “co-ordinates” to be based

on the whole page, make sure that tag doesn’t have any parent tags which are relatively positioned. Phew. It’s a tough one.

One thing you might notice with absolute position is that the tag sticks to the page itself when you scroll. But what if you want the tag to be fixed to the browser rather than the page?

### Fixed positioning (or how to make things sticky)

You may have seen a lot of the next CSS rule on the Internet. The idea of having tags that follow you down the page. Facebook and Twitter both have “sticky” headers.

We talked a little about how to fix things to the browser back in CSS backgrounds, when we used “background-attachment: fixed” to fix the background to the browser itself rather than the tag. We can use the similar idea of “fixed” in the tag’s position too:

```css
header {

position: fixed; top: 0;

left: 0;

}
```

This will attach the tag to the page in the top left corner and keep it there, even if scrolling up and down the page.

**Fixed vs absolute positions on browser scroll**

**position: ﬁxed;**

**position: absolute;**

One thing you might noticed is that when you take the tag out of the usual context of the page, it might lose its width. That’s because it has no clue about what size it should be. If you want to fill up the whole width of the browser, you can add in:

```css
header {

position: fixed; top: 0;

left: 0;

width: 100%;

}
```

This will stretch the header across the whole of the page. We could also start to add heights, background colors and more to this header to fill it out.

### Combining positions and floats

One thing you might be tempted to do is start building your layouts using positions rather than floats, because it looks easier — it’s similar to design programs like Photoshop and Sketch where you set an “x” and “y” position and away you go. But resist the temptation. Floats are a more powerful tool, especially when it comes to responsive design. The more positioning you use, the more tangles you’ll end up in, when it comes to fixing your layout for mobile.

We can however combine positions and floats in great ways. Let’s say we want a sticky header where our title is on the left and navigation is on the right. Our HTML would look something like:

```markup
<header>

<h1>Boyce</h1>

<nav>

<a href="portfolio.html">Portfolio</a>

<a href="about.html">About</a>

<a href="contact.html">Contact</a>

</nav>

</header>
```

So first we want to fix our header to the top of the page. Next we want to move our title to the left, then we want to move our navigation to the right. Remember, because we’re floating everything inside the header, we need to fix the layout with a hidden overflow:

```css
header {

position: fixed; top: 0;

left: 0; overflow: hidden;

}

h1 {

float: left;

}

nav {

float: right;

}
```

It might be very tempting to make the floats into absolute positions, but don’t do this as it makes it harder when we move to responsive later!

Overlapping positions

Sometimes you might have tags that overlap due to using position rules in lots of ways. The default order is based on whatever tag is further down in the HTML but sometimes you want to switch them out.

As we said earlier in the guide, going across the page is called the “x” direction and going down the page is called the “y” direction. There’s one more direction, the “z” direction, which is to do with how close a tag is to the user.

By default, every tag is at the base level, zero, and then sorted by the order of the HTML. We can change that by increasing the “z-index” of the tag. The higher the “z-index”, the “closer” to the user the tag will seem.

To change the z-index, just increase or decrease the number:

```css
header {

z-index: 1;

}

nav {

z-index: 2;

}
```

This would make the nav be always above the header. Both would be always above any tag without a z-index as the default is 0.