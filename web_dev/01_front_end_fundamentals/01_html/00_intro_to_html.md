# Introduction to HTML

<!-- 
  Objectives
  - Understand the purpose of HTML
  - Learn about tags and elements
-->

HTML, or **Hyper Text Markup Language** is one of the 3 main programming languages web browsers are designed to understand. HTML defines the structure and content of a web page. While the contents of a web page might look pretty boring without CSS, HTML is the backbone of every front end on the internet.

## Anatomy of an HTML Element

In order to understand HTML, we need to understand its most basic building block: the HTML element. An element is a simple piece of code that represents some content in a web page. For instance, to display a few sentences of text on the screen, you might use a `paragraph` element.

An HTML element is typically composed of 3 simple parts:

1. An opening HTML tag, letting the web browser (interpreter) know what type of element to render.
1. Some content to display on screen.
1. A closing HTML tag, indicating where our element's contents end.

It looks something like this:
```html
<p>This is a paragraph element. Notice the opening tag, the written contents, and the closing tag.</p>
```

Let's take a closer look at the code snippet above. `<p>` is the "opening tag". It differs from the corresponding closing tag (`</p>`) by one character. These starting and ending points let the HTML interpreter know that anything between `<p>` and `</p>` is the actual content of the paragraph.

## HTML Attributes

Sometimes, just rendering a paragraph isn't enough. Sometimes we need more functionality from our paragraph than just rendering a piece of text. We might want to make it look prettier with styles or make our site more accessible to people who have visual or physical impairments. There are plenty of moments where a tag on its own doesn't do the full job. That's where attributes come in.

An attribute is used to tell the interpreter that there are special modifications being made to the element. One popular attribute is the `class` attribute, which is useful for CSS. It looks like this:

```html
<p class="some-paragraph-class">This is a paragraph element with a class attribute. Notice how the attribute has a name (class) and a value ("some-paragraph-class"). Also check out how attributes go inside the opening tag, after the name of the element. Finally, notice that the value for class is surrounded by quotation marks. Never forget the quotation marks!</p>
```