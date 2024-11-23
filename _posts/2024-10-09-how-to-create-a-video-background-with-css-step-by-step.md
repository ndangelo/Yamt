---
id: 66735
title: 'How to Create a Video Background with CSS [Step-by-Step]'
date: '2024-10-09T17:06:52-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=66735'
permalink: /how-to-create-a-video-background-with-css-step-by-step/
categories:
    - Projects
---

**To use a video background,** we have to use the **HTML 5 `<video>` element with position `absolute` inside a container wrapper.**

Videos are increasingly common on websites nowadays and a great way to create a modern website. With just a bit of CSS you can add a video background to your site in minutes. However, note that this technique works only for `<video>` elements. This means the video will have to be hosted somewhere. You can also [use CSS to create a Youtube video background](https://alvarotrigo.com/blog/how-to-create-a-youtube-video-background-with-css/), but that’s not what this tutorial is about.

## Finding a background video

If you don’t have a video yet, the easiest way to find one for your site is to use video stock galleries like [Pixabay](https://pixabay.com/videos/) or [Pexel](https://www.pexels.com/videos/).

<div class="wp-block-image"><figure class="aligncenter">![Pixabay Free Video Stock](https://alvarotrigo.com/blog/assets/imgs/2021-10-27/pixabay-video-stock-free.jpeg)</figure></div>Once you find the one you want to use, you’ll have to download it and upload it to your server (or CDN services like [Cloudinary](https://cloudinary.com/)).

Once uploaded we have the URL of the video and we can use it in our `<video>` element.

## Adding the HTML for the video

For the video<span style="box-sizing: border-box; margin: 0px; padding: 0px;">, we’ll use the [HTML 5 video element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video). It expects at least a video source file and can be configured to pass</span> multiple HTML attributes.

For our example, we’ll be using this:

```markup
`<video <em>playsinline</em> <em>autoplay</em> <em>muted</em> <em>loop</em> <em>poster</em>="cake.jpg">    <source <em>src</em>="my-video-url.webm" <em>type</em>="video/webm">    Your browser does not support the video tag.</video>`<small>Code language: HTML, XML (xml)</small>
```

We’ll talk <span style="box-sizing: border-box; margin: 0px; padding: 0px;">more about the [background video configuration](https://alvarotrigo.com/blog/background-video-css/#configuring-the-video) and </span>[formats](https://alvarotrigo.com/blog/background-video-css/#video-formats-and-browser-compatibility).

## Placing the video in the background with CSS

Usually, in CSS we set the background image by using the `background` property or the `background-image` one.

```css
`background: url(imgs/my-background-image.png);background-size: cover;`<small>Code language: CSS (css)</small>
```

However, the [background property](https://developer.mozilla.org/en-US/docs/Web/CSS/background) only works for images and colors. Not with videos.

Now we have a standard video element, so, how do we convert it into a background? We’ll be using a little trick here. Using the CSS `position: absolute` we will simulate a background element.

```css
`video {  position: absolute;  top: 0;  left: 0;}`<small>Code language: CSS (css)</small>
```

This will place our video outside the document’s normal flow and relative to the element we choose within its parents.

So, time to add our video container! We’ll be using a `div` element as the container for our video. We called it `video-wrapper`.

```markup
`<div <em>class</em>="video-wrapper">  <video <em>playsinline</em> <em>autoplay</em> <em>muted</em> <em>loop</em> <em>poster</em>="cake.jpg">    <source <em>src</em>="my-css-video-background.webm" <em>type</em>="video/webm">    Your browser does not support the video tag.  </video></div>`<small>Code language: HTML, XML (xml)</small>
```

And here’s where the magic happens:

```css
`.video-wrapper {  /* Telling our absolute positioned video to   be relative to this element */  position: relative;  width: 400px;  height: 200px;  /* Will not allow the video to overflow the   container */  overflow: hidden;  /* Centering the container's content vertically   and horizontally */  text-align: center;  display: flex;  align-items: center;  justify-content: center;}`<small>Code language: CSS (css)</small>
```

I added comments on the CSS code so you can see what each of the properties is for.

## Making the background video cover the whole container

It’s common for backgrounds to cover the whole container. We usually do this with CSS by using the style `background-size: cover` directly on the background image. But because in this case, our video is not actually a CSS background, we’ll be using another little trick by using `object-fit: cover` together with `height: 100%` and `width: 100%` on our `video` element.

```css
`video {  /** Simulationg background-size: cover */  object-fit: cover;  height: 100%;  width: 100%;  position: absolute;  top: 0;  left: 0;}`<small>Code language: CSS (css)</small>
```

To illustrate this better, here’s an example of a video background not covering the whole container:

See the Pen Video background CSS – not background cover by Álvaro (@alvarotrigo) on CodePen.

And here’s the same video background covering the whole container:

See the Pen Video background CSS – not background cover by Álvaro (@alvarotrigo) on CodePen.

## Adding elements on top of the video background

Right now there’s nothing special we have to do in order to add content on top of our video. And that’s because we added the property `position: relative` to the video container when setting the video as a background (which is absolute positioned).

Anything that you add after the video element will be positioned on top of it.

```markup
`<div <em>class</em>="video-wrapper">  <video <em>playsinline</em> <em>autoplay</em> <em>muted</em> <em>loop</em> <em>poster</em>="cake.jpg">    <source <em>src</em>="my-css-video-background.webm" <em>type</em>="video/webm">    Your browser does not support the video tag.  </video>  <!-- This will be positioned on top of our video background -->  <div <em>class</em>="header">    <h1>Blueberry Cheesecake</h1>    <button>Recipe here</button>  </div></div>`<small>Code language: HTML, XML (xml)</small>
```

Here’s the final result:

See the Pen Video background CSS by Álvaro (@alvarotrigo) on CodePen.

## Configuring the video

If you noticed, in our HTML code we’ve added quite a few things on the `video` element. The most important ones are `loop`, `muted` and `autoplay`.

```markup
`<video <em>playsinline</em> <em>autoplay</em> <em>muted</em> <em>loop</em> <em>poster</em>="cake.jpg">    <source <em>src</em>="my-css-video-background.webm" <em>type</em>="video/webm">    Your browser does not support the video tag.</video>`<small>Code language: HTML, XML (xml)</small>
```

Videos won’t be able to autoplay unless we mute them first. And if you are using a video background using the `loop` option is quite common too, so the video will play endlessly.

The `poster` is the image we want to show while the video still loading and can’t yet autoplay.

## Video formats and browser compatibility

The [HTML 5 video element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video) allows the use of multiple source files. This means we can provide our video in different formats for browser compatibility.

```markup
`<video <em>playsinline</em> <em>autoplay</em> <em>muted</em> <em>loop</em> <em>poster</em>="my-static-image.jpg">    <source <em>src</em>="my-video-url.webm" <em>type</em>="video/webm">    <source <em>src</em>="my-video-url.mp4" <em>type</em>="video/mp4">    Your browser does not support the video tag.</video>`<small>Code language: HTML, XML (xml)</small>
```

In this example, we first try to load the `webm` video, and if the browser can’t play it, it will fall back to the `mp4` version of it.

Not all browsers can play all kinds of video formats, see [the compatibility table for each video format](https://caniuse.com/?search=video%20format).[](https://caniuse.com/?search=video%20format)

<div class="wp-block-image"><figure class="aligncenter">[![AVI Format Browser Compatibility](https://alvarotrigo.com/blog/assets/imgs/2021-10-27/video-formats-compatiblity.jpeg)](https://caniuse.com/?search=video%20format)</figure></div>The `mp4` most modern browsers widely accept format, but using alternatives like `webm` can come in handy to save bandwidth too. So, adding both can be a good combination.

If you wonder how to convert from one format to another, you can use any of the online converters. Just Google “mp4 to webm” or “webm to mp4” and you’ll find plenty of converters online.

## Conclusion

There’s no excuse to use videos nowadays. Videos in websites are a very powerful design tool that can provide your website a modern look. They are easy to implement, ligther that GIF animations and high quality.

As you could see, you only need a few lines of CSS to set any video as a background. And, if you want to go one step further, you can go full-screen by using components like [fullPage.js](https://alvarotrigo.com/fullPage/). Check out the [video example here](https://alvarotrigo.com/fullPage/examples/videoBackground.html).

[](https://alvarotrigo.com/fullPage/)