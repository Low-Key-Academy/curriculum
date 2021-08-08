# CSS Classes... Again

You might have realized that classes are **element agnostic**. In other words, we can now start attaching the `primary-bg` class to any other element that we'd like to have a blue background.

```html
<h1 class="primary-bg">I'm a header with a blue background</h1>
<p>I'm a normal paragraph</p>
<p class="primary-bg">I'm a paragraph with a blue background</p>
```
This is really useful because we can start defining classes that provide generic styles that work across elements, which helps us keep our site looking consistent.

We can also add more than one class to the same element. For instance, we might write a `secondary-text` class that has the following CSS. Added to our original CSS, it looks like this:
```css
.primary-bg {
  background-color: blue;
}

.secondary-text {
  color: white;
}
```

Now let's add to our HTML:
```html
<h1 class="primary-bg secondary-text">I'm a header with a blue background</h1>
<p>I'm a normal paragraph</p>
<p class="primary-bg">I'm a paragraph with a blue background</p>
```

Notice how our `h1` element has both the `primary-bg` and `secondary-text` classes applied to it. Keep in mind, the interpreter needs the space between classes to differentiate between the classes `primary-bg` and `secondary-text`, otherwise it would think there was just one class called `primary-bgsecondary-text`.