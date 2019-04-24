# CSS ESSENTIAL TRAINING

Overall

* 8/10
* Good introduction to almost everything important

_____________________

## CSS 1 - GETTING STARTED

### HTML overview / review

Front-end web technologies refer to HTML/CSS/JS  
While they are very closely related, each one is responsible for somtehing different:

* HTML - content and structure
* CSS - presentation and style
* JS - interactivity and behavior

HTML5 is the latest version of HTML, adding new features and tags  
--> look at the specs in W3C and MDN

Most elements have an opening a closing tag to wrap the content  
Some elements do not have a closing tag, since they do not wrap any content as they are the content

Void elements in XHTML required a closing bracket "/>"  
In HTML5 is no longer necessary, but not harm to put it

Tags can have also attributes

The DOM represents the tree-like structure of the HTML document. Each element (tag) matches to an object in the DOM

### Default browser styles

Browsers have usually a default styling defined in the user agent style sheet

Also, use Developer Tools

### Browser support and inconsistencies

There's a wide range of browsers available: Chrome, Firefox, Safari, Opera, Edge, IE...  
Browser support used to be painful with older versions of IE6 and IE7

Interesting resources:

* statcounter
* caniuse.com

The difference among browsers is not as big as it used to be  
Do not become obsessed with that if you're new to CSS

### Text editors

To create a Website we actually only need a plain text editor

Various options

* Atom
* Bracket
* VS Code
* Sublime

### Project overview and setup exercise

Overview

* doctype
* html / attribute: lang - defines the language of the page (for auto translation)
* head - the brains of the page
    * meta
        * charset - default UTF-8 (unicode)
        * viewport - for responsive web design
    * title
* body
    * header - personal info, name, logo...

### Inline, internal and external CSS

3 ways to add CSS to an HTML page

1) external - recommended method

`<link rel="stylesheet" href="style.css">`

In older versions:
`<link rel="stylesheet" type="text/css" href="style.css">`

2) Inline - should be avoided

add the style attribute to amn HTML element

3) Internal CSS

In the `<head>` section, inside `<style>` elements  
It might come in handy if we have specific styles for a given page, but for that scenario there are better methods that we will see

### Create a CSS file

Add the link tag in the HTML document to link to style.css and start coding CSS

### Naming conventions

* By convention, the initial page opened in a folder server side is named "index.html"
* use concise and descirptive filenames
* a website is basically a bunch of files linked together. Understanding project fodler structure is vital, and having good names helps prevent errors
    * Relative paths, relative to our document
    * Absolute paths, include the URL


___________________

## CSS 1 - CSS CORE

### Syntax, terminology and naming conventions

selectors determine which HTML element to apply styles to

declaration blocks consist of on or more rules enclosed in {}

declarations are style rules, wirtten in "property: value;" pairs

```css
p {
    color: blue;
}
```

properties determine the type of style
values depend on the properties

We have to memorize or reference the available properties and values

### Type, class and id selectors

Type selectors match the HTML by using the element name directly, w/o angle brackets

```css
h1 {
    color: blue;
}
```

The style apply to all elements wth that tag

We can be more precise by addign class or Id attributes to HTML elements

Class selectors can be applied multiple times per page. The class value is the selector, startin with "."

```css
.my_class {
    color: red;
}
```

Id selectors can be applied 1 time per page. The Id value is the selector, startin with "#"

```css
#my_id {
    color: red;
}
```

When adding classes to an HTML element, we separatae them with spaces to apply more than 1  
But only 1 id per element

`<div id="my_id" class="class1 class2 class3">`

### Practicing with simple selectors

Practice video in JSFiddle

To summarize, type elements target generic HTML elements, and classes and id allow us to be more specfic

### Pseudo-class selectors

* Group multiple selectors
    * we can apply the same property block to multiple selectors at the same time, separating by commas
    * this is more efficient as we save declarations
    * `h1, h2, h3 { /* this appllies to h1, h2 and h3 elements */}`
* Descendent selectors
    * use multiple selectors, separataed by a space
    * no limit in the number of selectors nested
    * `p a { /* select a links inside of p paragraphs */}`
* Pseudo-class selectors
    * pseudo-class selectors are used to target a specific state of an element
    * syntax: "selector:keyword"
    * `a:hover { /* applies to links on hover only */}`

Pseudo classes: examples: `a`    
* a:link - `<a>` with href only
* a:visited - links already clicked
* a:hover - on mouse hover
* a:active - the moment on which we click 
* a:focus - focus on keyboard




### Selectors: Best practices

* Type: when the style should apply to all the elements
* Class: when the style should apply to many instances, multiple times per page
* Id: when the style should apply to a specific element only
* Descendent selectors: when we want to target elements based on their parents/ancestors
    * Max 3 levels deep, otherwise the page will load slow

Try to combine selectors whenever possible

