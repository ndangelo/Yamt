---
id: 59613
title: '2. How to make a website, Recapping front-end web development, But how do you write code?'
date: '2023-01-13T13:36:42-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=59613'
permalink: /how-to-make-a-website/
categories:
    - 'DMET 155 Introduction to Web Design'
    - 'Learn to Code Now'
---

…and what exactly is “front-end web development”?

Earlier we talked about the different programming languages and the two types of code, for front-end and back-end web development. The former creates the look and feel of websites, it’s how our users and customers interact with what we’ve made. The latter is how users’ information is processed. Our users don’t see what’s happening in this code, they put in some information such as their log-in details or their credit card number to pay for a course, the site takes that information and processes it. Our user then sees the next bit of front-end code, depending on what’s happened — for instance, if your login details are wrong, you’ll see a try again page, or if you’ve paid correctly, you’ll see a confirmation page.

The web development we’ll be talking about here is the front-end code. There are two reasons why we’ll be concentrating on this in the course. Firstly, it’s important to know how front-end code works and is put together before we tackle back-end code. Secondly, it’s easier to learn front-end code than back-end.

Recapping front-end web development

There are three different code languages in front-end web development: HTML, CSS and Javascript. Each one has a different role to play.

- HTML *is the structure of websites*
- CSS *is the style of websites*
- Javascript *is the actions of websites*

Having these definitions in mind is always handy in helping you decide where you are going to put your code.

If you want to add a new paragraph to your site, or you want to remove a heading, what you’re essentially doing is changing content. Therefore, the language you’d use for this is HTML.

If you want to change the typeface of the headings, or make the paragraphs a different color, this is changing how it looks (or the style of the page). Therefore, the language you’d do this in is CSS.

If you want to change how a user interacts with an input box, or you want things to move when a user scrolls down the page, you’re changing the user actions or the user interactivity. Therefore, the language you’d do this in is Javascript.

Sometimes it can get a little tricky to work out. Don’t worry though, as you’ll pick up where the distinctions are. For instance, if you want to make the site look different on a mobile screen compared with a desktop, where would you start? A clue is in the sentence — you want to make the site look different — so you’d change the CSS of your website.

However, you may have initially thought making the site look different on mobile and desktop would have been user interactivity, as it depends on how the user is looking at it. The delineation could become clear

by asking yourself, is the user interacting with the site or not? If they are interacting and changing the site after they’ve loaded it, it would be Javascript. If they’re just seeing the site on a mobile screen and not interacting with it, then it would be CSS.

Don’t worry too much about this issue just yet though. We’ll talk about it a little more later in the book.

But how do you write code?

If you’re reading this guide, I’m going to assume that you’re a human (hi to any aliens reading this too). On our laptops, iPads and phones, we have a bunch of files. On my phone, I have some music files of songs by awful 90s indie bands, I have some videos of Tony T (my kitty), some photos sneakily taken of other people’s dogs and lots, lots more.

What kind of files are they? Most likely, my music files are MP3s, my videos are .mov files and my images are JPGs. How do we know what kind of file they are? We look at the extension of the file. For example, a file called “tonythecat.jpg” has the ending “.jpg” so the computer

can take a guess it is a photo. Similarly, the computer would guess that “all-star-by-smashmouth.mp3” would be a music file because of the MP3 extension at the end of the file name.

What’s in a file?

All these photo, video and music files contain instructions for our laptops and phones to play or view them in a certain way. A photo file would contain a certain number of pixels and what color each pixel was, so the laptop could build up an image of Tony the cat. A music file would contain a description of the sound waves that the computer should play so I can listen to All Star by Smashmouth.

All of this is just code. Code is instructions for a particular program to run. My music app plays music files. My photo viewer shows me photos. I can’t play a photo in a music player because the music player doesn’t understand the instructions.

Websites are no different. The program that runs website code is called a browser. There are a few popular brand names of browser — Google Chrome, Firefox, Safari and Internet Explorer are the well known ones.

Browsers take code files that contain HTML, CSS and Javascript and turn them into visual websites for users to interact with.

So if a music file is a file that ends in “.mp3” and contains instructions to play music, website files are the same. The code for the content of a site is an HTML file, e.g. “about.html”, that contains HTML code. The code for the style of a site is a CSS file, e.g. “style.css”, that contains CSS code. The code for the user interactions of a site is a Javascript file,

e.g. “scroll.js”, that contains Javascript code.

Where are my files?

A decade ago, if you were to play music on your laptop or phone, you’d have the files stored on your device. You’d have a folder called something like “music” or “iTunes” that would live on your hard drive.

But if you’re looking at Google or Facebook, there isn’t a folder on your hard drive called “Google” or “Facebook”, so how are you getting to view these files?

If you want to play music in a more modern way, you’d use a streaming service like Spotify or Apple Music. With these services, you’re not having to download all the music ever created to be able to have access to every song ever. Instead, you’re streaming the songs using the Internet to the device when you need them. The songs aren’t stored on your hard drive any more, they’re stored on the Internet and you get them whenever you want them.

