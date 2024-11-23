---
id: 59609
title: '3. Let&#8217;s Talk HTML, Heading, Blocks and inline, Links, Images, White space + indentation'
date: '2023-01-13T13:30:01-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=59609'
permalink: /lets-talk-html/
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'Learn to Code Now'
---

Why talk about HTML first? Well, we need to have **some content which we can style and interact with.**

HTML stands for **HyperText Markup Language**.

Remember, the user doesn’t see the actual code that the author writes. The user sees the final version of the website — the browser turns the HTML code into a web page, just like Spotify turns a music data file into an audio of Smashmouth’s All Star.

The first thing we’d do is create a new file and name it something related to the page, then with the HTML extension. For example, about.html is a good file name for the about page on a website. We then open it and start writing our content.

“Isn’t this scientific document cool?”

We would start the sentence with a paragraph open tag, then finish it with a paragraph closing tag:

```css
<p>Isn’t this scientific document cool?</p>
```

Notice the slight difference between the two tags. The open tag doesn’t have a slash in it and the closing tag does. When we have a slash in a tag, it means stop doing this tag now.

The name of the tag is a “p” tag — the p standing for paragraph. Tim liked to use shorter names for two reasons — it’s easier to write and back in the 80s the Internet was a lot slower, so the less text the less time the page took to load.

There are around 100 types of HTML tags but on a day to day basis, most coders only use around 15 to 20 of them. Paragraph tags (&lt;p&gt;) are among the most common.

Tags can also be reused too. There’s a high probability that there’s more than one tag on your page, so to “mark up” or describe the text, we can just use another &lt;p&gt; tag.

```markup
<p>Isn’t this scientific document cool?</p>

<p>I just discovered how to make lead into gold. I thought that wasn’t possible?</p>
```

Oh hi, I’m a heading

Of course, not everything is a paragraph. On any document, you’re likely to have titles and sub-titles. Just like at the top of this section, where there’s a heading saying hi to you.

As with paragraphs, we have to mark up our text with which bits are headings and sub-headings, and as with any document there’s a hierarchy to our headings and titles.

We start with the main headings and work our way down to sub-headings and sub-sub-headings.

Let’s take a résumé. The main heading on the page would be your name e.g. Rik Lomas. You’d then have sub-headings such as Education,

Experience and References. Then within each of those you’d have sub-sub-headings, so in Experience, you might have company names (e.g. SuperHi, Steer etc).

In HTML, there are tags to reflect these headings, sub-headings and sub-sub-headings (down to sub-sub-sub-sub-sub-headings!).

Your main heading would be a &lt;h1&gt; tag.

```markup
<h1>Rik Lomas</h1>
```

Your sub-heading would be a &lt;h2&gt; tag.

```markup
<h2>Education</h2>
```

Your sub-sub-heading would be a &lt;h3&gt; tag.

```markup
<h3>SuperHi Inc.</h3>
```

There are even &lt;h4&gt;, &lt;h5&gt; and &lt;h6&gt; tags too. Notice that it’s not just in descending number, it’s text of an equal importance. For instance, I might have a tag &lt;h3&gt; above another &lt;h2&gt;. I can continue to use paragraphs above and below my headings too.

```markup
<h1>Rik Lomas</h1>

<h2>Experience</h2>

<h3>SuperHi Inc</h3>

<p>I was the founder and coder for SuperHi...</p>
```

So very quickly, we’ve covered six more tags, taking our total to seven. Remember, we said that most professional coders only use 15 to 20 tags, so we’re 30 to 40 percent through all the tags you might ever need to make websites.

**index.html**

We talked earlier about naming our HTML files after the page they represent. An “about” page would be named “about.html”, a “contact” page would be named “contact.html” or “contact-us.html” (remember you can’t use spaces in file names).

There is a special name however for the first page you expect your user to visit. We’d call it the home page, but its file name is “index.html”.

### Blocks and inline

All the tags we’ve talked about so far are kind of bigger boxes of content. Visually they’d go across the whole page and the next tag would go below them. Your header is at the top, then a paragraph below, then another paragraph below that.

These tags are called block tags because they fill the width of the page and make the next tag go beneath them.

Most tags are block tags, but there are other tags where you don’t want to fill up the whole width of the page. For example, you might just want to highlight one or two words in a paragraph.

There are a few tags that can work within a line of text, these are called inline tags.

An example is a bold tag, the &lt;b&gt; tag. You might only want to highlight one or two words in the paragraph.

```markup
<p>At my last job, conversions improved by <b>over 50%</b> in just 4 months.</p>
```

To paraphrase Xzibit in Pimp My Ride: I heard you liked tags so I put tags inside your tags. We’ll be putting more tags inside other tags later.

Other inline tags include for italics (&lt;i&gt;) and to underline something (&lt;u&gt;). In this paragraph, we’re having “over 50%” as italic and “just 4” as underline. That’s a &lt;p&gt; tag with two different tags inside.

Block tags and inline tags

### BLOCK INLINE

```markup
<p>At my last job, conversions improved by <i>over 50%</i> in <u>just 4</u> months.</p>
```

One thing to note is that an inline tag could go to multiple lines of text

— for instance in the previous example, the word “over” could be the last word of the first line and the “50%” could be the first word of the second line.

A good rule of thumb is that block tags go down the page and inline tags go across the page.

### Links

One important tag that made the web successful was the ability to link one page to another, so users could click between the pages of not only one author’s website but to other author’s sites. The original idea came from scholarly referencing and footnotes, but it massively helped the discoverability of other people’s websites.

