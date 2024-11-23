---
id: 58382
title: 'CSS Flexbox Poster and Demo'
date: '2023-02-17T13:24:36-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=58382'
permalink: /css-flexbox/
footnotes:
    - ''
amazonS3_cache:
    - 'a:5:{s:63:"//www.nuggetofjoy.com/wp-content/uploads/css-flexbox-poster.png";a:1:{s:9:"timestamp";i:1732397993;}s:72:"//www.nuggetofjoy.com/wp-content/uploads/css-flexbox-poster-683x1024.png";a:1:{s:9:"timestamp";i:1732385582;}s:72:"//www.nuggetofjoy.com/wp-content/uploads/css-flexbox-poster-768x1152.png";a:1:{s:9:"timestamp";i:1732385582;}s:73:"//www.nuggetofjoy.com/wp-content/uploads/css-flexbox-poster-1024x1536.png";a:1:{s:9:"timestamp";i:1732385582;}s:73:"//www.nuggetofjoy.com/wp-content/uploads/css-flexbox-poster-1365x2048.png";a:1:{s:9:"timestamp";i:1732385582;}}'
categories:
    - 'DMET 155 Introduction to Web Design'
---

<figure class="wp-block-gallery has-nested-images columns-default is-cropped wp-block-gallery-23 is-layout-flex wp-block-gallery-is-layout-flex"><figure class="wp-block-image size-full">![Flexbox Poster](https://www.nuggetofjoy.com/wp-content/uploads/css-flexbox-poster.png)</figure></figure><div class="wp-block-image"><figure class="aligncenter size-large is-resized">![container](https://css-tricks.com/wp-content/uploads/2018/10/01-container.svg)</figure></div>## [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-properties-for-the-parentflex-container)Properties for the Parent  
(flex container)

#### [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-display)display

This defines a flex container; inline or block depending on the given value. It enables a flex context for all its direct children.

```
.container {
  display: flex; <em>/* or inline-flex */</em>
}
```

Note that CSS columns have no effect on a flex container.

#### [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flex-direction)flex-direction

<div class="wp-block-image"><figure class="aligncenter size-large is-resized">![the four possible values of flex-direction being shown: top to bottom, bottom to top, right to left, and left to right](https://css-tricks.com/wp-content/uploads/2018/10/flex-direction.svg)</figure></div>  
This establishes the main-axis, thus defining the direction flex items are placed in the flex container. Flexbox is (aside from optional wrapping) a single-direction layout concept. Think of flex items as primarily laying out either in horizontal rows or vertical columns.

```
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

- `row` (default): left to right in `ltr`; right to left in `rtl`
- `row-reverse`: right to left in `ltr`; left to right in `rtl`
- `column`: same as `row` but top to bottom
- `column-reverse`: same as `row-reverse` but bottom to top

#### [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flex-wrap)flex-wrap

<div class="wp-block-image"><figure class="aligncenter size-large is-resized">![two rows of boxes, the first wrapping down onto the second](https://css-tricks.com/wp-content/uploads/2018/10/flex-wrap.svg)</figure></div>By default, flex items will all try to fit onto one line. You can change that and allow the items to wrap as needed with this property.

```
.container {
  flex-wrap: nowrap | wrap | wrap-reverse;
}
```

- `nowrap` (default): all flex items will be on one line
- `wrap`: flex items will wrap onto multiple lines, from top to bottom.
- `wrap-reverse`: flex items will wrap onto multiple lines from bottom to top.

There are some [visual demos of `flex-wrap` here](https://css-tricks.com/almanac/properties/f/flex-wrap/).

#### [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flex-flow)flex-flow

This is a shorthand for the `flex-direction` and `flex-wrap` properties, which together define the flex container’s main and cross axes. The default value is `row nowrap`.

```
.container {
  flex-flow: column wrap;
}
```

#### [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-justify-content)justify-content

<div class="wp-block-image"><figure class="aligncenter size-large is-resized">![flex items within a flex container demonstrating the different spacing options](https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg)</figure></div>  
This defines the alignment along the main axis. It helps distribute extra free space leftover when either all the flex items on a line are inflexible, or are flexible but have reached their maximum size. It also exerts some control over the alignment of items when they overflow the line.

```
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right ... + safe | unsafe;
}
```

- `flex-start` (default): items are packed toward the start of the flex-direction.
- `flex-end`: items are packed toward the end of the flex-direction.
- `start`: items are packed toward the start of the `writing-mode` direction.
- `end`: items are packed toward the end of the `writing-mode` direction.
- `left`: items are packed toward left edge of the container, unless that doesn’t make sense with the `flex-direction`, then it behaves like `start`.
- `right`: items are packed toward right edge of the container, unless that doesn’t make sense with the `flex-direction`, then it behaves like `end`.
- `center`: items are centered along the line
- `space-between`: items are evenly distributed in the line; first item is on the start line, last item on the end line
- `space-around`: items are evenly distributed in the line with equal space around them. Note that visually the spaces aren’t equal, since all the items have equal space on both sides. The first item will have one unit of space against the container edge, but two units of space between the next item because that next item has its own spacing that applies.
- `space-evenly`: items are distributed so that the spacing between any two items (and the space to the edges) is equal.

Note that that browser support for these values is nuanced. For example, `space-between` never got support from some versions of Edge, and start/end/left/right aren’t in Chrome yet. MDN [has detailed charts](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content). The safest values are `flex-start`, `flex-end`, and `center`.

There are also two additional keywords you can pair with these values: `safe` and `unsafe`. Using `safe` ensures that however you do this type of positioning, you can’t push an element such that it renders off-screen (e.g. off the top) in such a way the content can’t be scrolled too (called “data loss”).

## [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-align-items)align-items

<div class="wp-block-image"><figure class="aligncenter size-large is-resized">![demonstration of differnet alignment options, like all boxes stuck to the top of a flex parent, the bottom, stretched out, or along a baseline](https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg)</figure></div>  
This defines the default behavior for how flex items are laid out along the **cross axis** on the current line. Think of it as the `justify-content` version for the cross-axis (perpendicular to the main-axis).

```
.container {
  align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline | start | end | self-start | self-end + ... safe | unsafe;
}
```

- `stretch` (default): stretch to fill the container (still respect min-width/max-width)
- `flex-start` / `start` / `self-start`: items are placed at the start of the cross axis. The difference between these is subtle, and is about respecting the `flex-direction` rules or the `writing-mode` rules.
- `flex-end` / `end` / `self-end`: items are placed at the end of the cross axis. The difference again is subtle and is about respecting `flex-direction` rules vs. `writing-mode` rules.
- `center`: items are centered in the cross-axis
- `baseline`: items are aligned such as their baselines align

The `safe` and `unsafe` modifier keywords can be used in conjunction with all the rest of these keywords (although note [browser support](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)), and deal with helping you prevent aligning elements such that the content becomes inaccessible.

## [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-align-content)align-content

<div class="wp-block-image"><figure class="aligncenter size-large is-resized">![examples of the align-content property where a group of items cluster at the top or bottom, or stretch out to fill the space, or have spacing.](https://css-tricks.com/wp-content/uploads/2018/10/align-content.svg)</figure></div>  
This aligns a flex container’s lines within when there is extra space in the cross-axis, similar to how `justify-content` aligns individual items within the main-axis.

**Note:** This property only takes effect on multi-line flexible containers, where `flex-wrap` is set to either `wrap` or `wrap-reverse`). A single-line flexible container (i.e. where `flex-wrap` is set to its default value, `no-wrap`) will not reflect `align-content`.

```
.container {
  align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch | start | end | baseline | first baseline | last baseline + ... safe | unsafe;
}
```

- `normal` (default): items are packed in their default position as if no value was set.
- `flex-start` / `start`: items packed to the start of the container. The (more supported) `flex-start` honors the `flex-direction` while `start` honors the `writing-mode` direction.
- `flex-end` / `end`: items packed to the end of the container. The (more support) `flex-end` honors the `flex-direction` while end honors the `writing-mode` direction.
- `center`: items centered in the container
- `space-between`: items evenly distributed; the first line is at the start of the container while the last one is at the end
- `space-around`: items evenly distributed with equal space around each line
- `space-evenly`: items are evenly distributed with equal space around them
- `stretch`: lines stretch to take up the remaining space

The `safe` and `unsafe` modifier keywords can be used in conjunction with all the rest of these keywords (although note [browser support](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items)), and deal with helping you prevent aligning elements such that the content becomes inaccessible.

## [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-gap-row-gap-column-gap)gap, row-gap, column-gap

<div class="wp-block-image"><figure class="aligncenter size-large is-resized">![row gap](https://css-tricks.com/wp-content/uploads/2021/09/gap-1.svg)</figure></div>[The `gap` property](https://css-tricks.com/almanac/properties/g/gap/) explicitly controls the space between flex items. It applies that spacing *only between items* not on the outer edges.

```css
.container {
  display: flex;
  ...
  gap: 10px;
  gap: 10px 20px; <em>/* row-gap column gap */</em>
  row-gap: 10px;
  column-gap: 20px;
}
```

The behavior could be thought of as a *minimum* gutter, as if the gutter is bigger somehow (because of something like `justify-content: space-between;`) then the gap will only take effect if that space would end up smaller.

It is not exclusively for flexbox, `gap` works in grid and multi-column layout as well.

## Properties for the Children  
(flex items)

<figure class="wp-block-image aligncenter size-large is-resized">![Flex Items
](https://css-tricks.com/wp-content/uploads/2018/10/02-items.svg)</figure>## order

<div class="wp-block-image"><figure class="aligncenter is-resized">![Diagram showing flexbox order. A container with the items being 1 1 1 2 3, -1 1 2 5, and 2 2 99.](https://css-tricks.com/wp-content/uploads/2018/10/order.svg)</figure></div>  
By default, flex items are laid out in the source order. However, the `order` property controls the order in which they appear in the flex container.

```css
.item {
  order: 5; <em>/* default is 0 */</em>
}
```

Items with the same `order` revert to source order.

## flex-grow

<div class="wp-block-image"><figure class="aligncenter is-resized">![two rows of items, the first has all equally-sized items with equal flex-grow numbers, the second with the center item at twice the width because its value is 2 instead of 1.](https://css-tricks.com/wp-content/uploads/2018/10/flex-grow.svg)</figure></div>  
This defines the ability for a flex item to grow if necessary. It accepts a unitless value that serves as a proportion. It dictates what amount of the available space inside the flex container the item should take up.

If all items have `flex-grow` set to `1`, the remaining space in the container will be distributed equally to all children. If one of the children has a value of `2`, that child would take up twice as much of the space as either one of the others (or it will try, at least).

```css
.item {
  flex-grow: 4; <em>/* default 0 */</em>
}
```

Negative numbers are invalid.

## [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flex-shrink)flex-shrink

This defines the ability for a flex item to shrink if necessary.

```css
.item {
  flex-shrink: 3; <em>/* default 1 */</em>
}
```

Negative numbers are invalid.

## [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flex-basis)flex-basis

This defines the default size of an element before the remaining space is distributed. It can be a length (e.g. 20%, 5rem, etc.) or a keyword. The `auto` keyword means “look at my width or height property” (which was temporarily done by the `main-size` keyword until deprecated). The `content` keyword means “size it based on the item’s content” – this keyword isn’t well supported yet, so it’s hard to test and harder to know what its brethren `max-content`, `min-content`, and `fit-content` do.

```css
.item {
  flex-basis:  | auto; <em>/* default auto */</em>
}
```

If set to `0`, the extra space around content isn’t factored in. If set to `auto`, the extra space is distributed based on its `flex-grow` value. [See this graphic.](http://www.w3.org/TR/css3-flexbox/images/rel-vs-abs-flex.svg)

## [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-flex)flex

This is the shorthand for `flex-grow,` `flex-shrink` and `flex-basis` combined. The second and third parameters (`flex-shrink` and `flex-basis`) are optional. The default is `0 1 auto`, but if you set it with a single number value, like `flex: 5;`, that changes the `flex-basis` to 0%, so it’s like setting `flex-grow: 5; flex-shrink: 1; flex-basis: 0%;`.

```css
.item {
  flex: none | [ <'flex-grow'> <'flex-shrink'>? || <'flex-basis'> ]
}
```

**It is recommended that you use this shorthand property** rather than set the individual properties. The shorthand sets the other values intelligently.

## [](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-align-self)align-self

<div class="wp-block-image"><figure class="aligncenter is-resized">![One item with a align-self value is positioned along the bottom of a flex parent instead of the top where all the rest of the items are.](https://css-tricks.com/wp-content/uploads/2018/10/align-self.svg)</figure></div>  
This allows the default alignment (or the one specified by `align-items`) to be overridden for individual flex items.

Please see the `align-items` explanation to understand the available values.

```css
.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```

Note that `float`, `clear` and `vertical-align` have no effect on a flex item.