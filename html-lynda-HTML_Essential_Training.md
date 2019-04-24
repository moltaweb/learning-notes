# HTML ESSENTIAL TRAINING

<div class="hidden">
General impression

* 4/10, Not a top course
* Too much focus on content and structure
* Missing more info on certain tags (no forms, canvas etc.)
* Could have done the same in half the time
</div>
______________

## INTRODUCING HTML

### The importance of HTML

HTML provides the essential structure for Web pages  
CSS defines how it looks, and JS how it behaves, but HTML is the core content

HTML is a markup language, all it does is to mark-up some content to describe how it relates to other content on the page  
Does it through tags

### Basic HTML syntax

An HTML file is just a simple plain text file with a .html or .htm extension

HTML = HyperText Markup Language ->` use of tags to mark up content on the page to identify it

Tags syntax is `<element_chars>` to open and `</element_chars>` to close it

Tags can have attributes

* specific to the attribute (eg: method for form)
* global attributes (eg: class)

Attributes can be

* informational (eg: lang="en")
* functional (eg: href="#")

We can nest element tags inside of another

### The current state of HTML

HTML 1.0 in 1991, and HTML 4.0 in 1995
4.0 has been the most stable version for a long time

In 2000, W3C tried to move HTML towards XML with XHTML 1.0, to make it more strict and extensible
In 2009 this idea of moving to XML was abandoned

In parallel, in 2004, a consortium of companies consituted the WHATWG, took the HTML 4.0 and moved it forward

In 2007 W3C adopted the work of WHATG and renamed it HTML5

But up to now, both W3C and WHATWG work in parallel with independent branches...

HTML5 differs from HTML4.0 in:

* new elements (tags)
* more clear rules about to do when tags are missing, etc.
* more focused on building apps (drag and drop, canvas...)

Now, for the most part, specifications really don't differ that much. the biggest decision will be to decide which doctype to use on our HTML pages.

Advice is to go with HTML5 :
1. focus on writing clean syntax
2. then introduce new features as we need them (canvas, etc)

### HTML resources

* W3C specs: https://www.w3.org/TR/html5/
* WHATWG living standard: https://html.spec.whatwg.org/multipage/
* webplatform.org
* developer.mozilla.org

### Choosing a code editor

Anyone will suffice. Common features to look for:

* syntax highlight
* source formatting
* linting
* line numbers


_____________________

## BASIC PAGE STRUCTURE

### Exploring an HTML document

Essentials of what makes an HTML file

* doctype declaration - says the version of HTML
* html
    * head - all the thinkgs that make the document work
    * body - the actual contents

Now let's focus on each type individually

### DOCTYPE declarations

The Doctype is supposed to tell the browser or user agent the version of HTML the document is using, so that the reader can parse it correctly
Actually it triggers what is called "quirks mode", whicih ensures the page is rendered properly

html5 `<!DOCTYPE HTML>`

This is more than enough nowadays
At the very top of the document

Right after the doctype comes the `<html>`
* lang="en"

### The document head

head

* meta - don't need to be closed
    * charset="utf-8" - standard. Sets the characters set to tell the UA how to render (which symbols). Not everybody does it, because most server set it by default, but recommended to do it
    * name="description" content="what the page is about". This used t be important for SEO, now its a good practice
* `<title></title>` - what appear in the tab, the search results, etc.

Later we will see how to link to other files, CSS, JS...

### The document body

Contains the actual information
Theoretically, all the content should go between elements. If not, the UA will render a default (`<p>` for example), but this is not semantically correct.

body
* h1...h6 - headers
* p
    * b
    * em

We will see more details later

### Understanding content models

Content Models define the type of content expected inside an element and control syntax rules such as nesting

All elements in HTML belong to at least one Content Model

Prior to HTML5, there were basically 2 types:

* block level
    * they take etheir own line within the flow of the document
    * h1...h6, `<p>`, `<div>`, ...
* inline
    * they belong to other blocks
    * `<b>`, `<a>`, ...

HTML5 defines 7 types (which can be block or inline)

1. Flow
    * Includes almost all of the elements
    * except what?
2. Metadata
    * in the head section
3. Embedded
    * imports other resources into the document
    * audio, canvas, embed, iframe, img, math, object, svg, video
4. Interactive
    * intended for some type of user interaction
    * a, audio, button, input, keygen, label, select...
5. Heading
    * defines the header of a section (with or without a section element)
    * h1...h6
6. Phrasing
    * includes all the text of the document
    * basically, all the inline elements in HTML4
7. Sectioning
    * Define the scope of sections in ur documents
    * article, aside, nav, section

https://www.w3.org/TR/2011/WD-html5-20110525/content-models.html#kinds-of-content

Some models overlap, which means that elements can belong to several types at the same time



_____________________

## FORMATTING PAGE CONTENT

### Formatting content with HTML

Once we understand how the markup syntax works, it's just a matter of knowing which tags (elements) are available, and what options they have

Don't be confused about the use of an element or another based on how the browser renders it. For example, do not use h1...h6 based on the size!!!

Styles are done by CSS
HTML is about semantics

For exaple `<em>` displays italic, but its logical meaning is "emphasize". So if a machine reads it (vocal transaltion), it will emphasyze that word

HTML removes extrs spaces and line breaks. If we want to keep the pre-format, we can do so with the `<pre>` tag

### Using headings

Headings are used to structe pages and determine content hierarchy

h1... h6

They denote different levels of importance of our content, like the titles in a MS Word document

Prior to HTML5 the only elements we had to determine sections were headings
Now we have more, but headings are useful for creating and ranking sections

Tips:

* don't abuse h1
* don't skip levels (use h1 and h3, skipping h2)

### Formatting paragraphs

Paragraphs are the most baisc wrapper for text. In fact, by default most browsers will wrap unformatted text within `<p>`

Tips:

* don't use empty paragraphs to gain spacing (`<p>`&nbsp;`</p>`). There's CSS `margin` for that

### Controlling line breaks

`<br>` is used to insert line breaks, when we don't want necesarrily to set a new paragraph  
`<br />` is just as valid

### Emphasizing text

`<em>` emphasis  
`<strong>` strong  
These are logical tags, they have a meaning

`<b>` bold  
`<i>` italic  
These are visual tags, just for presentation purposes. They tell the UA to display it differently, but has no semantic meaning at all

They are compatible between them

### Displaying special characters

We have to use named character entities when we want to display special chars, not ready uin our keyboard, the copyright symbol, or "`<" for exple

