---
id: 58408
title: '8. Inspecting HTML And CSS'
date: '2023-01-09T17:57:50-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=58408'
permalink: /inspecting-html-and-css/
amazonS3_cache:
    - 'a:10:{s:51:"//www.nuggetofjoy.com/wp-content/uploads/00-9-1.png";a:2:{s:2:"id";s:5:"59390";s:11:"source_type";s:13:"media-library";}s:68:"//image-control-storage.s3.amazonaws.com/2023/01/12172918/00-9-1.png";a:2:{s:2:"id";s:5:"59390";s:11:"source_type";s:13:"media-library";}s:51:"//www.nuggetofjoy.com/wp-content/uploads/01-2-1.png";a:2:{s:2:"id";s:5:"59391";s:11:"source_type";s:13:"media-library";}s:68:"//image-control-storage.s3.amazonaws.com/2023/01/12172922/01-2-1.png";a:2:{s:2:"id";s:5:"59391";s:11:"source_type";s:13:"media-library";}s:51:"//www.nuggetofjoy.com/wp-content/uploads/02-2-1.png";a:2:{s:2:"id";s:5:"59392";s:11:"source_type";s:13:"media-library";}s:68:"//image-control-storage.s3.amazonaws.com/2023/01/12172923/02-2-1.png";a:2:{s:2:"id";s:5:"59392";s:11:"source_type";s:13:"media-library";}s:51:"//www.nuggetofjoy.com/wp-content/uploads/03-4-2.png";a:2:{s:2:"id";s:5:"59393";s:11:"source_type";s:13:"media-library";}s:68:"//image-control-storage.s3.amazonaws.com/2023/01/12172927/03-4-2.png";a:2:{s:2:"id";s:5:"59393";s:11:"source_type";s:13:"media-library";}s:51:"//www.nuggetofjoy.com/wp-content/uploads/04-3-1.png";a:2:{s:2:"id";s:5:"59394";s:11:"source_type";s:13:"media-library";}s:68:"//image-control-storage.s3.amazonaws.com/2023/01/12172928/04-3-1.png";a:2:{s:2:"id";s:5:"59394";s:11:"source_type";s:13:"media-library";}}'
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'odin project'
---

Being able to inspect and debug your HTML and CSS is critical to frontend development. This lesson will take us through the Chrome Dev Tools, which allow you to see detailed information about your elements and CSS rules, as well as assist you in finding and fixing problems in your code.

### [Lesson Overview](https://www.theodinproject.com/lessons/foundations-inspecting-html-and-css#lesson-overview)

This section contains a general overview of topics that you will learn in this lesson.

- You will know how to access the element inspector.
- You will know how to select and inspect specific elements.
- You will know how to test out HTML and CSS in the inspector.

### [The Inspector](https://www.theodinproject.com/lessons/foundations-inspecting-html-and-css#the-inspector)