A link tag in HTML is called the &lt;a&gt; tag — the “a” stands for anchor because it might link to another site, another page or another section within the page so it doesn’t always go away from the same place.

Just like the bold, italic and underline tags, a link tag is an inline tag, as you could just link one word in a paragraph to somewhere else.

The link is a little more complex than the other tags we’ve covered. We need to introduce a new part of HTML called attributes.

### Attributes

Let’s give an example of a link tag.

```markup
<a>Go to Facebook</a>
```

This is some text that says “Go to Facebook” and is surrounded by the

&lt;a&gt; link tags at the start and end. But if a user clicks the link, where should they go to? Should they go to the Facebook.com homepage? Should they go to the Wikipedia entry on Facebook? Should they go to the Google Finance page for Facebook’s stock price? It depends.

We need to give this some more information.

We don’t want to write out the URL for where the link is going to in the text, otherwise our user will see an ugly URL when they just want the words “Go to Facebook”.

To add this extra information, we need to add in an HTML attribute — an extra bit of information for this tag. To do this, we are going to add a special HTML attribute to the link called the “href” attribute (short for hypertext reference).

```markup
<a href="http://www.facebook.com/" rel="noreferrer noopener" target="_blank"><a href="</a>http://www.facebook.com">Go to Facebook</a>
```

The way we add attributes is to add them to opening tags in HTML. We add a space after the name of the tag (e.g. “a”, “h1”), then the name of attribute (e.g. “href”) with an equals symbol, then something in quotation marks.

There are more attributes that we’ll talk about later, but for now we’ll only be using the “href” attribute on link tags.

### Different types of links

The link above goes to a different website completely. These links are called “absolute” links — basically something that isn’t on your own site.

You can write the href attribute as a “relative” link if you’re linking to another page on your own website.

```markup
<a href="about.html">About page</a>
```

Notice you don’t need the full URL, just the name of the file on your site.

Other links — email me…

You don’t have to link to other HTML pages on a link. You can do other actions such as pop open a new email compose box.

```markup
<a href="mailto:rik@superhi.com" rel="noreferrer noopener" target="_blank"><a href="</a>mailto:rik@superhi.com">Email me!</a>
```

Notice this href attribute starts with “mailto:” then the email address of where you want to send it.

### Joining everything together

So we’ve covered paragraphs, titles, sub-titles, inline tags and links. We can combine them all together to get something like this.

```markup
<h1>Rik Lomas</h1>

<h2>Experience</h2>

<h3>SuperHi Inc</h3>

<p>I worked at <a href="https://www.superhi.com"> SuperHi</a> from 2014-2017.</p>

<p>When I was there, I helped increase profits by

<b>30%</b> over the course of those years</p>

<p>You can <a href="about.html">contact me here</a>.</p>
```

### Images

How to use the &lt;img&gt; tag

Most tags have an open and a close tag. Images just have one open tag and no close tag.

```markup
<img src="cat.jpg">
```

No close tag there and a brand new attribute called “src”.

You can use multiple images together and put them inside other tags too.

```markup
<p>

<img src="cat.jpg">

<img src="dog.jpg">

</p>
```

To put in two images inside a paragraph, one with a cat image and another with a dog image.

Note these “src” attributes are using “relative” sources, just like in the link tags being able to use “about.html”. You can also use “absolute” sources too.

```markup
<a href="http://i.imgur.com/5J5vJm8.jpg" rel="noreferrer noopener" target="_blank"><img src="</a>https://www.esu.edu">
```

### Image file types

There are only a few types of image file that we can use on the web. Certain image types are good for certain jobs. The file types are:

<figure class="wp-block-table">| .jpg | JPG files are great for photographs and detailed color imagery. |
|---|---|
| .gif | Are they called “giffs” or “jiffs”? Who knows… but GIF files are good for animated images. |
| .png | PNG files are good for flatter color images and if you have any transparency in your image. |
| .svg | SVG stands for scalable vector graphics which means they don’t pixelate when really large. Great for icons and logos. |

</figure>### White space + indentation

We mentioned earlier that HTML is all about content and CSS is all about style. Because of this, HTML doesn’t really care about how your code looks, it will ignore any white space you put in your code and make it look “normal”.

For instance, this code…

```markup
<p>Hi there, Rik!</p>

...would look exactly the same as...

<p> Hi there, Rik!</p>
```

HTML ignores all the spacing and treats it as if it’s one sentence. If we want to control how the website looks, we need to use CSS.

### Indentation

As HTML doesn’t care about gaps, it means we can make our code cleaner to read so that when we come back to it in a few months, or if we’re working with another coder, it can make more sense.

For instance, this is hard to read:

```markup
<p><a href="about.html">About</a></p>
```

So to make it easier, I would write it like:

```markup
<p>

<a href="about.html">About</a>

</p>
```

Notice that not only have I put the &lt;a&gt; tag with some space above and below, but I’ve also indented the code so it goes into the page a little. I do this by pressing the tab key to push it further in.

This is just my personal preference. There’s no right and wrong way to do HTML — both ways would look the same to a user.

Indentation is a powerful tool when you start getting more complex code.

One more example to make it more apparent. We could have code like this:

```markup
<p><a href=”about.html”>About</a> 

<a href=”blog.html”> Blog</a> 

<a href=”contact.html”>Contact</a></p>
```

Simply one paragraph with three one-word links. We can clean it up like this:

```markup
<p>

<a href="about.html">About</a>

<a href="blog.html">Blog</a>

<a href="contact.html">Contact</a>

</p>
```

All I’ve done is separate the links onto different lines, then indent (or tab) the contents of the paragraph. Nice, clean and looks the same.