The syntax is:
`&abcd;`

where "abcd" represents the named enticty

https://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references

### Controlling whitespace

Normally, browsers ignore all the whitespaces after the first one

If we want to introduce an extra whitespace we should use `&nbsp;`

nbspc = non-breaking space

But beware, nbsp is not for separating stuff, for that we have CSS

Its actual use is for example we have "Formula One" in our text, ny putting "Formula&nbsp;One", the 2 words will not be separataed in line breaks, always together

### Displaying images

To display an image we use `<img>` or `<image>`

Now, images are considered as "replaced content", which means the UA will replace the tag by the resource asked for. Therefore, the attributes of the `<img>` tag are very very important

Attributes

* src - where to get the resource from
* alt - alternate text for acccessibility, etc.
* width, heigth - optional
* align - deprecated, now done with CSS

### Challenge: Formatting page content

Not interesting
Given a bunch of HTML code, tag it and structure it

### Solution: Formatting page content

Not interesting


_______________________

## STRUCTURING CONTENT

### The value of structure

One of the benefits of HTML is that it allows us to structure the content basedon its meaning
This is known as SEMANTICS

Visually, everybody can intuitively recognize the sections.
But it's important to design also for machines (UA, search engines, voice recognizers, etc...) that rely on the section semantics

This is where sectioning comes into play

It is importanto for mainatenance, performance, etc.

### Controlling document outlines

This is about recognizing sections of the document, content hierarchy, etc...
How to organize the content based on its level of importance

HTML5 has new tags that provide even more semantical detail:

* nav
* article
* section
* aside

