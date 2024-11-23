---
id: 66330
title: 'Create a logo and icon set. III'
date: '2024-08-21T16:43:16-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=66330'
permalink: /create-a-logo-and-icon-set/
enclosure:
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_01.mp4\n346424\nvideo/mp4\n"
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_02.mp4\n166925\nvideo/mp4\n"
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_03.mp4\n560038\nvideo/mp4\n"
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_04.mp4\n866669\nvideo/mp4\n"
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_05.mp4\n1576309\nvideo/mp4\n"
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_06.mp4\n896807\nvideo/mp4\n"
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_07.mp4\n1940904\nvideo/mp4\n"
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_08.mp4\n3027168\nvideo/mp4\n"
    - "https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_09.mp4\n4018091\nvideo/mp4\n"
categories:
    - UI/UX
---

Figma 101: Create a logo and icon set. (n.d.). Retrieved from https://designlab.com/figma-101-course/create-a-logo-and-icon-set

Build a simple logo and icon set using shapes and the Pen tool.

## Learning objectives:

- Combine shapes using “Boolean operations.”
- Explore the Pen tool
- Discover the power of vector networks
- Please design a logo for our app
- Begin creating a set of icons

**Time to complete:** 30 minutes

## Today’s tutorial

Today, we will create a logo and some icons for our app, using shapes and Figma’s Pen tool’s exciting “vector network” functionality. (More about that later.)

### 1. Open up your Figma file, and create a new Frame

Let’s open up the same file in Figma and add today’s work. Generally, keeping all of the work for a project in a single file makes sense because it allows us to move easily and duplicate elements between Frames. As we’ll see on Day 5, it’s also crucial when it comes to creating app prototypes.

For today, though, let’s hit F and create a new iPhone 8 SE. We’re not going to make the next app screens until tomorrow, but today, we’ll use this blank Frame to create our logo and icons.

### 2. Draw a rectangle for the camera body

Inspired by Instagram’s logo, let’s create a little camera logo just using shapes. This is as simple as stacking a couple of circles on top of a rectangle. First, press R, and drag a rectangle 64 pixels by 64 pixels. If the size isn’t quite right, you can tweak it by changing the size values in the Properties panel to the right, or by resizing the rectangle using the resize handles.

<figure class="wp-block-video"><video controls="" loop="" muted="" playsinline="" preload="none" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_01.mp4"></video></figure>‍

### 3. Round the corners of the rectangle

Next, round the corners of the rectangle just like we did on Day 1 when we made our button. This time, set the corner radius to be 18 pixels.

<figure class="wp-block-video"><video controls="" loop="" muted="" playsinline="" preload="none" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_02.mp4"></video></figure>‍

### 4. Draw a circle for the camera lens

Then, press O to select the ellipse (circle/oval) tool. Click and drag to create a circle that’s 32 pixels by 32 pixels. You can hold down Shift ⇧ while doing this to “constrain” the shape—meaning that that height and width stay the same. Set it to have a white fill color so that we can see it on top of the rectangle.

<figure class="wp-block-video"><video controls="" loop="" muted="" playsinline="" preload="none" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_03.mp4"></video></figure>‍

### 5. Align the two shapes horizontally and vertically

Zoom in a bit and then click and drag a marquee around the two shapes you just made. At the top of the Properties panel, select the “Align Horizontal Centers” and “Align Vertical Centers” buttons.

<figure class="wp-block-video"><video controls="" loop="" muted="" playsinline="" preload="none" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_04.mp4"></video></figure>‍

### 6. Create another circle for the light meter

Finally, create another circle, this time 8 pixels by 8 pixels, and set that to have a white fill, too. Position it at the top-right of the rectangle shape (4 pixels from the top and 4 pixels from the right). Pro tip: You can check the position of any shape relative to another shape by selecting it, holding down Option (Mac) or Alt (PC), and hovering over a second shape.

<figure class="wp-block-video"><video controls="" loop="" muted="" playsinline="" preload="none" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_05.mp4"></video></figure>‍

### 7. Use “Boolean operations” to turn the camera into a single shape

There’s a group of commands in Figma called “Boolean operations”. These allow you to take two or more shapes and unite them into a single shape, or subtract one shape from the other, or even isolate where the shapes overlap.

