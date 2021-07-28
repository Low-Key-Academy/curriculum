# Structural Elements

Thankfully, the web isn't just blog posts anymore, but in order to create the kinds of complex visuals we're accustomed to, we need to start adding more structure to our HTML documents.

Let's say we want to create a website that looks like this:
![structured website example](../images/structured_website_example.png)

You might recognize that the page's contents are composed entirely of `paragraphs` and `headers`. Just the contents of this page might look something like this in HTML:
```html
<body>
  <h1>Concerts in Denver</h1>
  <h3>The Bumblebees</h3>
  <h4>June 29</h4>
  <p>
    The Bumblebees are the latest, greatest fake band in the Denver
    music scene.
  </p>
  <h3>The Blowhards</h3>
  <h4>July 3</h4>
  <p>The Blowhards are just okay!</p>
  <h3>The Dunning-Kreuger Effect</h3>
  <h4>July 5</h4>
  <p>They know a lot about how to make you enjoy their show.</p>
</body>
```

Using CSS, it would be almost impossible (or at least really annoying) to make the HTML look like the image if we leave it as-is. We're immediately presented with multiple problems.

1. The image has 3 clear sections for 3 different concerts with their own background color and border. Right now, there's no way to put a border around the section without putting a border around each individual element.
1. The `paragraph` and `header` elements are all `block` elements, so their CSS boxes are going to take up all of the available horizontal space possible. We don't yet know how to make block elements render side-by-side.

To solve both of these problems, we need to be able to divide this content into individual sections. That's where the `<div>` element comes in. A `div`'s only job is to create a division in HTML content. It's really useful for more complicated styling like the styling seen in the image above. Let's take a look at how we might break this content up into sections:

```html
<body>
  <h1>Concerts in Denver</h1>
  <div class="concert">
    <h3>The Bumblebees</h3>
    <h4>June 29</h4>
    <p>
    The Bumblebees are the latest, greatest fake band in the Denver
    music scene.
    </p>
  </div>
  <div class="concert">
    <h3>The Blowhards</h3>
    <h4>July 3</h4>
    <p>The Blowhards are just okay!</p>
  </div>
  <div class="concert">
    <h3>The Dunning-Kreuger Effect</h3>
    <h4>July 5</h4>
    <p>They know a lot about how to make you enjoy their show.</p>
  </div>
</body>
```
Look at how the `div`s are creating 3 distinct sections for our content. We could change the `concert` class in CSS to have a border and a background color and we've solved our first problem!

## Boxes are Like... Sooooo Meta

Solving our second problem requires more understanding. If we don't change anything else, our header and paragraph elements will appear to take up the entire horizontal width of the page, but that's not exactly true anymore. Now, our paragraphs and headers are nested *inside* of a `div`.

`div` elements are `block` elements, and they will respect any width value we give them. So if we change the width property in the `concert` class to `200px`, all the `div`s will be set to `200px` wide. The paragraph and header elements inside the `div`s will now collapse as well. `block` elements can only take up the horizontal space available in their parent!

Try it and see for yourself!

To describe the relationship between HTML elements, it's useful (and common) to use the ancestry analogy. In this case, the `div`s are parents to the `h3`, `h4`, and `p` elements. Each `div` is a sibling to each other `div` and the `h1`.

**Quick Tip**: Notice how useful indentation is in our HTML code! We can easily see the ancestral relationship of all of our elements just by looking at the indentation! It might not matter to the browser, but it sure as heck makes it easier to write code!