# CSS Specificity

You may have noticed that using HTML element selectors seems like kind of an "all or nothing" approach to changing styles. You might want all of the paragraphs on your web page to have a blue background, but what if we want only some of our paragraphs to have a blue background and others to have a green background? If all we had were HTML element selectors we'd be in a pickle. Luckily, we have other options!

## Element Styling

The first, and possibly most obvious thing to do, might be to just apply specific styles directly to an HTML element, which we can do with the `style` attribute.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        background-color: aqua;
      }
    </style>
  </head>
  <body>
    <p>First blue paragraph</p>
    <p>Second blue paragraph</p>
    <p style="background-color: yellow;">First yellow paragraph</p>
    <p style="background-color: yellow;">Second yellow paragraph</p>
    <p style="background-color: yellow;">Third yellow paragraph</p>
  </body>
</html>
```
The resulting HTML page will render 2 blue paragraphs followed by 3 yellow paragraphs, which definitely accomplished our goal, but it's not exactly an elegant solution. Try copy/pasting the code from the example into an HTML file and opening it up to see it work!

## A Note on Specificity

First, let's figure out why the CSS above works the way it does. CSS applies styles based on **specificity**. Specificity is a crucial concept to understand in CSS because it impacts basically all of the CSS you'll ever write. It's also part of the reason *why CSS is called CSS*, so pay attention to this next part.

CSS will always give the *most specific* selector that applies to an element precedence. Technically, in the above example, CSS applies the blue background color to all of the paragraph tags in the entire page, but that's a pretty general selector. The element style attribute is saying that "these specific paragraphs should have styling applied directly to them". This specific CSS *overrides* the style they got from the `p` selector.

Let's explore this even further. What happens when we add another property to our CSS?

```css
p {
  background-color: aqua;
  color: purple;
}
```

Stop here and try it yourself! What happens?

We see that the paragraphs have different background colors, but the same text color! This is because CSS only overrides the *specific properties* that were changed in the specific style attributes.

It may seem strange for CSS to work this way, but don't fret, we'll keep learning why this *cascading* approach is useful in future lessons.