The same thing is due of web browsers. If you’re looking at Google or Facebook, you’re downloading HTML, CSS and Javascript files on demand. Essentially web browsers were the first streaming service.

What is streaming though?

Let’s take Spotify as an example. When you’re listening to a music file on Spotify, you’re requesting the file from Spotify’s very large hard drive (or server) instead of your own hard drive. You’re using the Internet between you and Spotify to stream the file.

Because you’re the one asking Spotify for the file using the Internet, this is called downloading.

On a site like Facebook, if I want to share a photo that’s on my phone and put it on Facebook’s very large hard drive/server, then I use the Internet between Facebook and me to upload the photo.

So all downloading really means is sending a file from someone else’s hard drive to my hard drive, and all uploading means is sending a file from my hard drive to someone else’s using the Internet.

[When you’re in a web browser like Google Chrome and you type in a web address like “www.go](http://www.google.com/)ogle.com”, all you’re telling the web browser to do is download files from Google’s server for the homepage. What files are we downloading? HTML, CSS and Javascript files to show us the content, style and actions for that page.

Wait! The Internet and the Web are different?

Most people just assume that the Internet and the Web (or World Wide Web to give it its full name) are the same thing. In reality, they’re two things.

The Internet is a service that connects hard drives or servers together.

For example, you need the Internet to play songs on Spotify but you don’t need to be in a web browser to use Spotify. Similarly, you don’t need to be in a web browser to use Instagram — most of the time,

Instagram’s users use the iPhone or Android app — not Chrome or Safari.

The Web is a subset of the Internet which deals mainly with HTML, CSS and Javascript files. We can pull other assets like images, videos and audio into our sites but they live within a web browser.

So why not just build an app? Why contain me in a browser?

The eternal question. When should I build for the Web and when should I build an app? This is a question that a lot of startup founders get really stuck with, and a lot go with what’s trendy over what would be best.

For a time in around 2006, Facebook pages were all the rage. I was working at a creative agency and pretty much every one of its clients had requested a Facebook page, even if it wasn’t suitable for the business. Why did they want it? Because their rivals had them so they wanted to join in the fun. Most of the time, they were a complete waste of money and their users didn’t really care.

Nowadays, apps are in a similar category — you can build them but you might be wasting your time.

Why build for the Web over building an app?

Firstly, with the Web you have 100 percent of the audience. Earlier in the book, we talked about mobile programming. If you want to build an app for iOS and Android, you’re essentially having to build two completely separate apps. Which, surprise surprise, takes twice as long. If you decide to do just one, you’re missing a big audience using whichever mobile platform you ignore.

Secondly, there’s no installation process with websites. If you look at the level of people who commit to installing an app once they’ve got to the installation page, it’s a pretty low percentage, so not only do you need to get people to the installation page, you need to get them over the hurdle of installing the app. The median average of apps installed

per person per month is zero. Most people do not install any new apps. The average American uses just three apps 80 percent of the time.

Thirdly, the publishing cycle for apps is up to the app stores and can be days and even weeks, whereas the Web is instant. Why let your customers and users wait for weeks for updates when you could do it instantly?

Lastly, discoverability is a lot tougher for apps. Most users are more likely to search via Google rather than an App Store.

Only recently have search engines like Google added apps to search results. It’s also a lot harder to share an app versus a link on social media. Ninety percent of apps are deleted after being opened just once.

So for four big points, the Web wins out: more audience, no installation, instant publishing and high discoverability.

Granted, there are certain instances where apps win out, such as offering complex functionality when using cameras or geolocation, but for 90 percent of new internet businesses, publishing a website over an app makes far more sense.

What is a code editor?

When we’re making our files, what program do we make them in? Is there a special program we need? If so, is it expensive?

Luckily for us, all the files that we’ll be making are essentially text files with a different extension. You can open them in Notepad, TextEdit, IA Writer or any program that you would write plain old text in.

Make a folder on your computer, then store all your code and assets in there.

There are, however, easier ways to edit code. There are specialist programs that make it simpler to see what’s happening when you write code.

Some of the most popular code editors include **Atom** (atom.io), **Sublime Text** (sublimetext.com), **Coda** (panic.com/coda) and **Dreamweaver** (adobe.com/dreamweaver). Some are free to download, some are paid for.

Insert product placement here

Now, usually I hate it when a company plugs their own products and tells you how great they are. I’m going to do just that, but I’ll keep it very brief.

After teaching hundreds of students, I noticed a few problems when beginners were coding with the popular code editors — the same typos, the same mistakes, the same problems with hosting — so as a team we felt we could fix this for our students.

We didn’t want our students feeling dumb and discouraged because they’d made a mistake. They should be able to be shown how to fix their own problems without needing to search on Google, ask a friend or give up. So we made our own code editor.

It’s aimed at beginners like you. We’ve been working on it for more than two years and all our students have been using it.

I won’t go into all the product features as we’re constantly making it better and better, but it includes instant hosting, live previews, version control, artificial intelligent helpers and lots more.

Try it for yourself at **editor.superhi.com** and tell us what you think.