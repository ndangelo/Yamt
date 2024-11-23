---
id: 59694
title: '2. CSS: Units, Connecting HTML + CSS, Typography'
date: '2023-01-14T01:25:35-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=59694'
permalink: /css-units-connecting-html-css-typography/
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'Learn to Code Now'
---

The cascading part of CSS is the idea that you begin to style your site on a general basis, then get more particular as you get into the nitty-gritty. For instance, you might want to make the typeface Arial across the whole site, except for headers where you prefer Georgia.

So it’s always good to keep this in mind. Start off thinking about styling in the most generic way possible. What is the most used color? What is the most used typeface?

How does CSS work?

The first thing we do is similar to how we make HTML files. Instead of having a file that ends in “.html”, we just make one with “.css”. The name doesn’t matter too much, whatever makes sense to you. I like to call my style sheets something like “style.css” so it’s very obvious. You could break your files up into smaller style sheets later on, e.g. “about.css” and “homepage.css”, but it’s personal preference.

The next thing to know is that CSS is not HTML. It looks different because it does a completely different job. It’s not marking up content, it’s describing what content should look like.

There are two main parts to CSS: selectors and rules. The selector picks which part of HTML you want to style, then the rules tell the HTML how to look.

Let’s see an example:

```css
h1 {

font-size: 48px; font-family: Arial;

}
```

The selector in this case is the word “h1” — we’re picking all the &lt;h1&gt; tags across our website. We’re then using an open curly bracket “{“ to start selecting. There are two rules in the style, the first telling the font size to be 48 pixels large and the second telling the typeface to be Arial. We’re then finished with styling so we use a close curly bracket “}” to tell the browser to stop styling.

How rules work is you have a defined list of what you can change about the styling (more on them later), then you add a colon “:” to say do this rule, then give it a particular value depending on the rule. We then finish the rule with a semi-colon “;” to let the browser know we’re done and we can move on to the next rule — think of it like a period or full stop when we finish a sentence. Like this. Or. This.

### Basic CSS selectors

In the previous example, we picked all the &lt;h1&gt; tags on the page by using the CSS selector “h1”. Take a guess at how we’d pick all the &lt;p&gt; paragraph tags on the page? It’s simply “p”.

Here is our CSS picking all the paragraphs on our website and just applying one simple rule to them all, that they should all be 14 pixels font size.

```css
p {

font-size: 14px;

}
```

Take a guess at how we’d pick all the links on the page? Well, we add links to the page with &lt;a&gt; tags, so to style them in CSS, we’d use:

```css
a {

color: red;

}
```

Here I’ve selected every link on the page, then added one rule to make the text color red.

### Body selector

Let’s talk about the cascading part of CSS a little more. We could go through our website and apply styles to every single tag, but that gets a little laborious over time.

Håkon Wien Lie thought it would be better to do things once and then overwrite individually. To make a style apply across the whole website we can write things in the “body” selector.

```css
body {

font-family: Arial; font-size: 16px; color: black;

}
```

This CSS style means that by default, everything in the “body” of our web pages (e.g. the visual content of the page) would get these styles applied to them. Every tag would have the typeface Arial, the font size 16 pixels and the text color black until you overwrite them with another style.

### Multiple and overwriting styles

In our style sheets, we’re very likely to have multiple styles in the same file. The way we do this is just to put them on top of each other:

```css
body {

font-family: Arial; font-size: 16px; color: black;

}

h1 {

font-size: 24px;

}
```

In this example, we have two styles, one for the whole of the page, then one style just for the &lt;h1&gt; tags. To add a third, we can just do it at the bottom of the file.

What typeface will the &lt;h1&gt; tag be? We haven’t explicitly said in the style sheet. The answer is it would be Arial because we said in the stylesheet that all the content should be Arial in the “body” selector. The styles get passed down into all tags until we overwrite them.

What font size would a &lt;p&gt; tag in our HTML be? Well, by default again we said the “body” selector has a size of 16 pixels, so everything in the HTML will be that size until we overwrite it. We have overwritten the default 16px font size in the “h1” selector by making our heading 24 pixels high.

