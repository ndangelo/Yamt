---
id: 59656
title: '9. CSS Displays @Media'
date: '2023-01-13T18:58:08-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=59656'
permalink: /css-displays/
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'Learn to Code Now'
    - Projects
---

Earlier in this guide, we talked about different tags having different types — some tags were “blocks” that push other tags down the page, others were “inline” that follow along the usual style of text.

Some examples of “block” tags are &lt;header&gt;, &lt;h1&gt;, &lt;p&gt; and &lt;div&gt;. When we place them next to each other, they go down the page (ignoring any floats we might do).

Some examples of “inline” tags are &lt;a&gt;, &lt;img&gt;, &lt;b&gt; and &lt;span&gt;. When we place these inline tags next to each other, they go across the page and on to the next line if they can’t fit, just like words in a sentence would.

Sometimes we may want to change the type of tag in CSS depending on its context. A good example of this is when we have links in a navigation. On a desktop layout, we may want the links next to each other, but on a mobile, it may make more sense to have them go down the page instead.

Let’s take an example piece of HTML:

```markup
<nav>

<a href="about.html">About</a>

<a href="blog.html">Blog</a>

<a href="contact.html">Contact</a>

</nav>
```

On a desktop layout, it would make sense for this to go across the page and we can let our users read from left to right.

However, on a mobile device, we might not have enough room to display them from left to right. We can switch how these links look from their default “inline” display to looking like a “block” tag. To do this we will use a CSS rule called display to change how the tag acts.

First of all we’ll set a media query for mobile only at around 600px browser width, then select the links in the nav, and change how they act:

```css
@media (max-width: 600px) { nav a {

display: block;

}

}
```

### Making buttons with inline-block

CSS was invented in the mid 1990s by scientists and little did they think that it would become quite as used as it has. The downside of having scientists make tools used for design is they didn’t really think about how designers would use the tools in 20 years’ time.

Perhaps the most annoying thing about inline tags like &lt;a&gt; and &lt;span&gt; is that they don’t listen to a few of the more important CSS rules, mainly width and height.

If you try and give them a width and height, they’ll just ignore you. Ugh. What’s with that? The reason is inline tags were always meant to act like text, and technically, they should fit to the content inside them and not be sized.

Several years later, the new committee that updates CSS called the W3C (or the World Wide Web Consortium) decided that if they suddenly gave inline tags the power to control width and height, they may break a lot of older websites. So instead they came up with a half-way house: the “inline-block”. A rule that lets tags go across the page, just like inline tags, but can be given widths and heights.

So where would be good places to use this? For me, this would be for buttons.

Let’s take an example of some HTML:

```markup
<nav>

<a href="about.html">About</a>

<a href="login.html">Log in</a>

<a href="signup.html">Sign up</a>

</nav>
```

Let’s say I want to highlight the sign up link. At the moment, all the links would look the same, so the first thing I’d want to do is add a class to the sign up link. We’ll call the class “button”, but you could call it anything you like (e.g. “signup”, “attention”, etc):

```markup
<nav>

<a href="about.html">About</a>

<a href="login.html">Log in</a>

<a href="signup.html" class="button">Sign up</a>

</nav>
```

Now in our CSS we can make this look more like a button. We can give it a width, some padding, make the text centered, rounded corners and more!

```css
nav a {

text-decoration: none; color: black;

}

nav a.button {

display: inline-block; width: 100px; background-color: red; color: white;

text-align: center;

padding: 10px 20px 10px 20px; border-radius: 5px;

}
```

Just by adding in the **“inline-block**” we have a lot more control over how it looks.

### Hiding tags completely

Alongside the option to change the display type of tags between “inline”, “inline-block” and “block”, we also have the option of completely hiding the tag.

A first question may be, why not just delete the content from the HTML? Yes, you could if you’re not going to need it anymore, but what if you want to be selective? What if you want to see something on a desktop screen but not a mobile?

Let’s say we want to remove any &lt;section&gt; tag with the class of “timeline” on a mobile screen. Roughly we want to say, at around 600px or less on the browser width, hide this completely.

We don’t want to make its opacity zero as the area will still be taken up by a see-through box. We want to pretend it wasn’t there at all, as if it wasn’t in the HTML:

```css
@media (max-width: 1800px) { section.timeline {

display: none;

}

}

/*We could do the opposite too, which would be to hide on a desktop but show on the mobile browser:*/

section.timeline { display: none;

}

@media (max-width: 600px) { section.timeline {

display: block;

}

}
```

See the Pen Untitled by Nicholas D’Angelo (@ndangelo) on CodePen.

This way we start with the default (totally hidden), then show it when we’re on a mobile version of the site.