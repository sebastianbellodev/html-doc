# HTML
This documentation was obtained from *Google Developers* course [Learn HTML!](https://web.dev/learn/html/overview/)

## Introduction
---

HTML (Hypertext Markup Language) is the standard markup language for describing the structure of documents displayed on the web.

HTML documents are basically a **tree of nodes**, including HTML elements and text nodes.

## Elements
---
HTML consists of a series of elements, which you use to enclose, or wrap, different parts of the content to make it appear or act in a certain way. HTML elements are delineated by tags, written using angle brackets <code><</code> and <code>></code>.

~~~
<h1>Machine Learning Workshop</h1>
~~~

The closing tag is the same tag as the opening tag, preceded by a slash <code>/</code>. The tags are used to interpret the content of the page.

The text between the tags is called content. The entire thing —the opening tag, closing tag, and the content— is the element. [Here is the snippet](/index.html).

Each element may have multiple attributes specified. Many elements can have content, including other elements and text. Other elements are empty, with the tag and attributes defining their function.

It is possible to nest tags, but it is important to do it properly. HTML tags should be closed in the reverse order of which they were opened.

~~~
<p>This paragraph has some <strong><em>strongly emphasized</em></strong> content</p>
~~~

Always remember to include the closing tag. Althought the browser will render the content for most of the tags, this isn't consider a good practice.
The [specification provides a list of all the required closing tags](https://html.spec.whatwg.org/multipage/syntax.html#syntax-tag-omission).

There are two types of elements: replaced and non-replaced.

### Non-replaced elements

Non-replaced elements have opening and (sometimes optional) closing tags that surround them and may include text and other tags as sub-elements.

### Replaced and void elements

Replaced elements are replaced by objects, be it a graphical user interface (UI) widget in the case of most form controls, or a raster or scalable image file in the case of most images. Being replaced by objects, each comes with a default appearance. Depending on the type of object and the browser, the applicable styles are limited.

Void elements are all self-closing elements and are represented by one tag. This means there is no such thing as a closing tag for a void element.

[Here is an example](/index.html) of a replaced element by non-text content (user interface object):

~~~
<input type="range">
~~~

Void elements cannot contain text content or nested elements. Void elements include <code>&lt;br&gt;</code>, <code>&lt;col&gt;</code>, <code>&lt;embed&gt;</code>, <code>&lt;hr&gt;</code>, <code>&lt;img&gt;</code>, <code>&lt;input&gt;</code>, <code>&lt;link&gt;</code>, <code>&lt;meta&gt;</code>, <code>&lt;source&gt;</code>, <code>&lt;track&gt;</code>, and <code>&lt;wbr&gt;</code>, among others.

Most replaced elements are void elements, but not all. The <code>&lt;video&gt;</code>, <code>&lt;picture&gt;</code>, <code>&lt;object&gt;</code>, and <code>&lt;iframe&gt;</code> elements are replaced, but aren't void. They can all contain other elements or text, so they all have a closing tag.

Void elements are used to **provide information** about the content.
