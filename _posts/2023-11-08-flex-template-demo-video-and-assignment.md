---
id: 64007
title: 'Flex-Template: Demo Video and Assignment'
date: '2023-11-08T12:42:48-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=64007'
permalink: /flex-template-demo-video-and-assignment/
footnotes:
    - ''
categories:
    - Projects
---

<iframe allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen="" frameborder="0" height="500" loading="lazy" src="https://www.youtube.com/embed/v2WpYzBe5zc?si=Y2O-8x0idDbBx4F9" title="YouTube video player" width="800"></iframe>## Smooth Scroll Script

```javascript
<script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>
<script src="https://google-code-prettify.googlecode.com/svn/loader/run_prettify.js"></script>

<script>
  $(function() {
    $("a[href*=#]:not([href=#])").click(function() {
      if (
        location.pathname.replace(/^\//, "") ==
        this.pathname.replace(/^\//, "") &&
        location.hostname == this.hostname
      ) {
        var target = $(this.hash);
        target = target.length ? target : $("[name=" + this.hash.slice(1) + "]");
        if (target.length) {
          $("html,body").animate({
              scrollTop: target.offset().top
            },
            1000
          );
          return false;
        }
      }
    });
  });
</script>
```

## Fixed Top Navbar

<iframe allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen="" frameborder="0" height="500" loading="lazy" src="https://www.youtube.com/embed/4rocQPjZPjc?si=KCNYpda8hid6vOxw" title="YouTube video player" width="800"></iframe>```css
/*Default Fixed Top Navbar Code*/

.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  width: 80%;
  margin: auto;
  height: auto;
  background: #257ca1;
  border-radius-left: 10px;
  border-bottom-left-radius: 10px;
  border-bottom-right-radius: 10px;
  padding: 25px;
  margin-bottom: 50px;
  display: flex;
  flex-wrap: wrap;
  max-width: 1200px;
  justify-content: center;
  justify-content: space-between;
}


/*Default Tablet Fixed Top Navbar Code*/

.navbar {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    width: 80%;
    background: #257ca1;
    max-width: 750px;
    height: auto;
    margin-left: 10%;
    margin-right: 50%;
    padding: 50px;
    display: flex;
    flex-wrap: wrap;
    align-content: space-between;
    justify-content: center;
    display: block;
  }


/*Default Phone Fixed Top Navbar Code*/

.navbar {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    background: #257ca1;
    width: 400px;

    height: auto;
    overflow: auto;
    margin: auto;
    /* margin-left: 10%;
    margin-right: 50%;*/
    padding: 50px;
    display: flex;
    flex-wrap: wrap;
    align-content: space-between;
    justify-content: center;
    display: block;
  }
```

## Background Video (HTML)

<iframe allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen="" frameborder="0" height="500" loading="lazy" src="https://www.youtube.com/embed/S1IvivmqMmE?si=K6-0nHAFcYz9O2Ah" title="YouTube video player" width="800"></iframe>If you wish to include a Background Video to your project, insert the following code below the stylesheet link in your pages header tags.

```markup
<video src="video/australia_opera.mp4" loop muted autoplay poster="#" type="video/mp4"></video>
```

## Background Video (CSS)

```css
video {
  object-fit: cover;
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  left: 0;
}
```

## Flex Trick

Having trouble removing flex commands in @media? Use the folling command and start from scratch!

```css
.column {
 all: initial;
}
```

## Utilizing the template and demo you worked on in class, perform the following:

- Remove all background colors, border radius, etc.
- Make all links visible (use #999 or #ccc) if you want to use greys until you pick a color scheme.
- Decide what your website will be. Portfolio? Business, etc..
- You most likely will need a logo. It can be created in CSS or a graphic program.
- Decide what separate pages you will need (6 minimum). How many (class=”cols”) will you need on each page? What type? What will they contain? Images, text, video, audio?
- Will you need code and functionality not demonstrated in the template? We can make it happen!
- Use a separate folder for this project. It will live in your home (root) directory.

## Part II

Your website should consist of six pages. The topic of the site is your choice (with my approval.)

**The following are the requirements for your project.**

- Six web pages
- Top fixed navigation (if you wish. view the video on this page for more information on fixed navigation). The nav items need to be linked to the appropriate page.
- Social media Icons (They don’t need to link to your social media accounts (if any)
- A logo. (It can be straightforward. Your initials or name in a nice, clean font would suffice. Although, you can create something in the Adobe Creative Suite.
- Create a color scheme that will go well with your site. Many sites can help you. One is <https://coolors.co/>, [colorlovers.com](http://colorlovers.com), <https://color.adobe.com/create/color-wheel>
- Each page needs a specific topic (The pages should correspond to your topnav)
- Include interesting photography. (People like big pictures)
- Your site should be dynamic and viewable on multiple devices. We already established this functionality with our template.
- Please keep it simple and clean. Whitespace can make a viewer feel comfortable.
- You may wish to put all your content in a wrapper. That will help you constrain and organize your layout.
- Use at least one media type on a page (audio, video, animated gif, Soundcloud or YouTube?)
- The amount of content per page should be appropriate to the classification of the page. A simple “about” page should include pictures, text, and perhaps some links to external sites.
- Links should have a rollover state – including the navigation.
- One or more image rollover states (we did this in CSS).
- One link (or more) should direct a viewer to another site page. (Internal Links)
- Div nesting (You will need to do this anyway to build your site.)

**Optional:**

Do not feel constrained. You can do amazing things with this project!

Perhaps use gradients somewhere? Maybe a background? Anything that will complement the design of your site.

Video background. If you decide to do this, be subtle and use a simple video that doesn’t detract from your

**NOTE: You will have time to work on this site. Do not rush. (It should be completed in class ) – mostly. I will need to approve your site before you upload it.**