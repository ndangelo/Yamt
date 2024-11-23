---
id: 59674
title: 'The CSS Box Model: Block And Inline/Divs and Spans'
date: '2023-01-14T00:31:49-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=59674'
permalink: /the-box-model-block-and-inline-divs-and-spans/
amazonS3_cache:
    - 'a:14:{s:54:"//www.nuggetofjoy.com/wp-content/uploads/boxes-3-3.png";a:2:{s:2:"id";s:5:"59358";s:11:"source_type";s:13:"media-library";}s:71:"//image-control-storage.s3.amazonaws.com/2023/01/12170537/boxes-3-3.png";a:2:{s:2:"id";s:5:"59358";s:11:"source_type";s:13:"media-library";}s:59:"//www.nuggetofjoy.com/wp-content/uploads/odin-lined-1-3.png";a:2:{s:2:"id";s:5:"59360";s:11:"source_type";s:13:"media-library";}s:76:"//image-control-storage.s3.amazonaws.com/2023/01/12170538/odin-lined-1-3.png";a:2:{s:2:"id";s:5:"59360";s:11:"source_type";s:13:"media-library";}s:58:"//www.nuggetofjoy.com/wp-content/uploads/box-model-1-3.png";a:2:{s:2:"id";s:5:"59361";s:11:"source_type";s:13:"media-library";}s:75:"//image-control-storage.s3.amazonaws.com/2023/01/12170541/box-model-1-3.png";a:2:{s:2:"id";s:5:"59361";s:11:"source_type";s:13:"media-library";}s:58:"//www.nuggetofjoy.com/wp-content/uploads/box-model-1-4.png";a:2:{s:2:"id";s:5:"60289";s:11:"source_type";s:13:"media-library";}s:75:"//image-control-storage.s3.amazonaws.com/2023/01/01181137/box-model-1-4.png";a:2:{s:2:"id";s:5:"60289";s:11:"source_type";s:13:"media-library";}s:63:"//www.nuggetofjoy.com/wp-content/uploads/standard-box-model.png";a:2:{s:2:"id";s:5:"60290";s:11:"source_type";s:13:"media-library";}s:80:"//image-control-storage.s3.amazonaws.com/2023/01/01181138/standard-box-model.png";a:2:{s:2:"id";s:5:"60290";s:11:"source_type";s:13:"media-library";}s:64:"//www.nuggetofjoy.com/wp-content/uploads/alternate-box-model.png";a:2:{s:2:"id";s:5:"60291";s:11:"source_type";s:13:"media-library";}s:81:"//image-control-storage.s3.amazonaws.com/2023/01/01181139/alternate-box-model.png";a:2:{s:2:"id";s:5:"60291";s:11:"source_type";s:13:"media-library";}s:63:"//www.nuggetofjoy.com/wp-content/uploads/box-model-devtools.png";a:2:{s:2:"id";s:5:"60292";s:11:"source_type";s:13:"media-library";}s:80:"//image-control-storage.s3.amazonaws.com/2023/01/01181140/box-model-devtools.png";a:2:{s:2:"id";s:5:"60292";s:11:"source_type";s:13:"media-library";}}'
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'Learn to Code Now'
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

Now that you understand the basic syntax of HTML and CSS, we’re going to get serious. The most important skills you need to master with CSS are *positioning* and *layout*. Changing fonts and colors is a crucial skill, but being able to put things exactly where you want them on a webpage is even more crucial. After all, how many webpages can you find where absolutely every element is just stacked one on top of another?

