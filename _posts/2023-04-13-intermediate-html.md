---
id: 62734
title: 'Intermediate HTML'
date: '2023-04-13T07:23:00-04:00'
author: admin
layout: post
guid: 'https://www.nuggetofjoy.com/?p=62734'
permalink: /intermediate-html/
categories:
    - Projects
---

# Beginning of Intermediate HTML

# Span and Div

HTML is all about applying **meaning** to content. Whereas most HTML tags apply meaning ([`p`](https://www.htmldog.com/references/html/tags/p/) makes a paragraph, [`h1`](https://www.htmldog.com/references/html/tags/h1h2h3h4h5h6/) makes a heading etc.), the [`span`](https://www.htmldog.com/references/html/tags/span/) and [`div`](https://www.htmldog.com/references/html/tags/div/) tags apply no meaning at all. This might sound about as useful as a foam hammer but they are actually used quite extensively in conjunction with CSS.

They are used to group together a chunk of HTML and hook some information onto that chunk, most commonly with the attributes `class` and `id` to associate the element with a [class or id CSS selector](https://www.htmldog.com/guides/css/intermediate/classid/).

The difference between [`span`](https://www.htmldog.com/references/html/tags/span/) and [`div`](https://www.htmldog.com/references/html/tags/div/) is that a [`span`](https://www.htmldog.com/references/html/tags/span/) element is **in-line** and usually used for a small chunk of HTML inside a line (such as inside a paragraph) whereas a [`div`](https://www.htmldog.com/references/html/tags/div/) (division) element is **block-line** (which is basically equivalent to having a line-break before and after it) and used to group larger chunks of code.

```markup

<div id="scissors">
    <p>This is <span class="paper">crazy</span></p>
</div>

```

[`div`](https://www.htmldog.com/references/html/tags/div/), and especially [`span`](https://www.htmldog.com/references/html/tags/span/), shouldn’t actually be used that often. Whenever there is a sensible alternative that should be used instead. For example, if you want to emphasize the word “crazy” and the class “paper” is adding italics for visual emphasis, then, for richer, more meaningful content, the code might look like this:

```markup

<div id="scissors">
    <p>This is <strong><em class="paper"></strong>crazy<strong></em></strong></p>
</div>

```

If you haven’t got a clue about classes and ID’s yet, don’t worry, they’re all [explained in the CSS Intermediate Tutorial](https://www.htmldog.com/guides/css/intermediate/classid/). All you need to remember is that span and div are “meaningless” tags.

While they are not replacement for the [`div`](https://www.htmldog.com/references/html/tags/div/) tag, HTML 5 introduces a number of tags used for grouping blocks of code together and adding meaning at the same time. For more information on [`article`](https://www.htmldog.com/references/html/tags/article/), [`header`](https://www.htmldog.com/references/html/tags/header/), [`footer`](https://www.htmldog.com/references/html/tags/footer/), and more, see the [article about sectioning](https://www.htmldog.com/guides/html/intermediate/sectioning/).

# Beginning of Intermediate HTML

# Text: Abbreviations, Quotations, and Code

The basics of defining text using paragraphs (as well as emphasis and line breaks) and headings was covered in the HTML Beginner Tutorial. And for the same reason we use [`p`](https://www.htmldog.com/references/html/tags/p/) and `h1`, `h2`, etc, there are a number of other tags we should also use to specifically represent other text-types, such as **abbreviations**, **quotations**, and computer **code**.

## Abbreviations

`abbr` is used to markup an abbreviation, a shortened form of a word or phrase.

The expanded phrase that the abbreviation represents can be defined in the value of the `title` attribute. This is optional but recommended.

```markup

<p>This web site is about <strong><abbr title="HyperText Markup Language">HTML</abbr></strong> and <strong><abbr title="Cascading Style Sheets">CSS</abbr></strong>.</p>

```

## Quotations

[`blockquote`](https://www.htmldog.com/references/html/tags/blockquote/) and [`q`](https://www.htmldog.com/references/html/tags/q/) are used for quotations. [`blockquote`](https://www.htmldog.com/references/html/tags/blockquote/) is generally used for standalone often multi-line quotations whereas [`q`](https://www.htmldog.com/references/html/tags/q/) is used for shorter, in-line quotations.

If the source of the quotation can be found on the Web, the `cite` attribute can be used to point to its origin.

```markup

<p>So I asked Bob about quotations on the Web and he said <strong><q>I know as much about quotations as I do about pigeon fancying</q></strong>. Luckily, I found HTML Dog and it said:</p>

<strong><blockquote cite="https://</strong>ndangelo.com<strong>"></strong>
    <p>blockquote and q are used for quotations. blockquote is generally used for standalone often multi-line quotations whereas q is used for shorter, in-line quotations.</p>
<strong></blockquote></strong>

```

Blockquotes work very nicely with the HTML5 elements [`figure`](https://www.htmldog.com/references/html/tags/figure/) and [`figcaption`](https://www.htmldog.com/references/html/tags/figcaption/), enabling a nice, semantic way to group a quotation with a citation:

```markup

<figure>
    <blockquote>[Big old quotation about evolution]</blockquote>
    <figcaption>Charles Darwin</figcaption>
</figure>

```

But let’s not get carried away with that here – see the [article about Sectioning](https://www.htmldog.com/guides/html/intermediate/sectioning/) for more.

## Citations

Just to make things nice and confusing, as well as a `cite` attribute, there is also a [`cite`](https://www.htmldog.com/references/html/tags/cite/) tag. This can be used to define the title of a work, such as a book.

```markup

<p>According to <strong><cite>the Bible</cite></strong>, after six days God said <q>screw this for a lark, I'm having a nap</q>.</p>

```

## Code

[`code`](https://www.htmldog.com/references/html/tags/code/) is used to represent any form of computer **code**. Further, [`var`](https://www.htmldog.com/references/html/tags/var/) can be used for **variables** (which could be a variable in anything, not just in code – it could be a variable in an equation, for example), [`samp`](https://www.htmldog.com/references/html/tags/samp/) for sample **output**, and [`kbd`](https://www.htmldog.com/references/html/tags/kbd/) (keyboard) for user **input**.

```markup

<p>If you add the line <strong><var>givevaderachuckle</var> = true;</strong> to the <strong>destroy_planet</strong> subroutine and then type <strong><kbd>ilovejabba</kbd></strong> into the console, the big bad green Death Star laser will etch <strong><samp>Slug Lover!</samp></strong> on the planet's surface.</p>

```

## Preformatted text

[`pre`](https://www.htmldog.com/references/html/tags/pre/) is **preformatted** text and is unusual in HTML tags that it takes notice of every character in it, including the white space (whereas other elements will ignore a consecutive space or a line-break, for example). It is most commonly used for blocks of code, where spacing, such as indentations, can be relevant.

```markup

<strong></strong>
&lt;div id="intro"&gt;
    &lt;h1&gt;Some heading&lt;/h1&gt;
    &lt;p&gt;Some paragraph paragraph thing thing thingy.&lt;/p&gt;
&lt;/div&gt;
<strong></strong>

```

As an example, [`pre`](https://www.htmldog.com/references/html/tags/pre/) and [`code`](https://www.htmldog.com/references/html/tags/code/) are used extensively throughout this site. The code blocks, such as the one above, are [`code`](https://www.htmldog.com/references/html/tags/code/) elements inside [`pre`](https://www.htmldog.com/references/html/tags/pre/) elements. In-line references to tags and properties are simply [`code`](https://www.htmldog.com/references/html/tags/code/) elements, often inside [`a`](https://www.htmldog.com/references/html/tags/a/) elements to link to [the reference section](https://www.htmldog.com/references/).

# Meta Tags

Once upon a time, many eons ago, when the Internet was just a small number of cardboard boxes attached to each other with string, **meta tags** were the town criers of the Internet… erm… town.

Meta tags don’t do anything to the content presented in the browser window, but search engines use them to catalog information about the web page.

There is one [`meta`](https://www.htmldog.com/references/html/tags/meta/) tag which can be used as many times as you desire inside a `head` element and they can contain the attributes `charset`, `name`, `http-equiv`, and `content`.

When the `name` or `http-equiv` attribute is used, which is then used in conjunction with them to apply meta data.

## Names

The `name` attribute can be anything you like. The most commonly used names are `author`, `description`, and `keywords`. `author` is used to explicitly state one of the HTML page’s authors and `description` is often used by search engines (such as Google) to display a web page description in its search results.

The reason why [`meta`](https://www.htmldog.com/references/html/tags/meta/) tags used to be so important was because they were relied on by search engines to build a profile of a web page. The `keywords` meta data was used (and abused) extensively, for example. Nowadays, however, most search engines use the actual content of the page itself.

## HTTP Equivalents

The `http-equiv` attribute can be used instead of the `name` attribute and will make an HTTP header, which is information sent to the server where the web page is held. The **attribute** should rarely be used (although see `charset` note, below) but the value can be:

- `content-type`, an encoding declaration, defining what character set is being used,
- `default-style`, the preferred stylesheet from a selection of [`link`](https://www.htmldog.com/references/html/tags/link/) or [`style`](https://www.htmldog.com/references/html/tags/style/) elements,
- or `refresh`, which defines how often (in seconds) a page automatically refreshes or if it should automatically redirect to another page. Not great for accessibility.

The charset attribute can be used as a shorthand method to define an HTML document’s character set, which is always a good thing to do. `<meta charset="utf-8">` is the same as `<meta http-equiv="content-type" content="text/html; charset=utf-8">`.

```markup

<head>
    <title>Air conditioners? YEAH conditioners!</title>
<strong>    <meta charset="utf-8"></strong>
<strong>    <meta http-equiv="refresh" content="3"></strong><!--not recommended for sane people-->
<strong>    <meta name="description" content="This is my really, really, REALLY exciting web page about air conditioners"></strong>
    ...

```

# Tables: rowspan and colspan

**Tables** may have seemed complicated enough [in the HTML Beginner Tutorial](https://www.htmldog.com/guides/html/beginner/tables/). It can be quite difficult to visualize a two-dimensional grid from one-dimensional lines of code.

Well, it gets trickier. All thanks to the `rowspan` and `colspan` attributes. Those bastards.

The following code is similar to that in [the Tables page of the HTML Beginner Tutorial](https://www.htmldog.com/guides/html/beginner/tables/):

```markup

<table>
    <tr>
        <strong><th></strong>Column 1 heading<strong></th></strong>
        <strong><th></strong>Column 2 heading<strong></th></strong>
        <strong><th></strong>Column 3 heading<strong></th></strong>
    </tr>
    <tr>
        <td>Row 2, cell 1</td>
        <td <strong>colspan="2"</strong>>Row 2, cell 2, also spanning Row 2, cell 3</td>
    </tr>
    <tr>
        <td <strong>rowspan="2"</strong>>Row 3, cell 1, also spanning Row 4, cell 1</td>
        <td>Row 3, cell 2</td>
        <td>Row 3, cell 3</td>
    </tr>
    <tr>
        <td>Row 4, cell 2</td>
        <td>Row 4, cell 3</td>
    </tr>
</table>

```

The first difference is that the [`td`](https://www.htmldog.com/references/html/tags/td/) tags of the first row have been replaced with [`th`](https://www.htmldog.com/references/html/tags/th/) tags. Whereas a [`td`](https://www.htmldog.com/references/html/tags/td/) is a standard **data** cell, [`th`](https://www.htmldog.com/references/html/tags/th/) is a **header** cell. As with [`td`](https://www.htmldog.com/references/html/tags/td/) elements, these must be enclosed inside [`tr`](https://www.htmldog.com/references/html/tags/tr/) elements.

## Spanning columns and rows

`colspan` and `rowspan` attributes have also been used in some of the [`td`](https://www.htmldog.com/references/html/tags/td/) tags. If you look at this code in a browser, you will see that on the second row there are now two cells instead of three, the second cell spanning the second and third column. The `colspan` attribute, which means “column span” will span the cell over the number of cells that is specified. This means, in this example, that there is no need for a third [`td`](https://www.htmldog.com/references/html/tags/td/) element — two cells are **merged** into one.

The `rowspan` attribute is similar to `colspan`, except, obviously, it will span across rows rather than columns. Again, the cells that it spans should be removed. In this example, because it spans over the fourth row, there are only two cells in that row.

As with the simpler 3×4, 12-cell table, the numbers on these tables with merged cells should also add up. Although there are only 10 cells in this example, there are 2 spans.

# Description Lists

**Description lists** are quite often forgotten. This is maybe because they are much more specific than ordered and unordered lists and therefore less useful, generally, but where there is a list of terms and descriptions (such as a glossary), a description list is your go-to-element.

[`dl`](https://www.htmldog.com/references/html/tags/dl/) gets the ball rolling, similar to the [`ul`](https://www.htmldog.com/references/html/tags/ul/) and [`ol`](https://www.htmldog.com/references/html/tags/ol/) elements, establishing the list. Rather than containing [`li`](https://www.htmldog.com/references/html/tags/li/) elements, though, description lists have [`dt`](https://www.htmldog.com/references/html/tags/dt/) elements, which are the **terms**, followed by [`dd`](https://www.htmldog.com/references/html/tags/dd/) elements, which are the **descriptions** associated to the [`dt`](https://www.htmldog.com/references/html/tags/dt/) elements.

There doesn’t have to be one [`dt`](https://www.htmldog.com/references/html/tags/dt/) followed by one [`dd`](https://www.htmldog.com/references/html/tags/dd/), there can be any number of either. For example, if there are a number of words that have the same meaning, there might be a number of [`dt`](https://www.htmldog.com/references/html/tags/dt/)’s followed by one [`dd`](https://www.htmldog.com/references/html/tags/dd/). If you have one word that means various different things, there might be one [`dt`](https://www.htmldog.com/references/html/tags/dt/) followed by several [`dd`](https://www.htmldog.com/references/html/tags/dd/)’s.

```markup

<h1>Some random glossary thing</h1>
<dl>
    <dt>HTML</dt>
    <dd>Abbreviation for HyperText Markup Language - a language used to make web pages.</dd>

    <dt>Dog</dt>
    <dd>Any carnivorous animal belonging to the family Canidae.</dd>
    <dd>The domesticated sub-species of the family Canidae, Canis lupus familiaris.</dd>

    <dt>Moo juice</dt>
    <dt>Cat beer</dt>
    <dt>Milk</dt>
    <dd>A white liquid produced by cows and used for human consumption.</dd>
</dl>
```

# Text: Addresses, Definitions, Bi-directional, and Editorial

OK, so we should all be know by now that there are lots of tags for text. We’ve done paragraphs, we’ve done headings, we’ve even done abbreviations, quotations, and code. And there are several other, more obscure tags that can be used. Obscure because you won’t find them plastered around the Web, not because they are unhelpful. If you find you have text that fits these elements’ descriptions, you will have a nicer, richer, more meaningful HTML page if you use them.

## Addresses

`address` should be used specifically for the **contact details** relating either to the entire web page (and so only used once) or to an `article` element (see Sectioning). It’s isn’t, as it might at first appear, for marking up any old address willy-nilly.

```markup
<h3>Author contact details</h3>
<strong><address></strong>
<ul>
    <li>0123-456-7890</li>
    <li>author_dude@noplaceinteresting.com</li>
    <li>http://www.noplaceinteresting.com/contactme/</li>
</ul>
<strong></address></strong>
```

## Definition terms

[`dfn`](https://www.htmldog.com/references/html/tags/dfn/) is a **definition** term and is used to highlight the first use of a term. Like [`abbr`](https://www.htmldog.com/references/html/tags/abbr/), the `title` attribute can be used to describe the term.

```markup

<p>Bob's <strong><dfn title="Dog">canine</dfn></strong> mother and <strong><dfn title="Horse">equine</dfn></strong> father sat him down and carefully explained that he was an <strong><dfn title="A mutation that combines two or more sets of chromosomes from different species">allopolyploid</dfn></strong> organism.</p>

```

## Bi-directional text

[`bdo`](https://www.htmldog.com/references/html/tags/bdo/) can be used to reverse the **direction** of the text, and can be used to display languages that read right to left. The value of the required attribute `dir` can be `ltr` (left to right) or `rtl` (right to left).

```markup

<bdo dir="rtl">god lmth</bdo>

```

## Editorial

[`ins`](https://www.htmldog.com/references/html/tags/ins/) and [`del`](https://www.htmldog.com/references/html/tags/del/) are used to display editorial **insertions** and **deletions** respectively. Strictly speaking, they aren’t limited to text and can be used over whole swathes of content but, typically, they are used in moderation just like “Track Changes” feature in word processors tend to be.

They can have the attributes `datetime` to indicate when the edit was made and `cite`, to point to a description as to why the edit has been made.

```markup

<p>I have decided to <strong><del datetime="2013-01-26">decrease</del></strong> <strong><ins cite="http://www.icecreamforall.com/changeofpolicy/">increase</ins></strong> the amount of free ice cream that the State will provide for its citizens.</p>

```

As with traditional word processor-based editing, the [`ins`](https://www.htmldog.com/references/html/tags/ins/) element is typically shown **underlined** and the [`del`](https://www.htmldog.com/references/html/tags/del/) element is usually displayed with a **strikethrough**.

And there’s yet more… HTML 5 brings with it even more text-related elements. See the [final article on text in the HTML Advanced Guide](https://www.htmldog.com/guides/html/advanced/text), complete with a look at the reclassification of the dreaded “presentational” elements.

# Sectioning

While [headings](https://www.htmldog.com/guides/html/beginner/headings/) do a grand, perfectly valid, job in defining the **start** of a new section or sub-section in a document, there are a number of elements that can be exploited to establish a cleaner, clearer semantic structure.

Whereas div elements can be used to contain sections, used primarily as scaffolding on which to hang CSS, they don’t hold a great deal of **meaning**. Sectioning involves a handful of tags that can be used to define specific parts of a page, such as **articles**, **headers**, **footers**, and **navigation**.

## Articles and Sections

An [`article`](https://www.htmldog.com/references/html/tags/article/) element can be used to mark up a **standalone section** of content. This could be used just once, if you think of a blog post as an article, for example, or a number of times, if you imagine replicating a traditional newspaper page with numerous articles.

A [`section`](https://www.htmldog.com/references/html/tags/section/) element represents a more **general section** and could be used to split up an article, or to represent chapters, for example.

```markup

<strong><article></strong>
    <strong><section id="intro"></strong>
        <p>[An introduction]</p>
    <strong></section></strong>
    <strong><section id="main_content"></strong>
        <p>[Content]</p>
    <strong></section></strong>
    <strong><section id="related"></strong>
        <ul>
            <li><a href="that.html">That related article</a></li>
            <li><a href="this.html">This related article</a></li>
        </ul>
    <strong></section></strong>
<strong></article></strong>

```

While [`div`](https://www.htmldog.com/references/html/tags/div/)s could be used to make these separations (or even if you didn’t need these separations for styling), this provides a much richer, more meaningful document.

The HTML5 specifications suggest that you can use [`h1`](https://www.htmldog.com/references/html/tags/h1h2h3h4h5h6/) elements at the start of each section, which would become a sub-heading of anything preceding that section (so, in the example above, if you had an [`h1`](https://www.htmldog.com/references/html/tags/h1h2h3h4h5h6/) immediately following the opening [`article`](https://www.htmldog.com/references/html/tags/article/) tag, an [`h1`](https://www.htmldog.com/references/html/tags/h1h2h3h4h5h6/) immediately after an opening [`section`](https://www.htmldog.com/references/html/tags/section/) tag would be a **sub-heading** of that initial [`h1`](https://www.htmldog.com/references/html/tags/h1h2h3h4h5h6/)). This screws backwards compatibility, however, and any user agents (including screen readers) that don’t understand this won’t apply properly structured heading levels. We suggest sticking to the headings levels you would use if you didn’t use sections (so [`h1`](https://www.htmldog.com/references/html/tags/h1h2h3h4h5h6/), followed by [`h2`](https://www.htmldog.com/references/html/tags/h1h2h3h4h5h6/), etc, regardless of the sectioning). This doesn’t break anything or detract from the meaning or semantics.

## Headers and Footers

[`header`](https://www.htmldog.com/references/html/tags/header/) and [`footer`](https://www.htmldog.com/references/html/tags/footer/) provide further specialized, self-descriptive, sections:

```markup

<body>
<article>
    <strong><header></strong>
        <h1>Alternatively&hellip;</h1>
        <p>[An introduction]</p>
    <strong></header></strong>
    <section id="main_content">
        <p>[Content]</p>
    </section>
    <strong><footer></strong>
        <p>[End notes]</p>
    <strong></footer></strong>
</article>
<strong><footer></strong>
    <p>[Copyright bumf]</p>
<strong></footer></strong>
</body>

```

The [`footer`](https://www.htmldog.com/references/html/tags/footer/) is the footer of the section in which it is contained. So, in the above example, the first [`footer`](https://www.htmldog.com/references/html/tags/footer/) is the footer of the article and the second [`footer`](https://www.htmldog.com/references/html/tags/footer/) is the footer of the page.

## Asides

An [`aside`](https://www.htmldog.com/references/html/tags/aside/) can be used to represent content that is **related** the content surrounding it. Think of pull-quotes or snippets of related information in an article:

```markup

<section id="main_content">
    <h1>Tixall</h1>
    <p>[All about Tixall]</p>
    <strong><aside></strong>
        <h2>Tixall Obelisk</h2>
        <p>[A short note about Tixall Obelisk]</p>
    <strong></aside></strong>
    <p>[Maybe a bit more about Tixall]</p>
</section>

```

While we’re at this structure-love, if you want to include figures, there happens to be two tags for doing just that:

```markup

<strong><figure></strong>
    <img src="obelisk.jpg">
    <strong><figcaption></strong>Tixall Obelisk<strong></figcaption></strong>
<strong></figure></strong>

```

Note that the [`img`](https://www.htmldog.com/references/html/tags/img/) element doesn’t need an `alt` attribute IF the [`figcaption`](https://www.htmldog.com/references/html/tags/figcaption/) (that’s “figure caption”, in case you need it spelling out) does that job.

## Navigation

Finally, there’s [`nav`](https://www.htmldog.com/references/html/tags/nav/), used to mark up a group of **navigation links**:

```markup

<strong><nav id="main_nav"></strong>
    <ul>
        <li><a href="/tutorials/">Tutorials</a></li>
        <li><a href="/techniques/">Techniques</a></li>
        <li><a href="/examples/">Examples</a></li>
        <li><a href="/references/">References</a></li>
    </ul>
<strong></nav></strong>

```

This could also be used for in-page navigation (`<a href="#overthere">...` etc.) but it isn’t necessary for every group of links – it is designed for major groupings. A copyright, author, and contact link could sit happily by themselves in a [`footer`](https://www.htmldog.com/references/html/tags/footer/) element, for example.

If you want to style these new HTML 5 elements (and you probably do, right? It’s much nicer than using `<div id="content">...`, etc) you will experience a problem in older browsers, most notably Internet Explorer versions 8 and earlier, that don’t understand these tags.

[HTML5Shiv](https://code.google.com/p/html5shiv/) can come to your rescue, however; a small piece of JavaScript, slotted in to your [`head`](https://www.htmldog.com/references/html/tags/head/) element, that teaches the remedial browsers and holds their hands so that you can use new HTML 5 tags and style them up to your heart’s content with CSS.

It’s your call if you want to use a JavaScript fudge or stick with the safe old (and, again, perfectly valid) but semantically poorer headings and divs approach. This site, along with many others, chooses the former. Because HTML 5’s loveliness just about outweighs a hack’s ugliness.

# End of Intermediate HTML

</body>