To open up the inspector, you can right-click on any element of a webpage and click “Inspect Element” or press F12. For example, if you navigate to [our homepage](https://theodinproject.com/) and open the inspector, you might see something that looks a little bit like the image below. (Note that if you are already logged in to TOP you will not see the page shown below. If you want to stay logged in, use Incognito mode or your browser’s equivalent to separately view the page.)

<figure class="wp-block-image">[![Chrome Inspector](https://image-control-storage.s3.amazonaws.com/2023/01/12172918/00-9-1.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/594984d7c9f9e744577f19ea475b3864e8cc7c91/html_css/v2/foundations/inspecting-html-and-css/imgs/00.png)</figure>Don’t get overwhelmed with all the tools you’re now seeing! For this lesson, we want to focus on the Elements and Styles panes.

### [Inspecting Elements](https://www.theodinproject.com/lessons/foundations-inspecting-html-and-css#inspecting-elements)

In the Elements pane, you can see the entire HTML structure of your page. You can click on any of the elements in this pane to select that specific element. Alternatively, you can click the blue-highlighted icon shown below on the left, and hover over any element on the page.

<figure class="wp-block-image">[![Inspector Icon](https://image-control-storage.s3.amazonaws.com/2023/01/12172922/01-2-1.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/594984d7c9f9e744577f19ea475b3864e8cc7c91/html_css/v2/foundations/inspecting-html-and-css/imgs/01.png)</figure>When an element is selected, the Styles tab will show all the currently applied styles, as well as any styles that are being overwritten (indicated by a strikethrough of the text). For example, if you use the inspector to click on the “Your Career in Web Development Starts Here” header on the TOP homepage, on the right-hand side you’ll see all the styles that are currently affecting the element, as seen below:

<figure class="wp-block-image">[![Styles Pane](https://image-control-storage.s3.amazonaws.com/2023/01/12172923/02-2-1.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/594984d7c9f9e744577f19ea475b3864e8cc7c91/html_css/v2/foundations/inspecting-html-and-css/imgs/02.png)</figure><figure class="wp-block-image">[![Overwritten style](https://image-control-storage.s3.amazonaws.com/2023/01/12172927/03-4-2.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/f8fd38fc62578d8e8368f5303126215a492847f0/foundations/html_css/inspecting-html-and-css/imgs/03.png)</figure>### [Testing Styles in the Inspector](https://www.theodinproject.com/lessons/foundations-inspecting-html-and-css#testing-styles-in-the-inspector)

The Styles pane also allows you to edit styles directly in the browser. You can click inside of any individual selector to add a new rule or click on an existing attribute or value to alter it.

In the below image, we have altered the value of `margin-bottom` in the `.hero__main-heading` class, and the webpage responds with the changes in real-time. This won’t affect the source code in your text editor, but it is extremely useful for quickly testing out various attributes and values without needing to reload the page over and over again.

<figure class="wp-block-image">[![Changed styles](https://image-control-storage.s3.amazonaws.com/2023/01/12172928/04-3-1.png)](https://cdn.statically.io/gh/TheOdinProject/curriculum/f8fd38fc62578d8e8368f5303126215a492847f0/foundations/html_css/inspecting-html-and-css/imgs/04.png)</figure>### [Assignment](https://www.theodinproject.com/lessons/foundations-inspecting-html-and-css#assignment)

Go through the following sections of the [official Chrome DevTools docs](https://developers.google.com/web/tools/chrome-devtools):

- [Overview](https://developer.chrome.com/docs/devtools/overview/): don’t navigate to any other pages linked here; just get familiar with *what* tools are available in the DevTools, rather than how to use all of them right now.
- [Open Chrome DevTools](https://developer.chrome.com/docs/devtools/open/): similar to what we went over above, but with some nice extras.
- [View and change CSS](https://developer.chrome.com/docs/devtools/css): be sure to follow along with any interactive instructions!
- [Get Started With Viewing And Changing The DOM](https://developer.chrome.com/docs/devtools/dom/): skip through any part that uses the JavaScript console.

### [Knowledge Check](https://www.theodinproject.com/lessons/foundations-inspecting-html-and-css#knowledge-check)

This section contains questions for you to check your understanding of this lesson on your own. If you’re having trouble answering a question, click it and review the material it links to.

- [How do you select a specific element on your page with your browser’s developer tools?](https://www.theodinproject.com/lessons/foundations-inspecting-html-and-css#inspecting-elements)
- [What does a strikethrough in a CSS element mean in your browser’s developer tools?](https://www.theodinproject.com/lessons/foundations-inspecting-html-and-css#strikethrough)
- [How do you change CSS in real time on specific elements of a web page with your browser’s developer tools?](https://www.theodinproject.com/lessons/foundations-inspecting-html-and-css#testing-styles-in-the-inspector)

### [Additional Resources](https://www.theodinproject.com/lessons/foundations-inspecting-html-and-css#additional-resources)

This section contains helpful links to related content. It isn’t required, so consider it supplemental.

- [This article about how we can utilize css overview in the developer tools](https://www.freecodecamp.org/news/how-to-use-css-overview-in-chrome-developer-tools/) to check the colors, font styles, media-queries, etc. used on a particular webpage.