Remember we can put tags inside other tags? What font size would an italic &lt;i&gt; tag inside a &lt;p&gt; paragraph tag be? Same as the paragraph — all the styles get passed down to the tags inside bigger tags.

One more question… if we have the style sheet:

```css
body {

font-size: 16px;

}

p {

font-size: 24px;

}
```

What size would an &lt;i&gt; italic tag be inside a &lt;p&gt; tag be? In this case, the default font size for the page is 16 pixels, but then we overwrite the

&lt;p&gt; paragraph tag and everything inside it to be 24 pixels, so the &lt;i&gt;

tag would be 24 pixel font size too.

### Units

Mostly in this guide, we’ll be using pixel units. A pixel is a single square of color on a screen. Until recently, a pixel was made up of three sub-pixels — one red, one green and one blue. Each of the sub-pixels adds together to make different colors. However, more recently, retina screens have been able to double the amount of sub-pixels both down and across the screen, so on retina screens like the iPhone, there are actually 12 sub-pixels (four red, four green and four blue). There are other types of unit that we’ll be using in the guide.

In CSS, a pixel unit is defined as a number (positive or negative) that ends with “px”:

```
header {

font-size: 16px;

}
```

### Percentages

We can also use percentages in our CSS instead of pixel units. These are mainly useful in layouts:

```css
section {

width: 75%;

}
```

### Em units

An em unit is a size relative to the current font size of that tag. By default, the font size would 16px, so we could use em units instead of px if we’re unsure what pixel size to use but want to make it relative sized:

```css
header {

font-size: 2em;

}
```

By default, that would be twice 16px (32px). However, if we have something inside the header and use em units, it would be now based on 32px sizes:

```css
header h1 {

font-size: 1.5em;

}
```

The pixel size for this &lt;h1&gt; tag would be 1.5 times 32px (not 16px), so 48px large in pixel units.

### Rem units

Similar to em units, rem units are based on the current font size of the page (not the current tag). In the last example, the header size would be

32px if we had “2em” or “2rem”, but the &lt;h1&gt; tag would be 24px if we were to use “1.5rem” instead of “1.5em”

vw, vh, vmin and vmax

We can base our sizes on the “viewport” — essentially the part of our page that the browser can currently see. If our unit is “1vw”, this is 1 percent of the viewport width, so if our browser is 1200px across, 1vw is 12px. “vh” is 1 percentage of the viewport height — so if we can only see 800px of our page in the browser, 1vh is 8px.

Sometimes we might not know how wide or tall our user’s browsers are, so using “vw” and “vh” units can work well. For instance, having a section at exactly the height of the browser could be useful for an intro to the page:

```css
section {

height: 100vh;

}
```

The “vmin” units look at the sizes of “vh” and “vw” and see which one of the two is the smallest. The “vmax” unit does the same, except looking for the larger of “vh” and “vw”.

### Degrees

For some CSS rules, we might use angles, such as in background gradients or rotations. To use degrees we use “deg”. For instance, “5deg” is rotate from the top by 5 degrees clockwise. We can use the opposite direction by making it negative, i.e. “-5deg”.

### Multipliers

Some CSS rules can also take multiplier numbers, such as line heights and scale. This would be just a single number, which might include decimal places. For instance:

```css
body {

line-height: 1.5;

}
```

This means make the line height (or leading), 1.5 times the current font size.

### Connecting HTML + CSS

One set of tags is the content of the page that our users see, such as image tags, paragraph tags and header tags. The other set of tags is to do with any other information. The content tags are put in a &lt;body&gt; tag and the other tags are put in a &lt;head&gt; tag (note: not &lt;header&gt;). Then both of these tags are put inside an &lt;html&gt; tag:

```markup
<html>

<head>

<title>My website</title>

</head>

<body>

<h1>Hey there!</h1>

</body>

</html>
```

The &lt;title&gt; tag lives in the &lt;head&gt; tag. The title isn’t included within the page’s content, but you’ll see the phrase “My website” in your browser tab and for your page’s headline in Google results.

To link up our HTML file with our CSS file, one more tag needs to be a &lt;head&gt; tag because it’s not part of our content. If our CSS file is called “style.css”, we need to add a &lt;link&gt; tag:

