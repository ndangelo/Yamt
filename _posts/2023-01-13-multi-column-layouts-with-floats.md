---
id: 59652
title: "7. multi-column layouts with\_floats: Wrapping elements using floats, Overflow,Transparency with opacity and rgba colors, Drop shadows"
date: '2023-01-13T18:56:29-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=59652'
permalink: /multi-column-layouts-with-floats/
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'Learn to Code Now'
    - Projects
---

Wrapping elements **using floats**

Let’s imagine our HTML is the following…

&lt;p&gt;

&lt;img src=”president.jpg”&gt;

Today, the president was very happy…

&lt;/p&gt;

Here we have a &lt;p&gt; tag which is a “block” tag so it fills across the page and any new tags after the &lt;p&gt; tag will go underneath. Inside our &lt;p&gt; tag, we have an image and some content. The content is just inline content as it’s regular old text. The &lt;img&gt; tag is also an inline tag, so by default the image sits as if it was part of text, its bottom sitting at the text’s baseline.

How do we make the text content wrap around the image’s right hand side? We make the &lt;img&gt; tag float to the left:

img {

float: left;

}

What if we wanted the text to wrap on the left and the image to go to the right?

img {

float: right;

}

Unfortunately, there’s no center floating at the moment, so you can’t wrap text on both sides of an image — we only get the choice of left or right.

Making layouts with floats

We can use the idea of moving tags to the left or the right to build up our content. Let’s take a header where we want to move our &lt;h1&gt; tag to the left corner and our &lt;nav&gt; tag to the right corner:

&lt;header&gt;

&lt;h1&gt;Furneaux’s Flower Shop&lt;/h1&gt;

&lt;nav&gt;

&lt;a href=”about.html”&gt;About&lt;/a&gt;

&lt;a href=”blog.html”&gt;Blog&lt;/a&gt;

&lt;a href=”contact.html”&gt;Contact&lt;/a&gt;

&lt;/nav&gt;

&lt;/header&gt;

First of all, in our style sheet, we can use floats to move the &lt;h1&gt; tag to the left:

h1 {

float: left;

}

This will make all the other content in the header wrap around the &lt;h1&gt; tag on the right hand side. We can then use floats to move the &lt;nav&gt; tag to the right hand side:

h1 {

float: left;

}

nav {

float: right;

}

Great! This will move the &lt;h1&gt; to the left and the &lt;nav&gt; to the right. However, you might notice — especially if you had a background on your &lt;header&gt; tag — that some of the layout could be messed up.

Fixing layouts with clearfix

Whenever you’re floating any tags, it’s a good idea to remember what you’re actually doing — you’re taking the tag out of its usual position to make other content and tags wrap around it. As you’re doing this, the tag that surrounds the floated tag — we’ll call this the “parent” tag

— doesn’t realize that you’ve floated the tag. Cascading style sheets can

only go deeper into tags so any higher-level tags are unaware of what you’re doing inside them.

When we float all of the content inside a tag (like in the &lt;header&gt; in the previous example), it doesn’t realize that there’s any content inside it as you’re floating every tag inside it. The tag gets confused and collapses down as if there’s no content inside it.

You might see this happen when your background disappears or your floated content starts to escape the edges of your tag.

Why does this happen? Well, the truth is that floats were never designed to make layouts, but us coders found a “hack” — a way that just happened to work even if it wasn’t meant to fix the problem.

Remember CSS was made by scientists in the mid 1990s when web sites looked a lot simpler, and they didn’t think web pages would need any complex layouts. So when we use floats to make layouts, we’re “hacking” the system and have to deal with its limitations.

To get around this, we use another fix called a “clearfix”. There are a lot of different fixes and no single agreed version. The simplest way is to add one rule to your outer tag:

header {

overflow: hidden;

}

h1 {

float: left;

}

nav {

float: right;

}

We’ll talk about what about overflow is in a later section, but for now, we’ll add it in and leave it unexplained!

Three column layouts

To add more columns to your layout, for instance if you have a blog with two sidebars and one main area for blog posts, we can structure our HTML in this way:

Floating content without and with clearfix

ﬂ**oat: left;** ﬂ**oat: right;**

over**ﬂ**ow: hidden;

ﬂ**oat: left;** ﬂ**oat: right;**

&lt;section&gt;

&lt;div class=”sidebar”&gt; Post by Rik Lomas

&lt;/div&gt;

&lt;div class=”content”&gt;

Here’s a really long blog post about…

&lt;/div&gt;

&lt;div class=”comments”&gt;

I love this post! It’s…

&lt;/div&gt;