### The nav element

This element is designed for main navigation blocks of the site (main nav menu, etc)
Again, important semantics for machines, search engines,etc.


### The article element

Typically, this element leads to confusion with the section element

According to W3C spec, it represents a complete or self-contained composition that is in pricnple,independently distributable or reusable (a post, a widget, a blog entry, a post comment, etc.)  
Things that if we tok them apart, they would make sense on their own

### The section element

Also pretty confusing for some people

According to W3C spec, it represents a generic section of a document or application. Typically, it should be identified by including a heading as a child of a section element

Also use section when the portion of the content has an outline in the document outline

In conclusion: 1 artcile may contain multiple sections

### The aside element

This is a perfect example of how standard usage becomes part of a specification.   The most common use of the aside element is the sidebar  
It is designed to represent related content

### The div element

Used when we want to group elements together without a particular semantic meaning

Typically they were always used to group content to assign CSS classes and Id  
With HTML5 this is still valid, but in most cases there will be a better, more semantic alternative

Advice is to use div as last resort, only when there are not other elements available with more semantic meaning

### Other semantic elements

So far, the elements we have seen define an outline (nav, article, section) with a lot of meaning  
Or, like div, no meaning at all

There are other elements that give meaning without modifying the outline sections. These are:

* main
* header
* footer


`<header>` represents introductory content for its nearest ancestor seciotning content element. It typically contains a group of introductory or navigational aids
When it follow directly `<body>`, it referes to theader of the whole page
Exmple: introduction of an article, etc.

`<footer>` represents a footer to its ancestor (like header but at the bottom). Typically contains information about the section, such as who wrote it, etc. It is not necessarily meant to be the footer of the page, but rather the footer of a section. But it can be used for page footer as well: copyright data, privacy policies, etc.

`<main>` represents the main content of the body of a document or application. It does not define a section, just mark up the content that is unique to the page. Typically, only 1 tag `<main>`, and should not be repeated across pages
It could be the same as `<article>`

### Using WAI-ARIA roles

ARIA = Accessible Rich Internet Applications  
It allows to assign roles to elements, through their attributes

* banner
* application
* main
* etc.

### Challenge: Adding sectioning content

### Solution: Adding sectioning content



______________________

## CREATING LINKS

### Exploring the anchor element

The anchor element `<a>` is used to create links
The link element is actually used to request external resources from the page, but not links themselves. Don't be confused

Attributes:

* href (hypertext reference)
* target - constrol where the new page opens
* rel - relationship of the target object to the link object (j: next, download...)
* title - make links accessible (like alt in img)

### Linking to pages within your site

This is the most common use of `<a>`

`<a href="path/to/file.html">`

The path is relative to the location of the html file that contains the link

Notes:

* we can wrap `<a>` tags around any other element to make it clickable
* Before HTML5, `<a>` was inline, now it can be also block-level

### Linking to external pages

Also common is to redirect users to resources in other sites

`<a href="http://www.url-address.com/path/to/resource">`

Note:

* The http protocol must be included

### Linking to downloadable resources

Usually we will do this with a script for security reasons, but with HTML it can be done directly, just by linking directly the resource

`<a href="path/to/resource.zip">`  
`<a href="path/to/resource.pdf">` --> opens in the browser if embedded pdf reader  
`<a href="path/to/resource.pdf" download>` --> downloads the document  
`<a href="path/to/resource.pdf" download="abc.pdf">` --> downloads the document and renames it

### Linking to page regions

Anchords allow to redirect to other sections in our page (named fragments)
For that, we use #

It's done in 2 steps:
1. Identify the section we want to jump to with an id attribute
2. add #identifier to the href value

This works both for the same page or for other pages

### Challenge: Creating links

### Solution: Creating links



______________________

## CREATING LISTS

### Unordered lists

Lists are used to group things together. Not only list them one after the other, but also grouping them. for example, a navbar shall contain a list of links, form elements, etc...

List items are referenced with `<li>``</li>`

Unordered lists:
`<ul>``</ul>`

wrap around the list elements