```markup
<html>

<head>

<title>My website</title>

<link rel="stylesheet" href="style.css">

</head>

<body>

<h1>Hey there!</h1>

</body>

</html>

We can add multiple stylesheets on the same page by adding another

<link> tag:

<html>

<head>

<title>My website</title>

<link rel="stylesheet" href="style.css">

<link rel="stylesheet" href="slideshow.css">

</head>

<body>

<h1>Hey there!</h1>

</body>

</html>
```

The order of the stylesheet is only important if you’re overwriting styles in more than one file — the bottom file will be the one that overwrites styles in the top one.

For now, most of the tags we’ll use will be within the body tag of our page.

### Typography

Now we know how to use some basic styles, let’s show some of the CSS rules for typography and how you use them.

### Font sizing

We talked about this earlier but we use:

```css
p {

font-size: 16px;

}
```

to give the font a particular size. Notice there’s no space between the number and the “px” — it’s all one word.

### Font weight and how to make fonts bold

To make a font bold, we give it a font weight:

```css
p {

font-weight: 700;

}
```

This number correlates to a typographic weight. There are essentially nine weights to pick from:

<figure class="wp-block-table">| 100 | thin |
|---|---|
| 200 | extra light |
| 300 | light |
| 400 | regular |
| 500 | medium |
| 600 | semi bold |
| 700 | bold |
| 800 | extra bold |
| 900 | black |

</figure>The default font weight is 400. Watch out, as not all typefaces have all the weights. If that is the case, your text will default to the nearest weight it can find (e.g. if there are only 400 and 700 weights and you select 900, it’ll display as 700).

### Typography and text

To change the typeface of the site, you can change the font’s family:

```css
p {

font-family: Arial;

}
```

By default, there are not many fonts to pick from, just the standard ones such as Arial, Georgia, Helvetica and Times New Roman. We’ll talk later about how to add web fonts into your site.

### Make the font italic

To make the font italic:

```css
p {

font-style: italic;

}
```

To overwrite an italic font and make it normal again:

```
p {

font-style: normal;

}
```

### Leading or line heights

To change the ratio between the height of the lines between text, we change the line height:

```
p {

line-height: 1.5;

}
```

The number is a ratio based on the font size, so for instance if the font size is 16 pixels, the space between each line would be 24 pixels (16 times 1.5). A tight leading would be around 1.2 and a looser leading would be around 1.6.

You can also use pixel sizes for this:

```css
p {

line-height: 24px;

}
```

But it’s better to use ratios as you may change the font size later on.

### Letter spacing or tracking

To change the distance between characters in text, we can change the letter spacing. To increase the spacing by one pixel per character, we can add:

To reduce the space, we can use negative pixels:

```css
p {

letter-spacing: -1px;

}
```

### Aligning text

When it comes to aligning text, you’re not really handling the typography but how the text works, so the rules look slightly different:

```css
p {

text-align: left;

}
```

There are four different values you can put in: left, center, right and justify.

Underlining text and removing underlines

You might want to add underlines to your code:

```css
p {

text-decoration: underline;

}
```

You may notice that by default links have underlines, if you want to get rid of them, add:

```css
a {

text-decoration: none;

}
```

### MAKING TEXT SHOUT

Sometimes you need to make your text shout out! We could just go back to our HTML and delete the content and replace with an upper case version, but there’s no need to rewrite your HTML. Having upper case letters could be a branding style and therefore we could do it in CSS.

You can make all the letters upper case by adding:

```css
p {

text-transform: uppercase;

}
```

You could also make each first letter capitalized too:

```css
p {

text-transform: capitalize;

}
```

Putting them all together

Remember you can add several of these rules together in one style or across multiple styles:

```css
p {

font-family: Arial; font-weight: 900; font-size: 16px; line-height: 1.5; text-align: center;

}
```

The order of the rules doesn’t matter as long as you don’t include two of the same rule. If you do, the latter one will take effect. For example:

```css
p {

font-size: 14px; font-size: 16px;

}
```

The font size will be 16 pixels as the first one gets overwritten by the second.

</body></html>