&lt;/section&gt;

Here we have one outer &lt;section&gt; tag that acts as the “parent” to the three &lt;div&gt; divider tags. We’ve given each &lt;div&gt; tag a different class so we can style them up differently.

To style them up, I’m going to give the sidebar around 20 percent of the width, the main content 50 percent, then give the remainder (30 percent) to the comments.

Remember as we’re floating all the tags inside the &lt;section&gt; tag, we need to add our “clearfix”:

section {

overflow: hidden;

}

div.sidebar { float: left; width: 20%;

}

div.content { float: left; width: 50%;

}

div.comments { float: right; width: 30%;

}

Notice that we’re floating two tags to the left and one to the right and all the numbers add up to 100 percent. The height of the section tag will be based on whatever the highest content is in the sidebar, content or comments &lt;div&gt; tags.

A grid layout with floats

over**ﬂ**ow: hidden; **ﬂ**oat: left;

Making a grid with floats

Let’s say we want to make a grid of 3 by 2 using floats. There are a few ways to do this. The first is if we have content that is equal heights — let’s say we have images that are all 300 by 300 pixels. We would set up the HTML like so:

&lt;section&gt;

&lt;img src=”photo\_1.jpg”&gt;

&lt;img src=”photo\_2.jpg”&gt;

&lt;img src=”photo\_3.jpg”&gt;

&lt;img src=”photo\_4.jpg”&gt;

&lt;img src=”photo\_5.jpg”&gt;

&lt;img src=”photo\_6.jpg”&gt;

&lt;/section&gt;

We can make the first image float left. That will then wrap the second image on the right hand side of the first image. If we float the second image to the left, the third image will wrap on the right hand side. If we float the third image, there’s no more room for the fourth image to fit into so it’ll go on to the next line down. In our CSS we can add:

section {

overflow: hidden; width: 900px;

}

img {

float: left; width: 300px; height: 300px;

}

Sometimes we don’t know how tall the items in our grid might be. If we use the previous HTML and CSS, we might get our grid looking a little messed up. To fix our HTML and CSS to make a grid with unknown heights, we can add:

&lt;section&gt;

&lt;img src=”photo\_1.jpg”&gt;

&lt;img src=”photo\_2.jpg”&gt;

&lt;img src=”photo\_3.jpg”&gt;

&lt;/section&gt;

&lt;section&gt;

&lt;img src=”photo\_4.jpg”&gt;

&lt;img src=”photo\_5.jpg”&gt;

&lt;img src=”photo\_6.jpg”&gt;

&lt;/section&gt;

Then our CSS will be:

section {

overflow: hidden; width: 900px;

}

img {

float: left; width: 300px;

}

You may have noticed that the style sheet is pretty much the same as before. Nothing’s changed. All we’ve done is change the HTML which is the structure of the web page. Sometimes the fixes we need aren’t in CSS, they can be in just the HTML, or even both HTML and CSS.

Clearing floats

Sometimes we might not want a particular tag to wrap around another floated tag, but go underneath. To add this is we can use the CSS rule “clear”. We can use the options to avoid (or “clear”) floated left tags, floated right tags or both.

To clear floated left tags only:

div {

clear: left;

}

To clear floated right tags only:

div {

clear: right;

}

To clear both left and right floated tags:

div {

clear: both;

}

Clearing tags in this way can be a really useful way of building up your web designs.

The different kinds of overflow

CSS IS

AWESOME

default

CSS IS

AWESOM

hidden

CSS IS

AWESOM

auto +

scroll

Overflow

We talked earlier about a new rule called overflow that we didn’t explain. In this chapter we’ll talk a little more about what overflow actually is and what it does.

Let’s say we have a &lt;div&gt; tag that’s 300 by 300 pixels. Most of the time we’d expect our content to fix inside the tag, but what if we have more content than can do that?

Think of a drinking glass. Most of the time, liquid would fit inside it comfortably, but if we have too much, what happens? It overflows.

Luckily in CSS, we can control what happens. By default, just like with a liquid, the content will overspill and escape the container, but we can change how that works.

If we want to cut off any extra content so it’s clipped, we can give the

&lt;div&gt; tag an overflow of “hidden”:

div {

overflow: hidden;

}

If we decide that within our tag, we want a little scroll bar so a user can see the rest of the clipped content, we can add:

div {

overflow: scroll;

}

On some web browsers, this will give the &lt;div&gt; tag a permanent scroll bar, even if the content isn’t bigger than the tag. To make it automat- ically have a scroll bar if the content is bigger and no scroll bar if it’s smaller, we can add the overflow automatically:

