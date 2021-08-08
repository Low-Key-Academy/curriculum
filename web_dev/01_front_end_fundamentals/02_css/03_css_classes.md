# CSS Classes 

So far we've seen one approach to adding more specific CSS selectors to HTML elements, but applying styles directly to our elements has some serious drawbacks.

Most importantly, the element style approach is extremely hard to maintain. Let's imagine that you work on a website with dozens of HTML files, each with a dozen paragraph tags that have one of two different overrides. By default all your paragraphs have black text on a white background, but 25% of your paragraphs need to have a blue background and another 25% need to have a red background. So far so good, the element style approach doesn't seem that unreasonable. Now let's imagine that your team decides one day that red is just too aggressive and is bumming everyone out, so you make the executive decision to change all the red paragraphs to yellow instead. Uh oh, now you have to go through dozens of files, each with dozens of paragraphs, and change each individual style tag from red to yellow. Now let's imagine that you have more than one property on each paragraph that needs to change. This is getting out of hand quickly.

Instead of changing hundreds of lines of code for a simple color change, we need a better solution. Lucky for us, CSS and HTML a handy solution for this exact problem, CSS classes.

## Changing Styles... With Class

CSS classes allow us to be more specific than the generic element styles, while also giving us a more maintainable way of doing so. In order to use a CSS class as a CSS selector, we need to add our class to an HTML element. We do so by using the class attribute:
```html
<p class="primary-bg">This is a paragraph tag with a class called primary-bg</p>
```
This tells the browser that the paragraph has a class called `primary-bg`.  Now, we just need to tell our CSS to apply styles to every element with our new class name!

```css
.primary-bg {
  background-color: blue;
}
```

**Quick Note**: Classes in HTML are usually `snake-case`, where words are separated by hyphens.

Notice that in our css, the name of our class starts with a `.`. This is to help both humans and browsers understand that this selector represents a class, which is more specific than an element selector.

Now imagine that we have to change all the blue backgrounds on our site to green; all we have to do is change one line in the `primary-bg` class and we're done!