Learning to position elements on a webpage is not that difficult once you understand just a few key concepts. Unfortunately, many learners race through learning HTML and CSS to get to JavaScript and end up missing these fundamental concepts. This leads to frustration, pain, ([and funny gifs](https://giphy.com/gifs/css-13FrpeVH09Zrb2)) because all the JavaScript skills in the world are meaningless if you can’t stick your elements on the page where you need them to be. So with that in mind, let’s get started.

### [Lesson Overview](https://www.theodinproject.com/lessons/foundations-the-box-model#lesson-overview)

This section contains a general overview of topics that you will learn in this lesson.

- You’ll learn all about *the box model*.
- You’ll learn how to make sure elements are just the right size with `margin`, `padding`, and `borders`

### [The Box Model](https://www.theodinproject.com/lessons/foundations-the-box-model#the-box-model)

The first important concept that you need to understand to be successful in CSS is the box model. It isn’t complicated, but skipping over it now will cause you much frustration down the line.

Every single thing on a webpage is a rectangular box. These boxes can have other boxes in them and can sit alongside one another. You can get a rough idea of how this works by sticking a border on every item on the page like this:

```
* {
  border: 2px solid red;
}

```

<figure class="wp-block-image">[![boxes](https://image-control-storage.s3.amazonaws.com/2023/01/12170537/boxes-3-3.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/main/foundations/html_css/the-box-model/imgs/boxes.png)</figure>You can use the browser’s inspector to add the CSS above to this web page if you want. Boxes in boxes!

<figure class="wp-block-image">[![lines](https://image-control-storage.s3.amazonaws.com/2023/01/12170538/odin-lined-1-3.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/main/foundations/html_css/the-box-model/imgs/odin-lined.png)</figure>OK, so there might be some circles in the above image… but when it comes to layout, they fit together like rectangular boxes and not circles. In the end, laying out a webpage and positioning all its elements is deciding how you are going to nest and stack these boxes.

The only real complication here is that there are many ways to manipulate the size of these boxes, and the space between them, using `padding`, `margin`, and `border`. The assigned articles go into more depth on this concept, but to sum it up briefly:

- `padding` increases the space between the edge of a box and the content inside of it.
- `margin` increases the space between a box and any others that sit next to it.
- `border` adds space (even if it’s only a pixel or two) between the margin and the padding.

Be sure to study the diagrams carefully.

<figure class="wp-block-image">[![the box model](https://image-control-storage.s3.amazonaws.com/2023/01/12170541/box-model-1-3.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/main/foundations/html_css/the-box-model/imgs/box-model.png)</figure><figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-16-9 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper"><iframe allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen="" frameborder="0" height="281" loading="lazy" referrerpolicy="strict-origin-when-cross-origin" src="https://www.youtube.com/embed/rIO5326FgPE?feature=oembed" title="Learn CSS Box Model In 8 Minutes" width="500"></iframe></div></figure>### [Assignment](https://www.theodinproject.com/lessons/foundations-the-box-model#assignment)

1. [This video](https://www.youtube.com/watch?v=rIO5326FgPE) is a straightforward overview of the box model, padding and margin. Go ahead and watch this now; it informs everything else.
2. Because the box model concept is so incredibly fundamental, check out [this lesson from MDN](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model). It covers the same material as the video above, but it goes a little further in-depth. Pay close attention to the examples and take the time to experiment with their in-browser editor!
3. [This CSS Tricks page](https://css-tricks.com/almanac/properties/m/margin/) has some further information about the `margin` property that you’ll find useful. Specifically, the sections about `auto` and margin collapsing contain things you’ll want to know.

# The box model

Everything in CSS has a box around it, and understanding these boxes is key to being able to create more complex layouts with CSS, or to align items with other items. In this lesson, we will take a look at the CSS *Box Model*. You’ll get an understanding of how it works and the terminology that relates to it.

## [Block and inline boxes](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#block_and_inline_boxes)

In CSS we have several types of boxes that generally fit into the categories of **block boxes** and **inline boxes**. The type refers to how the box behaves in terms of page flow and in relation to other boxes on the page. Boxes have an **inner display type** and an **outer display type**.

In general, you can set various values for the display type using the [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display) property, which can have various values.

## [Outer display type](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#outer_display_type)

If a box has an outer display type of `block`, then:

- The box will break onto a new line.
- The [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width) and [`height`](https://developer.mozilla.org/en-US/docs/Web/CSS/height) properties are respected.
- Padding, margin and border will cause other elements to be pushed away from the box.
- If [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width) is not specified, the box will extend in the inline direction to fill the space available in its container. In most cases, the box will become as wide as its container, filling up 100% of the space available.

Some HTML elements, such as `<h1>` and `<p>`, use `block` as their outer display type by default.

If a box has an outer display type of `inline`, then:

- The box will not break onto a new line.
- The [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width) and [`height`](https://developer.mozilla.org/en-US/docs/Web/CSS/height) properties will not apply.
- Vertical padding, margins, and borders will apply but will not cause other inline boxes to move away from the box.
- Horizontal padding, margins, and borders will apply and will cause other inline boxes to move away from the box.

Some HTML elements, such as `<a>`, `<span>`, `<em>` and `<strong>` use `inline` as their outer display type by default.

## [Inner display type](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#inner_display_type)

Boxes also have an *inner* display type, which dictates how elements inside that box are laid out.

Block and inline layout is the default way things behave on the web. By default and without any other instruction, the elements inside a box are also laid out in **[normal flow](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Normal_Flow)** and behave as block or inline boxes.

You can change the inner display type for example by setting `display: flex;`. The element will still use the outer display type `block` but this changes the inner display type to `flex`. Any direct children of this box will become flex items and behave according to the [Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) specification.

When you move on to learn about CSS Layout in more detail, you will encounter [`flex`](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox), and various other inner values that your boxes can have, for example [`grid`](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grids).

**Note:** To read more about the values of display, and how boxes work in block and inline layout, take a look at the MDN guide [Block and Inline Layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flow_Layout/Block_and_Inline_Layout_in_Normal_Flow).

## [Examples of different display types](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#examples_of_different_display_types)

The example below has three different HTML elements, all of which have an outer display type of `block`.

- A paragraph with a border added in CSS. The browser renders this as a block box. The paragraph starts on a new line and extends the entire available width.
- A list, which is laid out using `display: flex`. This establishes flex layout for the children of the container, which are flex items. The list itself is a block box and — like the paragraph — expands to the full container width and breaks onto a new line.
- A block-level paragraph, inside which are two `<span>` elements. These elements would normally be `inline`, however, one of the elements has a class of “block” which gets set to `display: block`.

<figure class="wp-block-embed"><div class="wp-block-embed__wrapper">https://mdn.github.io/css-examples/learn/box-model/block.html </div></figure>In the next example, we can see how `inline` elements behave.

- The `<span>` elements in the first paragraph are inline by default and so do not force line breaks.
- The `<ul>` element that is set to `display: inline-flex` creates an inline box containing some flex items.
- The two paragraphs are both set to `display: inline`. The inline flex container and paragraphs all run together on one line rather than breaking onto new lines (as they would do if they were displaying as block-level elements).

**To toggle between the display modes, you can change `display: inline` to `display: block` or `display: inline-flex` to `display: flex`.**https://mdn.github.io/css-examples/learn/box-model/inline.html

The key thing to remember for now is: Changing the value of the `display` property can change whether the outer display type of a box is block or inline. This changes the way it displays alongside other elements in the layout.

## [What is the CSS box model?](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#what_is_the_css_box_model)

The CSS box model as a whole applies to block boxes and defines how the different parts of a box — margin, border, padding, and content — work together to create a box that you can see on a page. Inline boxes use just *some* of the behavior defined in the box model.

To add complexity, there is a standard and an alternate box model. By default, browsers use the standard box model.

### [Parts of a box](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#parts_of_a_box)

Making up a block box in CSS we have the:

- **Content box**: The area where your content is displayed; size it using properties like [`inline-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/inline-size) and [`block-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/block-size) or [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width) and [`height`](https://developer.mozilla.org/en-US/docs/Web/CSS/height).
- **Padding box**: The padding sits around the content as white space; size it using [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding) and related properties.
- **Border box**: The border box wraps the content and any padding; size it using [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border) and related properties.
- **Margin box**: The margin is the outermost layer, wrapping the content, padding, and border as whitespace between this box and other elements; size it using [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) and related properties.

The below diagram shows these layers:

<figure class="wp-block-image">![Diagram of the box model](https://image-control-storage.s3.amazonaws.com/2023/01/01181137/box-model-1-4.png)</figure>### [The standard CSS box model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#the_standard_css_box_model)

In the standard box model, if you give a box an `inline-size` and a `block-size` (or `width` and a `height`) attributes, this defines the inline-size and block-size (width and height in horizontal languages) of the *content box*. Any padding and border is then added to those dimensions to get the total size taken up by the box (see image below).

If we assume that a box has the following CSS:

```
.box {
  width: 350px;
  height: 150px;
  margin: 10px;
  padding: 25px;
  border: 5px solid black;
}

```

The *actual* space taken up by the box will be 410px wide (350 + 25 + 25 + 5 + 5) and 210px high (150 + 25 + 25 + 5 + 5).

<figure class="wp-block-image">![Showing the size of the box when the standard box model is being used.](https://image-control-storage.s3.amazonaws.com/2023/01/01181138/standard-box-model.png)</figure>**Note:** The margin is not counted towards the actual size of the box — sure, it affects the total space that the box will take up on the page, but only the space outside the box. The box’s area stops at the border — it does not extend into the margin.

### [The alternative CSS box model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#the_alternative_css_box_model)

In the alternative box model, any width is the width of the visible box on the page. The content area width is that width minus the width for the padding and border (see image below). No need to add up the border and padding to get the real size of the box.

To turn on the alternative model for an element, set `box-sizing: border-box` on it:

```css
.box {
  box-sizing: border-box;
}

```

If we assume the box has the same CSS as above:

```css
.box {
  width: 350px;
  inline-size: 350px;
  height: 150px;
  block-size: 150px;
  margin: 10px;
  padding: 25px;
  border: 5px solid black;
}

```

Now, the *actual* space taken up by the box will be 350px in the inline direction and 150px in the block direction.

<figure class="wp-block-image">![Showing the size of the box when the alternate box model is being used.](https://image-control-storage.s3.amazonaws.com/2023/01/01181139/alternate-box-model.png)</figure>To use the alternative box model for all of your elements (which is a common choice among developers), set the `box-sizing` property on the `<html>` element and set all other elements to inherit that value:

```css
html {
  box-sizing: border-box;
}
*,
*::before,
*::after {
  box-sizing: inherit;
}

```

## [Playing with box models](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#playing_with_box_models)

In the example below, you can see two boxes. Both have a class of `.box`, which gives them the same `width`, `height`, `margin`, `border`, and `padding`. The only difference is that the second box has been set to use the alternative box model.

**Can you change the size of the second box (by adding CSS to the `.alternate` class) to make it match the first box in width and height?**https://mdn.github.io/css-examples/learn/box-model/box-models.html

**Note:** You can find a solution for this task [here](https://github.com/mdn/css-examples/blob/main/learn/solutions.md#the-box-model).

### [Use browser DevTools to view the box model](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#use_browser_devtools_to_view_the_box_model)

Your [browser developer tools](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_are_browser_developer_tools) can make understanding the box model far easier. If you inspect an element in Firefox’s DevTools, you can see the size of the element plus its margin, padding, and border. Inspecting an element in this way is a great way to find out if your box is really the size you think it is!

<figure class="wp-block-image">![Inspecting the box model of an element using Firefox DevTools](https://image-control-storage.s3.amazonaws.com/2023/01/01181140/box-model-devtools.png)</figure>## [Margins, padding, and borders](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#margins_padding_and_borders)

You’ve already seen the [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin), [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding), and [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border) properties at work in the example above. The properties used in that example are **shorthands** and allow us to set all four sides of the box at once. These shorthands also have equivalent longhand properties, which allow control over the different sides of the box individually.

Let’s explore these properties in more detail.

### [Margin](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#margin)

The margin is an invisible space around your box. It pushes other elements away from the box. Margins can have positive or negative values. Setting a negative margin on one side of your box can cause it to overlap other things on the page. Whether you are using the standard or alternative box model, the margin is always added after the size of the visible box has been calculated.

We can control all margins of an element at once using the [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) property, or each side individually using the equivalent longhand properties:

- [`margin-top`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-top)
- [`margin-right`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-right)
- [`margin-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-bottom)
- [`margin-left`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)

**In the example below, try changing the margin values to see how the box is pushed around due to the margin creating or removing space (if it is a negative margin) between this element and the containing element.**https://mdn.github.io/css-examples/learn/box-model/margin.html

#### Margin collapsing

Depending on whether two elements whose margins touch have positive or negative margins, the results will be different:

- Two positive margins will combine to become one margin. Its size will be equal to the largest individual margin.
- Two negative margins will collapse and the smallest (furthest from zero) value will be used.
- If one margin is negative, its value will be *subtracted* from the total.

In the example below, we have two paragraphs. The top paragraph has a `margin-bottom` of 50 pixels, the other has a `margin-top` of 30 pixels. The margins have collapsed together so the actual margin between the boxes is 50 pixels and not the total of the two margins.

**You can test this by setting the `margin-top` of paragraph two to 0. The visible margin between the two paragraphs will not change — it retains the 50 pixels set in the `margin-bottom` of paragraph one. If you set it to -10px, you’ll see that the overall margin becomes 40px — it subtracts from the 50px.**https://mdn.github.io/css-examples/learn/box-model/margin-collapse.html

A number of rules dictate when margins do and do not collapse. For further information see the detailed page on [mastering margin collapsing](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing). The main thing to remember is that margin collapsing is a thing that happens if you are creating space with margins and don’t get the space you expect.

### [Borders](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#borders)

The border is drawn between the margin and the padding of a box. If you are using the standard box model, the size of the border is added to the `width` and `height` of the content box. If you are using the alternative box model then the size of the border makes the content box smaller as it takes up some of that available `width` and `height` of the element box.

For styling borders, there are a large number of properties — there are four borders, and each border has a style, width, and color that we might want to manipulate.

You can set the width, style, or color of all four borders at once using the [`border`](https://developer.mozilla.org/en-US/docs/Web/CSS/border) property.

To set the properties of each side individually, use:

- [`border-top`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top)
- [`border-right`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right)
- [`border-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom)
- [`border-left`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left)

To set the width, style, or color of all sides, use:

- [`border-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width)
- [`border-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style)
- [`border-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color)

To set the width, style, or color of a single side, use one of the more granular longhand properties:

- [`border-top-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-width)
- [`border-top-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-style)
- [`border-top-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-color)
- [`border-right-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-width)
- [`border-right-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-style)
- [`border-right-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-right-color)
- [`border-bottom-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-width)
- [`border-bottom-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-style)
- [`border-bottom-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-color)
- [`border-left-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-width)
- [`border-left-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-style)
- [`border-left-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-left-color)

In the example below, we have used various shorthands and longhands to create borders. Play around with the different properties to check that you understand how they work. The MDN pages for the border properties give you information about the different available border styles.https://mdn.github.io/css-examples/learn/box-model/border.html

### [Padding](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#padding)

The padding sits between the border and the content area and is used to push the content away from the border. Unlike margins, you cannot have a negative padding. Any background applied to your element will display behind the padding.

The [`padding`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding) property controls the padding on all sides of an element. To control each side individually, use these longhand properties:

- [`padding-top`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-top)
- [`padding-right`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-right)
- [`padding-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-bottom)
- [`padding-left`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding-left)

In the example below, you can change the values for padding on the class `.box` to see that this changes where the text begins in relation to the box. You can also change the padding on the class `.container` to create space between the container and the box. You can change the padding on any element to create space between its border and whatever is inside the element.https://mdn.github.io/css-examples/learn/box-model/padding.html

## [The box model and inline boxes](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#the_box_model_and_inline_boxes)

All of the above fully applies to block boxes. Some of the properties can apply to inline boxes too, such as those created by a `<span>` element.

In the example below, we have a `<span>` inside a paragraph. We have applied a `width`, `height`, `margin`, `border`, and `padding` to it. You can see that the width and height are ignored. The vertical margin, padding, and border are respected but don’t change the relationship of other content to our inline box. The padding and border overlap other words in the paragraph. The horizontal padding, margins, and borders move other content away from the box.https://mdn.github.io/css-examples/learn/box-model/inline-box-model.html

## [Using display: inline-block](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#using_display_inline-block)

`display: inline-block` is a special value of `display`, which provides a middle ground between `inline` and `block`. Use it if you do not want an item to break onto a new line, but do want it to respect `width` and `height` and avoid the overlapping seen above.

An element with `display: inline-block` does a subset of the block things we already know about:

- The `width` and `height` properties are respected.
- `padding`, `margin`, and `border` will cause other elements to be pushed away from the box.

It does not, however, break onto a new line, and will only become larger than its content if you explicitly add `width` and `height` properties.

**In this next example, we have added `display: inline-block` to our `<span>` element. Try changing this to `display: block` or removing the line completely to see the difference in display models.**https://mdn.github.io/css-examples/learn/box-model/inline-block.html

Where this can be useful is when you want to give a link a larger hit area by adding `padding`. `<a>` is an inline element like `<span>`; you can use `display: inline-block` to allow padding to be set on it, making it easier for a user to click the link.

You see this fairly frequently in navigation bars. The navigation below is displayed in a row using flexbox and we have added padding to the `<a>` element as we want to be able to change the `background-color` when the `<a>` is hovered. The padding appears to overlap the border on the `<ul>` element. This is because the `<a>` is an inline element.

**Add `display: inline-block` to the rule with the `.links-list a` selector, and you will see how it fixes this issue by causing the padding to be respected by other elements.**https://mdn.github.io/css-examples/learn/box-model/inline-block-nav.html

### [Additional Resources](https://www.theodinproject.com/lessons/foundations-the-box-model#additional-resources)

This section contains helpful links to related content. It isn’t required, so consider it supplemental.

- [This W3Schools tutorial on CSS Box Model](https://www.w3schools.com/css/css_boxmodel.asp) provides an interactive playground to test your box model skills with exercises.