For our camera logo, let’s click and drag to select all of the three shapes we just created—the rounded rectangle and the two circles. Then, click the tiny arrow next to the “Boolean Groups” icon in the middle of the toolbar at the top, and select “Subtract Selection”:

Finally, use the Flatten command to convert the camera into a single vector object. With the logo selected, Hit ⌘E (Mac) or CtrlE (PC). This will cause the shape to resize correctly.

<figure class="wp-block-video"><video controls="" loop="" muted="" playsinline="" preload="none" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_06.mp4"></video></figure>‍

### 8. Create a 3D box using the Pen tool

So far today, we’ve created a logo using shapes and Boolean operations. But we can also draw using the Pen tool—and in Figma, the Pen tool has superpowers, aka “vector networks.” To understand vector networks, here’s a bit of background info.

In most graphics applications, including Photoshop, Illustrator, and Sketch, there is a Pen tool (sometimes called the vector tool). New users usually view the pen tool with suspicion because it’s not intuitive.

One reason for this is that in these other programs, the Pen tool is entirely linear: the points in a shape could only be connected A to B to C to D, and so forth. Paths could be “closed” by being joined back up to their starting point, but that was it.

Figma has redesigned the Pen tool to add “vector network” functionality. This means that a single point can now be connected to several other points. Also, when it comes to setting a fill color for a vector shape, you can choose which of the enclosed areas within the shape the fill will apply to.

For example, here’s how we drew a 3D box using vector networks. We recommend turning on Pixel Grid— ⌘’ on Mac, or Ctrl’ on PC—and adding a square-based Layout Grid to the Frame, giving you a visual guide for placing and aligning your points.

<figure class="wp-block-video"><video controls="" loop="" muted="" playsinline="" preload="none" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_07.mp4"></video></figure>‍Notice how, once we’d completed the first enclosed space, we had to select a previously created point to tell Figma which point we wanted the next point to connect to. When hovering over a point you’ve already made, you can see a black dot just below your cursor, indicating that you’re about to add to the vector network. If in doubt, click an existing point, and that will define the connection for the next point you add. Now try it yourself!

### 9. Create a set of icons

Once you’ve experimented a little with vector networks by drawing that 3D box, let’s go ahead and create a simple icon set! Using the vector network functionality, draw an envelope icon, a home icon, and a back arrow.

Note: because points don’t have to be connected in Figma’s Pen tool, it’s easy to accidentally create multiple shapes within the same vector element. So once you’ve completed one icon, exit that shape by clicking “Done” in the toolbar at the top of the interface. You’ll then need to re-select the pen tool and start on the next icon.

Here’s how we went about it:

<figure class="wp-block-video"><video controls="" loop="" muted="" playsinline="" preload="none" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_08.mp4"></video></figure>‍

### 10. Practice moving points, adding midpoints, and deleting points

After you’ve clicked “Done” (or have hit Escape), you can double-click on a vector network to edit it. Once you’ve re-entered vector edit mode, you can move individual or multiple points at once, add midpoints to lines, and delete points without breaking the network.

- To move multiple points while in vector edit mode, click and drag a marquee around a series of points you’d like to move. Grab one of the selected points or a line extending from one of the selected points and drag to move it.
- To add a midpoint to a line segment, hover your cursor over a line you’d like to edit. Click on the white circle on the line (your cursor will also show a “+” symbol). Now, you can grab the Pen tool and draw a line starting from that new point. Or, you can grab it and move it around.
- To delete a point without breaking the network, you must be in vector edit mode and have the Pen tool selected. Only then can you hold Option (Mac) or Alt (PC) and click on a point you wish to remove without deleting a whole section of lines. Using the Delete key removes all lines connected to that point you deleted. The video below demonstrates both scenarios and the first two tips.
- 

<figure class="wp-block-video"><video controls="" loop="" muted="" playsinline="" preload="none" src="https://storage.designlab.com/email-courses/figma-101/2023/F101_D3_09.mp4"></video></figure>Figma 101: Create a logo and icon set. (n.d.). Retrieved from https://designlab.com/figma-101-course/create-a-logo-and-icon-set