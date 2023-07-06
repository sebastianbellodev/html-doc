<h1>HTML</h1>

This documentation was obtained from *Google Developers* cours [Learn HTML!](https://web.dev/learn/html/overview/)

<h1>Table of contents</h1>
<ol>
<li><a href="#introduction">Introduction</a></li>
<li>
<a href="#elements">Elements</a>
<ol>
<li><a href="#non-replaced-elements">Non-replaced elements</a></li>
<li><a href="#replaced-void-elements">Replaced and void elements</a></li>
</ol>
</li>
<li><a href="#attributes">Attributes</a></li>
<li><a href="#dom">Document Object Model (DOM)</a></li>
</ol>

----

<h2 id="introduction">Introduction</h2>

HTML (Hypertext Markup Language) is the standard markup language for describing the structure of documents displayed on the web.

HTML documents are basically a **tree of nodes**, including HTML elements and text nodes.

<h2 id="elements">Elements</h2>

HTML consists of a series of elements, which you use to enclose, or wrap, different parts of the content to make it appear or act in a certain way. HTML elements are delineated by tags, written using angle brackets <code><</code> and <code>></code>.

```
<h1>Machine Learning Workshop</h1>
```

The closing tag is the same tag as the opening tag, preceded by a slash <code>/</code>. The tags are used to interpret the content of the page.

The text between the tags is called content. The entire thing —the opening tag, closing tag, and the content— is the element. [Here is the snippet](/index.html).

Each element may have multiple attributes specified. Many elements can have content, including other elements and text. Other elements are empty, with the tag and attributes defining their function.

It is possible to nest tags, but it is important to do it properly. HTML tags should be closed in the reverse order of which they were opened.

```
<p>This paragraph has some <strong><em>strongly emphasized</em></strong> content</p>
```

Always remember to include the closing tag. Althought the browser will render the content for most of the tags, this isn't consider a good practice.
The [specification provides a list of all the required closing tags](https://html.spec.whatwg.org/multipage/syntax.html#syntax-tag-omission).

There are two types of elements: replaced and non-replaced.

<h3 id="non-replaced-elements">Non-replaced elements</h3>

Non-replaced elements have opening and (sometimes optional) closing tags that surround them and may include text and other tags as sub-elements.

<h3 id="replaced-void-elements">Replaced and void elements</h3>

Replaced elements are replaced by objects, be it a graphical user interface (UI) widget in the case of most form controls, or a raster or scalable image file in the case of most images. Being replaced by objects, each comes with a default appearance. Depending on the type of object and the browser, the applicable styles are limited.

Void elements are all self-closing elements and are represented by one tag. This means there is no such thing as a closing tag for a void element.

[Here is an example](/index.html) of a replaced element by non-text content (user interface object):

```
<input type="range">
```

Void elements cannot contain text content or nested elements. Void elements include <code>&lt;br&gt;</code>, <code>&lt;col&gt;</code>, <code>&lt;embed&gt;</code>, <code>&lt;hr&gt;</code>, <code>&lt;img&gt;</code>, <code>&lt;input&gt;</code>, <code>&lt;link&gt;</code>, <code>&lt;meta&gt;</code>, <code>&lt;source&gt;</code>, <code>&lt;track&gt;</code>, and <code>&lt;wbr&gt;</code>, among others.

Most replaced elements are void elements, but not all. The <code>&lt;video&gt;</code>, <code>&lt;picture&gt;</code>, <code>&lt;object&gt;</code>, and <code>&lt;iframe&gt;</code> elements are replaced, but aren't void. They can all contain other elements or text, so they all have a closing tag.

Void elements are used to **provide information** about the content.

<h2 id="attributes">Attributes</h2>

These extra bits of space-separated <code>name="value"</code> pairs (though sometimes including a value is optional) are called attributes.

Attributes only appear in the opening tag, providing information about the element. The attribute, like the rest of the opening tag, won't appear in the content, but they do help define how the content will appear to both your sighted and non-sighted (assistive technologies and search engines) users. Attributes are what make HTML so incredibly **powerful**, because they define the behavior, linkages, and functionality of elements.

The opening tag always starts with the element **type**. The type can be followed by zero or more attributes, separated by one or more spaces.

```
<a href="#register" target="_self">Registration</a>
```

In this example, we have an anchor link with two attributes. These two attributes have converted the content into an internal anchor link that scrolls to the attribute <code>id</code> in the current browser tab when the link is clicked, tapped, or activated with the keyboard or other device.

It is important to notice that the next replaced element contains an attribute with no value associated, this syntax corresponds to **boolean** attributes.

```
<img src="switch.svg" alt="light switch" ismap>
```

Now that we understand the utility of attributes, let's navigate through some of them with the snippet above.

The <code>src</code> attribute is used to provide the location of the SVG image asset. The <code>alt</code> attribute provides alternative text describing the contents of the image. The <code>ismap</code> attribute is boolean, and doesn't require a value.

Also, remember that a good practice for writing values requires using lowercase letters. This is just a precaution to avoid conflicts with the [attribute selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors) in CSS or JavaScript.

Another key attribute is <code>role</code>; this one helps assistive technologies and, in some cases, search engines. Due to the element you choose, and therefore the tags you use, should be appropriate for the content you are displaying, as tags have semantic meaning.

<h2 id="dom">Document Object Model (DOM)</h2>

The Document Object Model (DOM) is the data representation of the structure and content of the HTML document. As the browser parses HTML, it creates a JavaScript object for every element and section of text encountered. These objects are called nodes—element nodes and text nodes, respectively.

The HTMLElement interface -from the [HTML DOM API](https://developer.mozilla.org/en-US/docs/Web/API/HTML_DOM_API)- represents the HTML element and all of its descendant nodes. Every other element implements it via an interface that inherits from it. Each inheriting interface has a constructor, methods, and properties. Via the inherited HTMLElement properties, you can access every global attribute, as well as input, pointer, transition, and animation events. Via the individual element's sub-type, such as HTMLAnchorElement and HTMLImageElement, you can access element-specific attribute values and methods.
