---
id: 59660
title: '11. Transforms: rotations, scaling and skews, Vertical alignment, Head tags and search engines, Flexbox, CSS animations, Forms, Audio, video and media'
date: '2023-01-13T19:03:14-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=59660'
permalink: /transforms-rotations-scaling-and-skews/
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'Learn to Code Now'
    - Projects
---

Back in 2010, Steve Jobs wrote an open letter about Adobe Flash, the multimedia tool that most of the Web was using for animation and video content.

Jobs said he didn’t want to include Flash as part of the iPhone’s web browser, because of what he said was its “rapid energy consumption, poor performance on mobile devices, abysmal security, lack of touch support, and desire to avoid a third party layer of software”.

Some in the industry were appalled — how dare Apple not include Flash? It was everywhere on the Web!

But Jobs was right. It made no sense to have a website that contained Flash — why have two separate areas, one using web technologies and one using Flash, when we could forget the latter and just build sites using the former?

Over the last few years, Flash has lost most of its power over the Web. Friends of mine who were Flash coders have had to change careers as they found less and less demand for their specialism.

So the Web has had to catch up to fill the gaps that Flash left behind. One of the things that CSS didn’t have was a way to transform tags

— meaning the ability to rotate, skew and scale tags. So the clever people at the World Wide Web Consortium (or W3C, the body which

coordinates the development of web standards) made the transform rule in CSS.

### Rotations

Previously in this guide we talked about linear gradients and how we can angle them using the units “deg” rather than “px”. We can reuse them in this instance. To rotate a tag clockwise by 10 degrees we can use:

```css
div {

transform: rotate(10deg);

}
```

See the Pen Rotate Div by Nicholas D’Angelo (@ndangelo) on CodePen.

If we want to rotate in a counter-clockwise (or anti-clockwise) way, we can use negative degrees:

```css
div {

transform: rotate(-10deg);

}
```

### Skewing

Skewing is the mathematical way to make a tag turn from a rectangle into a parallelogram. We can skew in two direction, the first being the “x” direction (across the page), the second being the “y” direction. Both take degree units too. We’re telling the corners to increase or decrease their angles by a certain amount. For instance, if we want to add a little bit of skew across the page, we would add:

```css
div {

transform: skew(10deg, 0);

}
```

This would mean the bottom of the tag would be further across the page than the top.

To skew down the page, we can do:

```css
div {

transform: skew(0, 10deg);

}
```

This would mean the right of the tag would be further down the page than the left.

### Adding scale

Sometimes you might want to add a scale to your tag. For instance, you may want the tag to get bigger as you hover over it. Scale takes a multiple number, similar to line heights, so by default all tags start at 1

times the size. If we want to make the tag 20 percent smaller, we would make it 0.8 times the size:

```css
div {

transform: scale(0.8);

}
```

We can also use this to make tags pop out on hover, let’s say we want to make all the images in a section pop out by 120 percent on hover:

```
section img {

transition: transform 1s;

}

section img:hover { transform: scale(1.2);

}
```

We don’t need to add the transform in the non-hovered style because the default is just 1. We’re also using transition to fade between 1x and

1.2x the size over 1 second. It’s easy to get the words transition and transform mixed up so watch out!

### Translate

We spoke earlier in the guide about moving tags around using relative positions. There is another way to do this, and that’s to use translate.

Again, we’re moving things in an “x” direction, then a “y” direction using pixels. We can also use negative pixels if we want to move up or to the right:

```
div {

transform: translate(0, 20px);

}
```

This would move the tag 20px further down the page.

You might be thinking “why do this … what’s the point”? Good question! Let’s give a good example. Let’s say we have some images that we want to be slightly transparent by default and then pop up into full view on hover. We can add:

```css
img {

opacity: 0.5;

transform: translate(0, 10px); transition: all 1s;

}

img:hover { opacity: 1;

transform: translate(0, 0);

}
```

Not only does it pop to full opacity on hover, but moves up by 10 pixels too. Nice little effect!

### Combining transforms

We don’t only have the option of picking one transform (e.g. rotate, scale, etc), we can put more than one together. We might want to scale and rotate in some cases:

```css
img {

transform: rotate(5deg) scale(0.9);

}

img:hover {

transform: rotate(-5deg) scale(1);

}
```

### Transform origin

Usually the transforms that you put on a tag will be right in the center of the tag, both horizontally and vertically, but you may want change that. For instance, you may want to rotate around the top left corner rather than the middle.

Alongside the transform rule, we can add the transform-origin rule to our styles:

```css
img {

transform: rotate(5deg); transform-origin: left top;

}
```

This will rotate the image around the top left corner. We can also add pixel units to the transform origin (across then down). Another useful unit to use would be a percentage from the top left corner. Let’s say we want to rotate around 25 percent across and down — we may not know how big the tag is. We can do:

```css
img {

transform: rotate(5deg); transform-origin: 25% 25%;

}
```

A nice thing about translates

Going back to translate for a moment, we can also use percentages for moving a tag around. The percentage is based on the how big the tag is, so for instance if I say move 100 percent to the left, it’s based on the width of the tag and will go one whole tag length across the page.

Why is this useful? One of the things we can do is move a tag so the middle of it is in the usual place of the top left. Most tags expand across and down the page, but we might want to expand from the center of the tag instead. To do this, we can move the tag 50 percent of its width to the left and 50 percent of its height up the page:

```css
img {

transform: translate(-50%, -50%);

}
```

It’s minus 50 percent because we’re moving it back to the top and back to the left of the page, instead of across and down the page. In the next chapter, we’ll talk about why this can be useful for vertically aligning large sections of HTML.

### Vertical Alignment

There are two types of way to vertically align tags, and the best to use really depends on the type of display that your tags has.

### Aligning within text

For “inline” and “inline-block” tags, there’s a pretty straightforward way to do this. There’s a rule in CSS called vertical-align that lets you change how the tag sits within text. For instance, if you want to sit a link to the top of a line of text, if we have bigger tags in that line of text, we can add:

```css
a {

vertical-align: top;

}
```

Other alignments we can use include “middle”, “bottom” and “baseline” (based on where the letters in text sit).

We can also use pixel or percentage units to push the tag up from the baseline:

```css
a {

vertical-align: 10px;

}
```

We can use negative pixels or percentage units to push the tag down from the baseline:

```css
a {

vertical-align: -30%;

}
```

### Aligning with block elements

Unlike with “inline” and “inline-block” tags, “block” tags are a little trickier to align. The problem is that CSS sucks at aligning things down the page, because technically the page shouldn’t know anything about browser size. Of course, we sometimes do want to make things look like they know about the size of the page!

There’s no one right way to do this. You can use margins and paddings to move tags around which works up to a point. You can use positions to move tags too.

One way to move the tag into the middle of the page uses positions and transforms together. We move the top left corner to the center of the page, then move it back across and up the page with a transform:

```css
section.intro { position: absolute; top: 50%;

left: 50%;

transform: translate(-50%, -50%);

}
```

Just using the position absolute (or fixed) to move the tag means the top left corner is right in the middle of the page, not the center of the tag. By using transform we can shift the whole tag upwards by half its height, then across by half its width.