### CSS comments

`/* This is a comment */`

Usage:

* leave notes for yourself and others
* organize code blocks
* comment out code temporarily

### RGB, hex and keyword color values

```css
color: rgb(0,0,0);
color: #AABBCC;
```

### Practicing with selectors and colors

Add classes and selectors to HTML
Add CSS properties


### Cascading, inheritance and specificity

Cascading: when several identical rules apply, the one last defined takes it

Inheritance: if we apply a style to a parent, it will be be inherited by ts children (unless those have already a more specific rule, like `<a>` for exple)

Specificity: browsers apply a rule to determine the highest specificty that applies. If specificty is the same, the cascading applies  
In general : id > class > type

Best practice to avoid specificity issues: start wth general selectors and then get more specific as needed


_____________________________

## CSS 1 - TYPOGRAPHY

### Web-safe fonts and the font-family property

Typography: the study of the design and use of type for communication

Typeface: a set of fonts, designed with common charactristics and composed of glyphs

Font: individual files part of a typeface

| Typefaces | Description
| --- | ---
| serif | they have small decorative lines<br/>Georgia, Times New Roman
| sans serif | they have rounded ends<br/>Verdana, Arial, Helvetica
| script | they have a hand-lettered look<br/>Cooki, Brush Script
| Decorative | they are distinct and onramental<br/>Lobster, Papyrus, Copperplate
| Monospace | each character uses the same width (used for code)<br/>Courier New, Consolas

To set the font family in CSS we use "font-family" property

Web-safe fonts are comonly preinstalled on computer or devices. Exple: Arial and Times New Roman

In general, fonts vary across OS
cssfontstack.com

When using a font-family in CSS; use a fallback font :

```css
h2 {
    font-family: 'Helvetica Neue', Arial, sans-serif;
}
```

The backups default browser for each typeface is:

* serif
* sans-serif
* cursive
* fantasy
* monospace

### Web fonts and Google fonts

They are not required to be installed on the device

2 methods:

* internal
* external

*Internal*

```css
@font-face {
    font-family: 'Museo Sans';
    src: url(museo.sans.ttf);
}

body {
    font-family: 'Museo Sans';
}
```

Different browsers support diff formats. Generally .woff and .woff2 are well supported

*External*

These are 3rd party services we can used by just linking to their site. Quite a std option s Google Fonts

### The font-size property

There are 3 ways to determine font size: 

* px - absolute, great for accuracy
* em, rem - relative


Relative values are calculates based on the nearest ancestor element

1 em is the size in px of the ancestor. If nothing is defined, is the browser's default for body (typically 16px)

rem is always relative to the size of the root element defined in the html selector:

```css
html {
    font-size: 20px;
}
```

More info
https://tympanus.net/codrops/css_reference/length/


### Practicing with web fonts and font-size

Add font family and size to styles.css

### The font-style and font-weight properties

Other properties for fonts:

* font-weight - thickness or boldness of typefaces
    * number values are 100, 200, ... 900
    * if nto available, the browser will map t to the neares available
    * can also use keywords:
        * normal = 400
        * bold = 700
        * lighter
        * bolder
* font-style - add or remove an italic style
    * 3 values: italic, oblique, normal

More CSS fonts : check mdn

### The color, line-height, and text properties

Other properties 

* color
* line-height - space between 2 lines of text
* text-decoration - add an underline above, below, or through the text
* text-transform - specifies the casing
    * Capitalize, lowercase, UPPERCASE, none
* text-align - this style is inherited by descendant elements

As a rule of thumb, the line-height shall be larger than the font size (Typically 1.5)

### Adjusting the font-weight property

Choose font-weights from Google fonts. We can add as many as we want, but the more we load, the longer to load the page, so only add what we need



_________________

## CSS 1 - LAYOUTS

### Block vs Inline display

There are 2 types of HTML elements

    block elements
* inline elements


Each has a set of default behaviors that determina how the element displays on a page

Block elements

* height = content
* width = 100% of the container
* they start on a new line
* They can wrap other elements (block or inline)
* ex: h1, div, p


Inline elements

* height and width = content
* elements align left, on the same line
* can only nest other inline elements
* ex: a, span, strong


Rapid check: add border or bakground color to the element to see f it takes 100% of width or not

We can modify width and height of block elements, but these have no effect on inline elements.

Also, we can modofy the diplay property of all elements. This property has many possible values, the most common being:

* inline - make block elements behave like inline elements
* block - make inline elements behave like block elements
* inline-block - blocks that display side by side on the same line
* none - hide content from the page




### The box model

The box model describes how the size of elements is calculated

Everysingle HTML element has its own box. They have 5 properties:

* content
*     width
*     height
* padding - adjust the space inside of an element's border
* border
* margin - adjust the space around the element


Typically the length of each is determined in px or %

