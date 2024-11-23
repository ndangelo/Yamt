---
id: 58398
title: '11. Introduction To Flexbox'
date: '2023-01-09T17:47:30-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=58398'
permalink: /introduction-to-flexbox/
amazonS3_cache:
    - 'a:6:{s:51:"//www.nuggetofjoy.com/wp-content/uploads/03-4-4.png";a:2:{s:2:"id";s:5:"59404";s:11:"source_type";s:13:"media-library";}s:68:"//image-control-storage.s3.amazonaws.com/2023/01/12173410/03-4-4.png";a:2:{s:2:"id";s:5:"59404";s:11:"source_type";s:13:"media-library";}s:51:"//www.nuggetofjoy.com/wp-content/uploads/04-3-3.png";a:2:{s:2:"id";s:5:"59405";s:11:"source_type";s:13:"media-library";}s:68:"//image-control-storage.s3.amazonaws.com/2023/01/12173412/04-3-3.png";a:2:{s:2:"id";s:5:"59405";s:11:"source_type";s:13:"media-library";}s:51:"//www.nuggetofjoy.com/wp-content/uploads/05-1-1.png";a:2:{s:2:"id";s:5:"59406";s:11:"source_type";s:13:"media-library";}s:68:"//image-control-storage.s3.amazonaws.com/2023/01/12173412/05-1-1.png";a:2:{s:2:"id";s:5:"59406";s:11:"source_type";s:13:"media-library";}}'
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'odin project'
    - Projects
---

[](https://www.theodinproject.com/paths/foundations/courses/foundations)

### [Introduction](https://www.theodinproject.com/lessons/foundations-introduction-to-flexbox#introduction)

As you’ll learn, there are *many* ways to move elements around on a web page. New methods have been developed over the years and older things have fallen out of style. Flexbox is a [relatively new](https://medium.com/@BennyOgidan/history-of-css-grid-and-css-flexbox-658ae6cfe6d2) way of manipulating elements in CSS, and its debut was *revolutionary*.

Many resources put it near the end of their curriculum because it is somewhat new as a technology. But at this point, it has become the default way of positioning elements for many developers. Flexbox will be one of the most used tools in your toolbox, so why not learn it first?

### [Lesson Overview](https://www.theodinproject.com/lessons/foundations-introduction-to-flexbox#lesson-overview)

This section contains a general overview of topics that you will learn in this lesson.

- You will learn how to position elements using flexbox.
- You will learn about flex containers and flex items.
- You will learn how to create useful components and layouts that go beyond just stacking and centering items.

### [Before We Get Started](https://www.theodinproject.com/lessons/foundations-introduction-to-flexbox#before-we-get-started)

Flexbox layouts can get a little complicated. In a previous lesson, you learned how to inspect and debug things using your browser’s developer tools. Those tools will be *crucial* for you in the following lessons. If something isn’t behaving the way you expect, inspecting it in the developer tools should be your first step *every time*.

### [Let’s Flex!](https://www.theodinproject.com/lessons/foundations-introduction-to-flexbox#lets-flex)

Flexbox is a way to arrange items into rows or columns. These items will flex (i.e. grow or shrink) based on some simple rules that you can define. To get started, let’s look at a simple demonstration. For all the exercises here, take your time to inspect the code and really understand what’s going on. In fact, playing with the code yourself will make it much easier to retain this information.

See the Pen first flex example by TheOdinProject (@TheOdinProjectExamples) on CodePen.

We’ll get into exactly what’s going on here soon enough. But for now, let’s uncomment the two flex related CSS declarations in the above Codepen by removing the `/*` and `*/` tags surrounding them, then check out the result.

Comments prevent the browser from interpreting lines as code, and are wrapped between specific tags. CSS uses `/*`as an opening comment tag and `*/` as a closing comment tag, while HTML and JavaScript have their own syntax. Commented out lines of code can be ‘re-enabled’ simply by removing the comment tags surrounding the code.

All 3 divs should now be arranged horizontally. If you resize the results frame with the “1x”, “.5x” and “.25x” buttons you’ll also see that the divs will ‘flex’. They will fill the available area and will each have equal width.

If you add another div to the HTML, inside of `.flex-container`, it will show up alongside the others, and everything will flex to fit within the available area.

If it’s hard to see what’s going on in the small embedded CodePen, feel free to click the “Edit on CodePen” or “Fork on CodePen” button. This will bring the example into a full-sized environment. Some of the later examples might especially benefit from doing this.

For a more interactive explanation and example, try the following Scrim (let us know what you think of these):

https://scrimba.com/learn/flexbox/your-first-flexbox-layout-flexbox-tutorial-canLGCw?embed=odin,mini-header,no-big-play,no-next-up

#### Flex Containers and Flex Items

As you’ve seen, flexbox is not just a single CSS property but a whole toolbox of properties that you can use to put things where you need them. Some of these properties belong on the *flex container*, while some go on the *flex items*. This is a simple yet important concept.

A flex container is any element that has `display: flex` on it. A flex item is any element that lives directly inside of a flex container.

<figure class="wp-block-image">[![container-vs-child](https://image-control-storage.s3.amazonaws.com/2023/01/12173410/03-4-4.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/495704c6eb6bf33bc927534f231533a82b27b2ac/html_css/v2/foundations/flexbox/imgs/03.png)</figure>Somewhat confusingly, any element can be both a flex container *and* a flex item. Said another way, you can also put `display: flex` on a flex item and then use flexbox to arrange *its* children.

<figure class="wp-block-image">[![nesting flex containers](https://image-control-storage.s3.amazonaws.com/2023/01/12173412/04-3-3.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/495704c6eb6bf33bc927534f231533a82b27b2ac/html_css/v2/foundations/flexbox/imgs/04.png)</figure>Creating and nesting multiple flex containers and items is the primary way we will be building up complex layouts. The following image was achieved using *only* flexbox to arrange, size, and place the various elements. Flexbox is a *very* powerful tool.

<div class="wp-block-image"><figure class="aligncenter">[![complex example](https://image-control-storage.s3.amazonaws.com/2023/01/12173412/05-1-1.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/495704c6eb6bf33bc927534f231533a82b27b2ac/html_css/v2/foundations/flexbox/imgs/05.png)</figure></div><figure class="wp-block-embed is-type-wp-embed is-provider-communication-art-design-amp-instruction wp-block-embed-communication-art-design-amp-instruction"><div class="wp-block-embed__wrapper">> [CSS Flexbox Poster and Demo](https://www.nuggetofjoy.com/css-flexbox/)

<iframe class="wp-embedded-content" data-secret="aCKM4J4SHX" frameborder="0" height="282" loading="lazy" marginheight="0" marginwidth="0" sandbox="allow-scripts" scrolling="no" security="restricted" src="https://www.nuggetofjoy.com/css-flexbox/embed/#?secret=fQTxfmNYhH#?secret=aCKM4J4SHX" style="position: absolute; visibility: hidden;" title="“CSS Flexbox Poster and Demo” — Communication, Art, Design & Instruction" width="500"></iframe></div></figure>