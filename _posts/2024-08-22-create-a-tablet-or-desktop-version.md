---
id: 66345
title: 'Create a Tablet or Desktop Version VI'
date: '2024-08-22T14:29:49-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=66345'
permalink: /create-a-tablet-or-desktop-version/
enclosure:
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D6_04.mp4\n458217\nvideo/mp4\n"
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D6_05.mp4\n2467163\nvideo/mp4\n"
categories:
    - Projects
---

Figma 101: Create a Tablet or Desktop Version. (n.d.). Retrieved from https://designlab.com/figma-101-course/create-a-tablet-or-desktop-version

Unleash your creativity to adapt your design to tablet or desktop size!

## Learning objectives:

- Learn about Constraints
- Research some tablet or desktop design patterns
- Practice adapting the mobile app design for a larger screen size
- Consolidate your app design and prototyping skills

## Today’s tutorial

Today, we’re setting you free! It’s time to get creative and make your designs for a tablet or desktop version of the app by adapting your existing layouts for a different screen size.

Just before you get started, though, let’s cover one more awesome feature in Figma: constraints. This is particularly useful when transposing a design from one device or screen size to another.

Constraints define how any object will behave if the frame it contains is resized. Each Layer in Figma actually has Constraints set by default—select any object in the canvas, and you’ll be able to see these settings in the Properties panel under the Design tab:

<div class="wp-block-image"><figure class="aligncenter">![The constraints panel](https://cdn.prod.website-files.com/65130e79c72ae8812db3412e/6580ac5c6ab4733f9f44c13a_F101_D6_01.jpeg)</figure></div>The first dropdown (which here says “Left”) tells Figma how to manage the object’s horizontal position, while the second dropdown (which by default says “Top”) sets its vertical position.

<div class="wp-block-image"><figure class="aligncenter">![The Figma menu](https://cdn.prod.website-files.com/65130e79c72ae8812db3412e/6580ac5b6ab4733f9f44c0e4_F101_D6_02.jpeg)</figure></div>The advantage of Constraints is that we can use them to resize our designs intelligently, which saves us the work of scaling and positioning elements manually. As an example, follow these steps to make the nav bar resizable.

Click and drag to select all the elements in the nav bar. Group those elements with ⌘G (Mac) or CtrlG (PC). Then, convert the new Group to a Frame using the dropdown menu near the top of the Properties panel. In Figma, Frames can be nested—meaning that one Frame can contain another Frame. Rename this new Frame “Nav Bar”.  
  
<video controls="" height="auto" loop="" muted="" poster="https://storage.designlab.com/email-courses/figma-101/2023/F101_D6_03_poster.jpg" preload="none" width="100%"></video>

2\. Next, let’s set the constraints for how the Nav Bar Frame will relate to its container, the Profile Frame. With the Nav Bar Frame selected, change the Constraints settings to “Left &amp; Right” and “Bottom,” respectively. This means that Figma will preserve the Nav Bar’s position relative to both left and right edges and keep it tethered to the bottom edge of the Frame.

<figure class="wp-block-video"><video controls="" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D6_04.mp4"></video></figure>3\. Finally, we need to set how the objects within the Nav Bar relate to their container. Double-click the Nav Bar Frame, select each object in turn, and set their Constraints to the following:

- Background rectangle: Left &amp; Right, Bottom
- Camera icon: Center, Bottom
- Back arrow: Left, Bottom
- Hamburger button: Right, Bottom

<figure class="wp-block-video"><video controls="" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D6_05.mp4"></video></figure>4\. Try grabbing a corner of the Profile Frame and resizing it to see what happens. Presto! A nav bar that resizes and scales correctly and stays pinned to the bottom of the Frame.

You can apply this method to other screen elements as you develop your tablet or desktop app version. To get you started with today’s challenge, first decide on how many screens you’d like to recreate at a larger scale. Don’t feel obligated to do all four, but give at least two a try. Here are some specifications for the Frames and Layout Grids for your chosen device:

### Tablet (landscape):

1. Hit F to select the Frame tool
2. Click the “Tablet” drill-down menu in the Inspector
3. Select “iPad Pro 11”
4. Once the Frame has been created, switch the orientation to Landscape at the top of the Properties panel, next to the drop-down we used earlier to switch a Group into a Frame
5. In the Properties panel, add a Layout Grid like we’ve done before. Set it to columns with a Count of 12, the Margin at 16, and the Gutter at 32.

<div class="wp-block-image"><figure class="aligncenter">![Frame orientation](https://cdn.prod.website-files.com/65130e79c72ae8812db3412e/6580ac5b6ab4733f9f44c0e1_F101_D6_06.jpeg)</figure></div>‍

### Desktop:

1. Hit F to select the Frame tool
2. Click the “Desktop” drill-down menu in the Inspector
3. Click “Desktop (1440 \* 1024)”
4. In the Properties panel, add a Layout Grid like we’ve done before. Please set it to Columns and then change the Type to Center, the Width to 74, and the Gutter to 32.
5. In the Properties panel, add a Layout Grid like we’ve done before. Please set it to columns with a Count of 12, the Margin at 16, and the Gutter at 32.

<div class="wp-block-image"><figure class="aligncenter">![The Figma menu](https://cdn.prod.website-files.com/65130e79c72ae8812db3412e/6580ac5b6ab4733f9f44c0de_F101_D6_07.jpeg)</figure></div>Tip: When translating your work from mobile to tablet or desktop, it’s helpful to have the original mobile screen design next to the new Frame you’re working on. You can copy elements across or use them as a point of reference.

Here’s a checklist to keep in mind as you work on this:

- As a user, what might you want to be consistent between the app’s mobile and tablet/desktop versions? (Perhaps color or certain layout patterns, like those on the Photo Post screen?)
- Equally, what might you want to be different? (How might navigation and menus be different on tablet or desktop?)
- Take a look at other websites or apps to get a sense of how the relative scale, sizing, and spacing of elements might need to be different on a larger device.
- Check out the site UI Patterns for some inspiration on how you might want to lay out elements in a different format: [ui-patterns.com](http://ui-patterns.com/).
- 

Figma 101: Create a Tablet or Desktop Version. (n.d.). Retrieved from https://designlab.com/figma-101-course/create-a-tablet-or-desktop-version