Padding/margin shorthands:

* padding: 2px; // trbl
* padding: 2px 10px; // tb rl
* padding: 2px 10px 5px; // t rl b
* padding: 2px 10px 5px 2px; // t r b l




### Margin and page layouts

By default, elements stack one on top of the other based on the order they appear in teh HTML

We can use negative margins to move the elements outside from their stacking position, but just a little

Use also margin to center block elements:

* assign a width
* apply margin: 0 auto;


To have a section that spans a bakground but the content has a margin, we use

`<section class="wrapper">`
`<div class="content">`
Content here
`</div>`
`</section>`


### Practicing layouts

Add CSS and HTML to the project

In the content-wrap class, if setting width: 950px;
When the size of the screen is smaller, the content overflows

We have to use max-iwdth instead. Then, when it is smaller, the width gets 100% by default



### Practicing with padding and spacing

Add CSS and HTML to the project



### Floats

Floats is another property to change the flow of HTML

When we float an element to the left or fight, it will stick to the side, and some of the following elements will rearrange to wrap the floating element, until we cover the height of it.

If we want a subsequent element to not float anymore, we do a clear: both; on the first element we want to take out from the floating flow

Floating affects sbsequent elements, but also the parent container. The parent container will not recognize the height of floated elements, and will only wrap around non floated child elements

To make the container wrap the floating element we have 2 options:

*     add an overflow property to the parent container

* hidden
* auto - adds a scrollbar if the text is longer than the container

* add a class and clearfix snippet, added to the parent of the floated element

* .clearfix:after {
* content: "";
* display: table;
* clear: both;
* }


There is a newer option called Flexbox, we will talk more about it



### Practicing with floats

Add CSS and HTML to the project

Note: while we can adjust the size of images with CSS, it doesn't make sense, just crop the original image to save bandwidth



### The box model fix

By default, browsers user content-box, meaning the padding and border add to the content size

Another option is border-box, meaning the padding and border are included in the total width and height, pushing the content inbounds

To use it:

html {
     box-sizing: border-box:
}

*, *: before, *:after {
     box-sizing: inherit;
}

How this affects our layout? for example, if we have a fixed content width and 2 blocks floating side by side (like fruittoday banners), with box-sizing we can play as we ant with content, padding and border, that it will not break



### Practicing with columns

Use of box model border-box and float-left with min-height


### Conclusion

Usually it's about trying and erroring. Most times there's no right or wrong answer, just try and solve the problems as they appear


________________________

# CSS 2

## CSS 2 - CSS SELECTORS

### CSS syntax review

*     Selectors are used to determine where to apply the styles
*     Declarations are the style rules and they're contained within the curly braces
*     Properties determine the type of style
*     Values set the style and are based on the proerty
*     comments are inside /*   ---   */
*     3 ways to add CSS to an HTML page

* inline
* internal
* external - recommended



### Basic and attribute selectors

        Type selectors
        Class 
        ID
        Attributes selectors

    [attr] elements with this attribute
    [attr=val] elements with this attribute and value




### Combinator selectors