Lists can nest other lists inside

### Ordered lists

Very similar to unordered lists, but using `<ol></ol>`

In opposition to `<ul>`, these have a sequence, so we can control it with some attributes:

* srtart="x" -determines at which number sequence it starts numbering
* reversed (bool) - reversed numbering
* type="x" - type of numbering
    * 1
    * I
    * i
    * A
    * a

### Definition lists

Description lists are also referred to as definition lists
They have 2 parts:

* term
* description

They are often misknown

Syntax:

```html
 <dl>
    <dt>Term 1</dt>
        <dd>Description 1</dd>
    <dt>Term 2</dt>
        <dd>Description 2</dd>
    <dt>Term 3</dt>
        <dd>Description 3</dd>
 </dl>
```

DD's are very flexible, we can put inside basically anythong we want

### Challenge: Creating lists


### Solution: Creating lists


_____________________________

## CONTROLLING STYLING

### HTML and CSS

These 2 technologies work very very closely together  
CSS defines styling and visual appearace, whereas HTML shoul limit to content and structure

By default, HTML is styled with the browser's default styles for every element.  
When we write CSS, what we do is to overwrite those default styles

CSS syntax is presentational. It's not logical code as JS,and not markup as HTML

The important thing to understand is that CSS can completely change the aspect of the page. But to machines, Search Engines, etc... the page is defined by HTML only

### Creating inline styles

Inline styles are created inside an element with the "style" attribute. this style appliesto the element only

Syntax:
`<h2 style="color:red; font-weight:bold;">`   
element styled `</h2>`

The problem of inline elements is that they are hard to maintain, it's very inefficient.  
Normally, not the preferred option

### The style element

The `<style>` element can be added inside the `<head>` section of the page
We just type in our CSS code between the tags

```html
<style>
h2 {
    color:red;
    font-weight:bold;
}
</style>
```

CSS in here apply to the whole page, so to all h2 elements, not one by one

But again, it's not the most efficient way either, we will see how to link external global CSS files

### Controlling typography

Typography is a wide subject. Examples:

* font-family: Georgia, "Times New Roman", serif;
* font-size: 2em;
* font-weight: normal;
* font-style: italic;
* line-height: 1.6;
* text-align: justify;

### Adding color

Colouring is also a wide subject. Examples:

* background-color: #777777;
* color: red;
* background: rgb(44,45,140);

Colouring can be RGB, HEX or RGBA

### Externalizing styles

The most efficient eand maintenable way to define styles is through and external file. Because once it's linked in all pages, just by editing the .css file, the styles will apply throughout the site automatically.

We write our CSS in a myCssFile.css file and link it in our HTML page, inside the `<head>`:

`<link rel="stylesheet" href="/path/to/myCssFile.css">`

The rel attribute is important

### Challenge: Controlling basic styling

### Solution: Controlling basic styling


___________________________

## BASIC SCRIPTING

### HTML and JavaScript

Pretty much like HTML and CSS work together, so do HTML and JS  
JS is a scriptong language developed for the web and suported in almost every web client

JS started as a basic language, but it has evolved into a very serious language now

Ideally, we should develop our websites keeping in mind what would be the minimum required functionality. ie, if somebody browses our site without CSSor JS, the experience should still be good enough

### The script element

Like for CSS we have the `<style>` element, for JS we have the `<script>` element

The script tag can be placed in the `<head>` section or right before `</body>`

```html
`<script type="text/javascript">`
    // here goes JS code
`</script>`
```

Whenever the browser encounters a script tag, it's going to stop, execute the code and resume rendering the page.  
This is why it's often better to put the scripts at the bottom of the page

### Writing a function

Example:

```JS
window.onload = function() {
  // code
}

function nyOwnFunction() {
  // code
}
```

### Using the DOM

The DOM is a standardized way of rendering HTML documents in the browser
It allows to access HTML elements programatically

### Listening for an event

creates a function but not interesting

### Responding to events

### Externalizing JavaScript

Just like CSS, it's more efficient to reference external JS files

`<script src="/path/to/file.js">``</script>`
