# Intro to CSS

<!-- 
  Objectives:
    - Understand the purpose of CSS
    - Understand the anatomy of CSS rules
 -->

You may have noticed that the HTML you've been writing doesn't exactly produce the most exciting results. Sure, it's nice to put contents on the page, but modern web users expect complex, beautiful interfaces. That's where CSS comes in.

CSS, or Cascading Style Sheets, is what defines the look and feel of the web pages we use. It can tell the browser to do simple things like changing the color of text or the size of an image, but it can also define complex animations, color gradients, and more!

## Anatomy of a CSS Rule

The most basic piece of CSS is the CSS rule. A rule is composed of 2 things:
1. A CSS selector, which matches up with 0 or more HTML elements
1. Properties and values to apply to the elements that match the selector

Here's a CSS rule that changes the text color in all paragraph elements to blue:
```css
p {
  color: blue;
}
```

Notice that our selector `p` matches the HTML paragraph (`<p></p>`) element name. Also notice the curly braces `{}`; these tell the interpreter where the CSS rule starts and ends. It's the same concept as opening and closing HTML tags. Finally, notice the property/value pair `color: blue;`. `color` is the name of the property and `blue` is the name of the value. The property always comes first and the value always comes second, there's always a colon `:` between them, and there's always a semicolon `;` after the value. The semicolon is another indicator character for the interpreter. It tells the browser that the value is over and that a new pair may be coming afterward, like so:

```css
p {
  color: blue;
  font-size: 14px;
  font-family: Arial, sans-serif;
  background-color: yellow;
}
```