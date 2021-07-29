# The CSS Box Model

Changing sizes and colors is useful, but if we're going to get anywhere near creating the kinds of visual displays we've become accustomed to on the web, we need to understand the CSS box model.

Each element on the page is surrounded by its own box (literally a rectangle). This box defines the boundaries of an element. You may have noticed that when you added a background color to an element, it changed the background of your element in the shape of a rectangle. That rectangle is the element's now visible CSS box!
## Basic Boxes

There are two basic kinds of boxes in CSS: `block` and `inline`. In order to understand the behavior of these boxes, it's useful to draw comparisons to the kinds of content we're used to seeing.

When CSS was being created, a vast portion of the web was text-based, so let's think of `inline` and `block` boxes in the context of a blog post. On a blog post, we typically see headers followed by paragraphs, each followed by line breaks to visually create space. Headers and paragraphs expand their box to fill space so we know where one ends and the others begin. This behavior is the behavior of a `block` box.

An `inline` box is meant for content that can go inside of a `block`. For instance, you might want a link in your paragraph or you might want one word in a sentence to be bold. If anchor `<a>` elements or `<strong>` elements behaved the same way as `block` elements, the page would have a new visual section for every link or bold word. You can see it in action on *the webpage you're looking at right now*. Notice how the last few words of the last sentence were italicized with an `inline` element, while all the paragraphs and headers are clearly taking up their own section as `block` elements. We didn't have to write any additional CSS code to make this happen.
