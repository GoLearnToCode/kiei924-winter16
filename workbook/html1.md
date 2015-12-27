# Cheat Sheet: HTML Basics

HTML is the primary language that all browsers understand.  Read the [opening clause on Wikipedia](http://en.wikipedia.org/wiki/HTML) (the paragraphs above the table of contents) for a brief overview of the language.

Web pages aren't made up of solid blocks of run-on text.  HTML coding enables us to break up a web page into a meaningful structure.  Expressing the meaning of each part of our web page is why we learn to write code in the HTML language.

### Elements

The fundamental building block in HTML is the **element**.

Every HTML element:

* takes up a rectangular portion of the page
* is identified by its **tag**
* is classified as a **block level element** or an **inline element**
* might be accompanied by one or more **attributes**
* might contain _inner content_, and therefore require an **end tag**, sometimes called a **closing tag**

### Block-Level Elements

Block-level elements always reserve the full width of the browser window for its rectangle.  Here is an example:

```html
<h1>Product Catalog</h1>
```

The `h1` is the tag. `Product Catalog` is the content.  This element has both an opening and closing tag.  Note that closing tags are almost identical to the corresponding opening tag but have a `/` before the tag name.

Here is another example:

```html
<p class="lead">The Cubs lost again today.</p>
```

Here the `p` tag has a `class` attribute assigned to it.

Try them in your browser to see how block-level elements always reserve the remaining horizontal space for themselves, regardless of how you resize the browser window.

### Inline Elements

Inline elements take up a minimal rectangle, and can have other elements to their left and right (hence the term _inline_).  They are intended to stay within the flow of their parent block-level element.  Here is an example of using the `strong` element inside of a paragraph:

```html
<p class="lead">The Cubs lost <strong>again</strong> today.</p>
```

Another inline element is the `img` tag, used to display photos and graphics:

```html
<img src="http://www.google.com/images/srpr/logo11w.png">
```

The `img` element never has any inner content.  Instead, the `src` attribute supplies all the information the element needs.  Therefore, no closing tag is needed.

### Attributes vs. Inner HTML

Depending on the type of element and its syntax, HTML elements can have **attributes**, **inner HTML**, or both.

For example, the `img` tag has the `src` attribute, which describes the "source" of the image:

```html
<img src="http://www.google.com/images/srpr/logo11w.png">
```

And here, the `h1` tag has **inner HTML** of `Cookies!!!`, which describes the content of this particular `h1` element:

```html
<h1>Cookies!!!</h1>
```

Elements can have both attributes and inner HTML; for instance, this `a` tag:

```html
<a href="http://golearntocode.com/">Visit our website</a>
```

Generally speaking, attributes represent data that is important for the web browser to know about, but not necessarily displayed to the user. And inner HTML is usually displayed to the user.

### Nesting

HTML elements may be **nested**, that is, you can have elements inside of other elements. For example, a `ul` (unordered list) has individual `li` (list items) inside of it.

```html
<ul>
  <li>Oreos</li>
  <li>Chips Ahoy</li>
  <li>Nilla Wafers</li>
</ul>
```

Here, we use nesting to build a link (`a` tag) with an image instead of text:

```html
<a href="http://golearntocode.com/"><img src="code.jpg"></a>
```