div {

overflow: auto;

}

The overflow hack we used in the last chapter for fixing floats works because we’re forcing the parent to stretch around all of the content, floated or not, by using a hidden overflow.

Transparency with opacity and rgba colors

In some web designs we might want to make parts of our page slightly transparent. There are two ways to do this. The first is using a CSS rule called opacity. By default, every tag is full opacity (“1”). We can hide tags by making them have no opacity (“0”), or we can pick somewhere in between.

Let’s say we want to make an &lt;h1&gt; tag 30 percent opaque (or mostly see-through), we can add:

h1 {

opacity: 0.3;

}

We can even make it so we can have it fade back into full opacity on hover:

h1 {

opacity: 0.3;

transition: opacity 0.5s;

}

h1:hover {

opacity: 1;

}

In this example we’ve even added a transition so we can fade it over half a second.

The opacity CSS rule will make the whole tag transparent, including the background and the content inside it. However, sometimes we might just want the background to be see-through, or the text to be slightly transparent.

To do this we need to talk about rgba colors.

rgba colors

Usually in our colors we use hex values, as discussed previously. We start with a hash, then six numbers or letters.

header {

background-color: #ff0099;

}

Forgetting the hash tag, the first two letters denote red, the next two denote green and the last two denote blue, but there’s no way to add a transparency effect in here.

However we can use a different style of color called rgba, which stands for red, green, blue and alpha.

This works slightly differently to hex values. Instead of writing in computer counting, we can add human/Arabic numbers from 0 to 255 (or “ff” in computer speak) to determine each separate color. We can then add a value from 0 to 1 for how much opacity the color should have.

We can convert the color above and make it half see-through:

header {

background-color: rgba(255, 0, 153, 0.5);

}

It’s not something I can easily convert just by looking at the hex value, I generally use an online tool, Photoshop or Sketch to work out what the hex value’s colors are.

Remember this will just change the background’s opacity, not the content. We can use a hover state to transition between two rgba colors in the same way:

header {

background-color: rgba(255, 0, 153, 0.5); transition: background-color 0.5s;

}

header:hover {

background-color: rgba(255, 0, 153, 1);

}

Drop shadows

For both text and tags, we can add drop shadows to apply some subtle (or not so subtle) effects to our designs. There are two types of drop shadows we can use, one for the text and one for the tag itself.

Text drop shadows

The CSS rule for text shadows takes four values, the “x” direction, the “y” direction, the “blur”, then the color of the shadow.

The “x” direction is across the page. If you want to move the shadow to the right of the tag, you can use a positive number of pixels (e.g. 5px). To keep the same, just use “0”. If you want to move the shadow to the left, you can use negative pixels (e.g. -5px). Same thing for the “y” direction, 5px would be further down the page, -5px would be back up the page, 0 would be no difference up or down.

The blur is also a pixel value referring to how far the drop shadow should be blurred over. If it’s 0, there’s no blur to the shadow and it looks sharp. The bigger the blur value, the more area the shadow spreads over and the lighter it will be.

The last is a color value. This can be a hex or rgba value. In fact, rgba colors are great for drop shadows as they can give them a transparency that hex values can’t.

Let’s say we want to give our &lt;h1&gt; tag a 50 percent transparent black text shadow that is slightly blurred, straight down and to the right. We would add:

h1 {

text-shadow: 0 5px 2px rgba(0, 0, 0, 0.5);

}

We’re not putting any left value to make it go straight down. Then we’re putting the value 5px downwards with a 2px blur, then giving it a rgba color.

Outer drop shadow

The other drop shadow effect is the “box-shadow” — instead of just being on the text, it’s on the overall tag itself. It has pretty much the same values, “x”, “y”, blur and color, just this time it’s a different rule, the “box-shadow” rule:

h1 {

box-shadow: 0 5px 2px rgba(0, 0, 0, 0.5);

}

As before, we’re having a shadow that goes straight down by 5px with a 2px blur and a 50 percent transparent black color.

Glow effect

We can use box-shadow to give a tag a glow effect too. All we’d need to do is not move the shadow down or to the left, then give it a large blur. In this example, we’ll blur by 15px with a 40 percent transparent white color:

header {

box-shadow: 0 0 15px rgba(255, 255, 255, 0.4);

}

Inner shadows

Most shadows go around the edge of the tag itself, but we can add one more value to make the box shadow go from the outer edge to the inner edge. All we do is add the word “inner” to the start of our box-shadow rule.

header {

box-shadow: inner 0 0 15px rgba(255, 255, 255, 0.4);

}