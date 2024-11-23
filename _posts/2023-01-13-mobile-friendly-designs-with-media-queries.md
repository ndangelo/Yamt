---
id: 59654
title: '8. Mobile-friendly designs with media queries'
date: '2023-01-13T18:57:37-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=59654'
permalink: /mobile-friendly-designs-with-media-queries/
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'Learn to Code Now'
    - Projects
---

In one of my classes a student was talking to me about how the company she worked for had recently spent thousands of dollars converting its website into a mobile-friendly version.

I was pretty surprised when I saw a simple desktop site turned into a basic mobile equivalent.

“Thousands of dollars?”, I thought, “that can’t be right!”. After delving into the code, I found just 14 lines had been added. It worked out at roughly $500 per line.

A few hours later, after being taught how to make sites mobile-friendly, the student came back to me with an angry thank-you. Happily she now understood how to make sites work on all different screens.

Less pleasingly she knew her company been ripped off by so-called professionals.

Mobile-friendly — or “responsive” — designs in the web are surprising- ly straightforward to add to your sites. You don’t need to make another version of the site, all you’re focusing on is the look and feel of the site and how it changes from one browser size to another.

As you’re changing the look and feel, all you need to do is add more code into your style sheets.

What we’ll add to our CSS is a new concept called “media queries”. Essentially, we’ll be turning on or off particular CSS styles depending on the size of the browser itself.

Very early in this guide, we talked about the idea that we can put HTML tags inside other tags — Pimp my Ride style. We can do something similar in CSS. We can say “if the browser is smaller than 600px then do these styles … if not, ignore”.

Let’s show an example where we have the whole site having a font size of 18px. On a smaller browser, the font size might look too big, so we want to reduce it to 14px if the browser is smaller than 600px wide:

body {

font-size: 18px;

}

@media (max-width: 600px) { body {

font-size: 14px;

}

}

Notice how we have an @ (or ampersand) with the word “media” straight after it. This is telling CSS to do a browser check. In our rounded brackets, our check is to ask: “Is the browser 600px or less?”. If it is, then add the styles. We can put multiple styles within a media query too:

body {

font-size: 18px;

}

h1 {

font-size: 32px;

}

@media (max-width: 600px) { body {

font-size: 14px;

}

h1 {

}

}

font-size: 21px;

You can also have multiple media queries in the same style sheet. Let’s say we want to have a mid point below 900px and above 600px where the font size should be 16px:

body {

font-size: 18px;

}

@media (max-width: 900px) { body {

font-size: 16px;

}

}

@media (max-width: 600px) { body {

font-size: 14px;

}

}

The order of the media queries matters, as the second one overwrites the first. If they were the other way around, the font size would 16px if the browser was less than 900px and less than 600px too.

Media queries for layouts

Media queries are heavily used to turn multi-column layouts into single-column layouts in responsive design. Let’s take a two-column desktop layout in HTML:

&lt;section&gt;

&lt;div class=”main”&gt;

Here is the main content

&lt;/div&gt;

&lt;div class=”side”&gt; Here is a sidebar

&lt;/div&gt;

&lt;/section&gt;

In your desktop version of your CSS, you’d have something like:

section {

overflow: hidden; width: 920px;

margin: 0 auto 0 auto;

}

div.main { width: 600px; float: left;

}

div.side {

width: 300px; float: right;

}

Media queries with floated layout changes

960px or larger

959px or smaller

ﬂ**oat: left;** ﬂ**oat: right;** ﬂ**oat: none;**

As we want to start breaking the layout at around 960px (920px with a bit of room either side), we can add media queries for browser widths less than 960px.

How do we break that layout? Firstly, we want to get rid of the width on the &lt;section&gt; tag, otherwise it’s bigger than the width of the browser.

Next, we want to stop the two &lt;div&gt; tags from wrapping anything and get rid of the widths so they span the whole width. To get rid of the floating, we can turn it off with “none”. To let the width revert back to normal, we can just say “auto”:

@media (max-width: 960px) { section {

width: auto;

}

div.main { float: none; width: auto;

}

div.side {

float: none; width: auto;

}

}

186 Learn to Code Now

Turning off floats and reverting the widths to automatic size is a very common technique in responsive design. In fact, these lines of code were similar to the thousands of dollars worth of code I mentioned at the start of the chapter.