Combinators are selectors that are combined in various ways to make more specific selections based on the HTML structure

        Descendent selectors  -apply to any nested element

    parent descendet

        Child combinators - used to select only child elements

    parent >` child

        Sibling combinators - used to select sibling elements

        only first adjacent sibling

    element + sibling

        element and all the following siblings

    element ~ siblings

    Multiple selectors -separataed by commas




### Pseudo-class selectors

A pseudo-class isa keyword, added to the selector with a ":"
It's used to specify a certain state of the element

Examples:

    hover
    first-child - selects the first child element of its parent (it assumes it is this type)
    last-child - selects the last child element of its parent  (it assumes it is this type)



    first-of-type - selects the last child element (of this type) of its parent (no matter if there are other elements)
    last-child - selects the last child element (of this type) of its parent (no matter if there are other elements)


        n-th-child() - selects one or more child elements based on the order within the paren-container. Arguments:

    keyword - n-th-child(odd)
    number - n-th-child(3)
    algebraic - n-th-child(an+b) / n from 0, 1, 2... / a,b any numbers

    nth-of-type() - same as before, but only selects the elements types of the selector




### Pseudo-element selectors

Used to select certain parts of the element, which are not explicitly part of the DOM tree

.element::first-letter

They can use "::" (CSS3) or ":"

Examples:

    :before - can be used to generate elements that are inserted before the selected element
    :after - same as previous, but after the element


:before/:afeter should have the "content" property to add content. This content is only visual, not added to the DOM
unicode-table.com



### Practicing with advanced selectors

Add CSS and HTML

Note: it's normal to have to be changing our CSS as the project moves along. Doing and redoing is a normal part of the process



## CSS 2 - LAYOUTS

### Box model review

The box model describes the way in hich CSS handles the szing and spacing of HTML elements

    width
    height
    padding
    border
    margin



### Float and display review

Both float:left; and display:inline-block; properties can be used to display block elements inline

Each has pros and cons


### Horizontal navs with the display property

The problem is that there is a space between the elements

To remove it, we do font-size:0; in the parent element, and reseet the font-size in the navigation link


### Horizontal navs with the float property

We have to self-clear the floated parent with overflow: hidden;

If we add float, the browser automatically displays it as a block
Also, the elelemtns get the width of their content automatically

Either 2 option is ok, it depends on the context and up to us to decide one or the other
We will se Flexbox in a future lesson



### Practicing with the nav element

Create the nav for the site



### Positioning

The "position" property can be used to arrange elements relative to the default page flow or browser viewport

5 values:

    relative - can be positioned within a containing parent element or browser viewport
    absolute - can be positioned within a containing parent element or browser viewport
    fixed - can be positioned within a containing parent element or browser viewport
    static - default: elements not positioned
    inherit - inherit from ancestor element


Also used with a combination of box offset properties: top, bottom, right, left

Relative: element stays in the normal page flow but can be moved from its original position with top/bottom/left/right

Absolute: element is removed from the normal page flow and additionally it can be moved from its original position with top/bottom/left/right. That move is relative to the parent container if this one is also positioned (relative), if not, to the viewport

Fixed: element is removed from the normal page flow and additionally it can be moved from its original position with top/bottom/left/right, relative to the viewport

It's not a good idea to use positioning for aligning elements (like float of inline-block), since positoining fixed/abs removes from the flow, it can be difficult to manage

Used rather to move specific elements

By default, if you don't set a width to a positioned element it will take its content's



### Practicing with fixed navigation

Make the nav bar fixed on top of the page



### Practicing with positioning elements

Add a button for "Download PDF", position absolute in the header bottom right



### Float, display and position

Guidelines to know when to use one or the other

    Float
        variable and flexible content (eg, image surrounded by text, or blog posts with different lengths)
        global page structures (eg, sidebar)
    Display
        algin page components (beware of the extra space!)
        align elements that need to be centered aligned (navbars)
        doesn't change the page's natural flow
    Position
        positioning elements relative to other elements
        position elements to a specific spot in the document
        align elements outside of the document flow


As a best practice, try to keep the natural flow page as much as possible

If using position, then float is ignored
If using float, then display is ignored



### Layers and the z-index position

Actually webpages are 3D, there is a z-axis to stack elements on top of another. This is known as the stacking context.

The stacking order is applied to a group of elements that have a common ancestor.

It only applies on positioned elements

The z-index property takes a number from 0 to 999 as value. The higher, the more on the top

In general, this property should not be used very often, if it does, probably there is a problem in the HTML



## CSS 2 - TIPS AND TOOLS

### Browser development tools

Learning how to use your browser's dev tools is essential



### ### Debugging CSS

Video explaining how CSS styles are displayed in the browser's dev tools



### Resetting stylesheets

2 options developed by people in teh WebDev community:

    Reset stylesheets remove all the default styles of the browser
    Normalize stylesheets: instead of removing, it adds CSS to make browser compatibility more consistent


It might be a good idea to use any of these, as long as we don't double the work



### Icon fonts

Icon fonts are a simple way to add imagery to our webpage but having the flexibility of styling them like fonts

Example: Font Awesome

Like for Web fonts, they can installed by just adding the resource from a CDN



### The background property

So far we've used "background" property to set color values, but this is a shorthand

Long-hand properties:

    background-color
    background-image
    background-repeat
    background-position
    background-attachment
    background-size


A not on background-image vs HTML `<img>`
->` if the image is part of the content (eg, your profile image) use HTML, if it is just for decoration (slider, etc.) use css


### Background shorthand syntax

In shorthand, the order of values don't matter
Exception: background-size must go after background-position, separated with "/"

selector {
    background: url(image.jpg) no-repeat fixed 0px 0px / cover;
}

Tip: do it in 2 lines:

selector {
    background: url(image.jpg) no-repeat fixed 0px 0px
    background-size: cover;
}

Use the shorthand first, then others, because shorthand if not declared values, assumed the default ones, so it will overwrite others. Example:

selector {
    background-color: red;
    background: url(image.jpg) no-repeat fixed 0px 0px
}

The color will be overwritten



### Alpha transparency and gradients

Use RGBA:

selector {
    background: rgba(r, g, b, a)
}

a is the transparency used to set the opacity 0`<=a`<=1

Another option is to use linear-gradients:




### Practicing with backgrounds and gradients





## CSS 2 - RESPONSIVE AND MOBILE

### Introduction to responsive design




### Mobile friendly and mobile first




### Creating flexible and fluid layouts




### Introducing media queries



### Using media queries



### testing responsive layouts



### Device emulation




### Revisiting your CSS


