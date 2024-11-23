---
id: 17042
title: 'AN IN-DEPTH INTRODUCTION TO HTML &#038; CSS'
date: '2018-04-23T18:46:43-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=17042'
permalink: '/?p=17042'
amazonS3_cache:
    - 'a:2:{s:66:"//www.nuggetofjoy.com/wp-content/uploads/Introduction-HTML-CSS.jpg";a:2:{s:2:"id";s:5:"17044";s:11:"source_type";s:13:"media-library";}s:95:"//image-control-storage.s3.amazonaws.com/blog-images/2018/04/23184645/Introduction-HTML-CSS.jpg";a:2:{s:2:"id";s:5:"17044";s:11:"source_type";s:13:"media-library";}}'
categories:
    - 'Design Instruction'
---

<header class="entry-header">
</header><div class="entry-content">![Want to learn the basics of HTML & CSS? Here is an in deoth introduction and a tutorial to create your own web page as well!](https://image-control-storage.s3.amazonaws.com/blog-images/2018/04/23184645/Introduction-HTML-CSS.jpg)

If you are living in the modern day computer world, your second best friend is probably – let me guess – Google, right? Just kidding! But I am sure you have an online presence of some kind – a social media account, a personal blog or maybe even a business!

We spend hours online – reading blogs, watching videos, scrolling through Pinterest, you name it! Ever wondered what goes on behind the scenes of those websites you browse? Today’s post gives you a brief introduction on how these websites are created and how to make them look beautiful!

Every website that you visit usually consists of multiple web pages. Every web page is made up of three layers – **Content Layer, Presentation Layer and Behavior Layer** – that work together to create a specific user experience. HTML handles the content layer of the web page, CSS provides for the presentation layer and the behavior layer is handled by Javascript!

![Want to learn the basics of HTML & CSS? Here is an in depth introduction and a tutorial to create your own web page as well!]()

Even if you do not build websites, knowing the basics of **HTML** and **CSS** is an incredibly useful skill to have in today’s internet world. So if you are intimidated by the technical jargon, code etc., don’t worry. We will dig into the fundamentals of HTML and CSS and understand how they work together. We will also build our own web page! Excited? Let’s go!

## WHAT IS HTML?

HTML stands for **H**yper**T**ext **M**arkup **L**anguage. Just as we, humans, use languages to communicate with each other, HTML is a language of the internet! Web browsers like Google Chrome read and interpret HTML to render the information you request for on the web.

HTML is essentially the building block of every website. It defines the structure of every web page and its content.

## Common HTML terms:

While getting started with HTML, it’s important to understand a few common terms associated with the language:

**Elements:** These are designators that define the order and structure of the content within a web page. &lt;span&gt; , &lt;p&gt; , &lt;div&gt;, &lt;h1&gt;, &lt;title&gt; etc. are all examples of basic HTML elements. Each HTML element is enclosed within a start and end tag as shown below.

**Element:** &lt;div&gt; … &lt;/div&gt;

**Tags:** The use of angle brackets around an HTML element creates what’s called an HTML tag. HTML tags most often occur in pairs of start and end tags.

A start tag indicates the beginning of an HTML element and looks like this:

**Start Tag: &lt;span&gt;**

An end tag indicates the end of an HTML element and consists of a forward slash as shown below:

**End Tag: &lt;/span&gt;**

**Attributes:** We use attributes to provide additional information about an HTML element. Some common attributes include id, class, src and href. Attributes are defined within the start tag of an element after its name. Each attribute is defined by a name and a value. For example, the <a>element below includes a href attribute as shown below:</a>

**&lt;a href=“[http://www.google.com](http://www.google.com/)”&gt; Google Search Engine &lt;/a&gt;**

## WHAT IS CSS?

CSS stands for Cascading Style Sheets. CSS defines the visual style and appearance of the web pages. So if you see italicized text or a background image on a web page, it is CSS that is doing the trick!

**Common CSS terms:**

Here are some of the common CSS terms that are useful to know:

a {  
color: #484848;  
font-size: 14px;  
font-weight: 300px;  
}

**Selectors:** A selector designates the exact HTML elements to target for styling. Selector generally targets all HTML elements of one type directly or a specific instance of an element, identified by an attribute such as id or class. The styles to be applied to the targeted element are enclosed within curly brackets following the selectors. For example, the selector in the above code is targeting all the <a>elements.</a>

**Properties:** A property determines the styles that will be applied to an HTML element. There are several properties that are available for use. Some of the common properties are font, background-color, size and color. In the example above, we are using the color, font-size and font-weight properties to style the <a>element.</a>

**Values:** Each property has a value associated with it. The value defines the behavior of the property. For example, the value 14px defines the behavior of the font-size property.

## What is the difference between HTML &amp; CSS?

Even though very often HTML &amp; CSS are used together in the same context, they are far from being the same. While HTML defines the structure of the web page, CSS defines the style and appearance.

To make this easier to understand, let’s compare a website to a house. HTML is like the bricks that make up the house while CSS is the paint and decor that makes the house presentable and beautiful.

A webpage can exist without CSS, but never without HTML.

## Develop a simple web page using HTML &amp; CSS

Now on to the exciting part, let’s build our own web page. It is a super simple and fun activity!

You will need:

A Text Editor to write the code for your web page. Some of my favorite code editors are [Sublime Text](http://www.sublimetext.com/), [Notepad++](https://notepad-plus-plus.org/), [Brackets](http://brackets.io/).

A Web Browser to view your web page. Anything from Google Chrome to internet explorer will do.

**3 – steps to creating your own web page:**

**Step 1:** Create a folder in your documents and name it, I am going with MyWebPage1.0 for mine.

**Step 2:** Create a text file inside the folder and paste the following HTML code in it. Name it as Webpage.html and save as an HTML file type.

<div class="gist" id="gist26600926"><div class="gist-file"><div class="gist-data"><div class="js-gist-file-update-container js-task-list-container file-box"><div class="file" id="file-webpage-html"><div class="blob-wrapper data type-html">|  | &lt;!DOCTYPE html&gt; |
|---|---|
|  | &lt;<span class="pl-ent">html</span> <span class="pl-e">lang</span>=<span class="pl-s"><span class="pl-pds">“</span>en<span class="pl-pds">“</span></span>&gt; |
|  | &lt;<span class="pl-ent">head</span>&gt; |
|  | &lt;<span class="pl-ent">meta</span> <span class="pl-e">charset</span>=<span class="pl-s"><span class="pl-pds">“</span>utf-8<span class="pl-pds">“</span></span>&gt; |
|  | &lt;<span class="pl-ent">title</span>&gt;My First Web Page&lt;/<span class="pl-ent">title</span>&gt; |
|  | &lt;<span class="pl-ent">link</span> <span class="pl-e">rel</span>=<span class="pl-s"><span class="pl-pds">“</span>stylesheet<span class="pl-pds">“</span></span> <span class="pl-e">href</span>=<span class="pl-s"><span class="pl-pds">“</span>style.css<span class="pl-pds">“</span></span>&gt; |
|  | &lt;/<span class="pl-ent">head</span>&gt; |
|  | &lt;<span class="pl-ent">body</span>&gt; |
|  | &lt;<span class="pl-ent">h1</span>&gt; Coding is so much fun!&lt;/<span class="pl-ent">h1</span>&gt; |
|  | &lt;<span class="pl-ent">p</span>&gt; The best way to learn coding is to explore and experiment with the different styles, attributes and tags. Have fun with it!&lt;/<span class="pl-ent">p</span>&gt; |
|  | &lt;/<span class="pl-ent">body</span>&gt; |
|  | &lt;/<span class="pl-ent">html</span>&gt; |

</div></div></div></div><div class="gist-meta">[view raw](https://gist.github.com/Chaitra7/86784b6f5b01c6b327d2/raw/7b80d204b1153ac28f5ee18276677ea9a1ec0ceb/Webpage.html)[Webpage.html](https://gist.github.com/Chaitra7/86784b6f5b01c6b327d2#file-webpage-html) hosted with ❤ by [GitHub](https://github.com/)</div></div></div>**Step 3:** Next, create another text file inside the folder and paste the following CSS code in it. Name it as style.css and save it as a CSS file type.

<div class="gist" id="gist26601027"><div class="gist-file"><div class="gist-data"><div class="js-gist-file-update-container js-task-list-container file-box"><div class="file" id="file-style-css"><div class="blob-wrapper data type-css">|  | <span class="pl-c">/\* This is the css code for styling the HTML page \*/</span> |
|---|---|
|  |  |
|  | <span class="pl-ent">html</span>, <span class="pl-ent">body</span>, <span class="pl-ent">div</span>, <span class="pl-ent">span</span>{ |
|  | <span class="pl-c1">margin</span>: <span class="pl-c1">0</span>; |
|  | <span class="pl-c1">padding</span>: <span class="pl-c1">0</span>; |
|  | <span class="pl-c1">border</span>: <span class="pl-c1">0</span>; |
|  | <span class="pl-c1">font</span>: <span class="pl-c1">inherit</span>; |
|  | <span class="pl-c1">vertical-align</span>: <span class="pl-c1">baseline</span>; |
|  | } |
|  |  |
|  | <span class="pl-ent">body</span>{ |
|  | <span class="pl-c1">background-color</span>: <span class="pl-c1">\#f6f6f6</span>; |
|  | <span class="pl-c1">font-size</span>:<span class="pl-c1">14<span class="pl-k">px</span></span>; |
|  | } |
|  |  |
|  | <span class="pl-ent">h1</span>{ |
|  | <span class="pl-c1">color</span>: <span class="pl-c1">\#f6a2a2</span>; |
|  | <span class="pl-c1">font-family</span>: <span class="pl-c1">Georgia</span>, <span class="pl-c1">sans-serif</span>; |
|  | <span class="pl-c1">font-size</span>:<span class="pl-c1">34<span class="pl-k">px</span></span>; |
|  | <span class="pl-c1">font-weight</span>: <span class="pl-c1">bold</span>; |
|  | <span class="pl-c1">text-align</span>: <span class="pl-c1">center</span>; |
|  | <span class="pl-c1">letter-spacing</span>: <span class="pl-c1">3<span class="pl-k">px</span></span>; |
|  | <span class="pl-c1">padding</span>: <span class="pl-c1">50<span class="pl-k">px</span></span>; |
|  | <span class="pl-c1">text-transform</span>:<span class="pl-c1">uppercase</span>; |
|  | } |
|  |  |
|  | <span class="pl-ent">p</span>{ |
|  | <span class="pl-c1">text-align</span>: <span class="pl-c1">center</span>; |
|  | <span class="pl-c1">font-family</span>: <span class="pl-c1">Times</span> new roman, <span class="pl-c1">sans-serif</span>; |
|  | <span class="pl-c1">font-size</span>:<span class="pl-c1">22<span class="pl-k">px</span></span>; |
|  | <span class="pl-c1">letter-spacing</span>: <span class="pl-c1">1<span class="pl-k">px</span></span>; |
|  | <span class="pl-c1">font-style</span>:<span class="pl-c1">italic</span>; |
|  | } |
|  |  |
|  | <span class="pl-ent">a</span>{ |
|  | <span class="pl-c1">color</span>: <span class="pl-c1">\#e4d51e</span>; |
|  | } |

</div></div></div></div><div class="gist-meta">[view raw](https://gist.github.com/Chaitra7/a8c645aaf26f7a96c92f/raw/87be0dc16100abea6b41e253fa57ba4d015ac52f/style.css)[style.css](https://gist.github.com/Chaitra7/a8c645aaf26f7a96c92f#file-style-css) hosted with ❤ by [GitHub](https://github.com/)</div></div></div>That’s it, now double click on your HTML file to run it on your web browser. Here’s a screenshot of the webpage you can expect to see on your browser.

![Want to learn the basics of HTML & CSS? Here is an in depth introduction and a tutorial to create your own web page as well!](https://s3.amazonaws.com/image-control-storage/blog-images/2018/07/18141327/download-1-1024x40511111111111111111111111111111111111111111111111111111111111111121111111111111111111111111111111121111111111111111111111111111111111111111.png)

There you go, you’ve created your first web page! Feel free to play around by changing the HTML and CSS code to alter your web page. The best way to learn HTML and CSS is to really just experiment and have fun exploring the various possibilities that they offer.

</div>