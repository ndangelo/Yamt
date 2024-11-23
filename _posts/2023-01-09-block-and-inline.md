---
id: 58406
title: '10. Block And Inline'
date: '2023-01-09T17:52:56-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=58406'
permalink: /block-and-inline/
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'odin project'
---

The MDN box model article linked in the previous lesson mentions that different display types have subtly different box models. It also mentions that you can change how a box is calculated by changing the `display` property. We will explore the different display values you can use further in this lesson.

### [Lesson Overview](https://www.theodinproject.com/lessons/foundations-block-and-inline#lesson-overview)

This section contains a general overview of topics that you will learn in this lesson.

- You’ll learn about “Normal flow”.
- You’ll learn the difference between `block` and `inline` elements.
- You’ll learn which elements default to `block` and which elements default to `inline`.
- You’ll learn what divs and spans are.

### [Block vs Inline](https://www.theodinproject.com/lessons/foundations-block-and-inline#block-vs-inline)

Most of the elements that you have learned about so far are block elements. In other words, their default style is `display: block`. By default, block elements will appear on the page stacked atop each other, each new element starting on a new line.

Inline elements, however, do not start on a new line. They appear in line with whatever elements they are placed beside. A clear example of an inline element is a link, or `<a>` tag. If you stick one of these in the middle of a paragraph of text, it will behave like a part of the paragraph. ([Like this…](https://www.youtube.com/watch?v=dQw4w9WgXcQ)) The link’s text will sit alongside other words in that paragraph. Additionally, padding and margin behave differently on inline elements. In general, you do not want to try to put extra padding or margin on inline elements.

Inline-block elements behave like inline elements, but with block-style padding and margin. Inline-block is a useful tool to know about, but in practice, you’ll probably end up reaching for flexbox more often if you’re trying to line up a bunch of boxes. Flexbox will be covered in-depth in the next lesson.

### [Divs and Spans](https://www.theodinproject.com/lessons/foundations-block-and-inline#divs-and-spans)

We can’t talk about block and inline elements without discussing divs and spans. All the other HTML elements we have encountered so far give meaning to their content. For example, paragraph elements tell the browser to display the text it contains as a paragraph. Strong elements tell the browser which texts within are important and so on. Yet, divs and spans give no particular meaning to their content. They are just generic boxes that can contain anything.

Having elements like this available to us is a lot more useful than it may first appear. We will often need elements that serve no other purpose than to be “hook” elements. We can give an id or class to target them for styling with CSS. Another use case we will face regularly is grouping related elements under one parent element to correctly position them on the page. Divs and spans provide us with the ability to do this.

Div is a block-level element by default. It is commonly used as a container element to group other elements. Divs allow us to *divide* the page into different blocks and apply styling to those blocks.

See the Pen block-inline-lesson-div-example by TheOdinProject (@TheOdinProjectExamples) on CodePen.

Span is an inline-level element by default. It can be used to group text content and inline HTML elements for styling and should only be used when no other semantic HTML element is appropriate.

See the Pen block-inline-lesson-span-example by TheOdinProject (@TheOdinProjectExamples) on CodePen.

### [Assignment](https://www.theodinproject.com/lessons/foundations-block-and-inline#assignment)

1. The concept of “Normal flow” is implied in the box-model resources, but isn’t laid out very specifically. Read [“Normal Flow” from MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow) to make sure you understand how elements lay themselves out by default.
2. W3 schools’ [“HTML Block and Inline Elements”](https://www.w3schools.com/html/html_blocks.asp) has a description and a list of all the default block and inline elements.
3. The Digital Ocean tutorial [“Inline vs Inline-block Display in CSS”](https://www.digitalocean.com/community/tutorials/css-display-inline-vs-inline-block) has a couple of great examples that clarify the difference between `inline` and `inline-block`.
4. Go to our [CSS exercises repository](https://github.com/TheOdinProject/css-exercises) and do “01-margin-and-padding-1” and “02-margin-and-padding-2” in the `margin-and-padding` directory.

### [Knowledge Check](https://www.theodinproject.com/lessons/foundations-block-and-inline#knowledge-check)