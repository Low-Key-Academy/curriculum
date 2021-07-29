# CSS FlexBox

Let's start our journey making more advanced layouts by exploring CSS FlexBox (flexible box layout), or `flex` display. Let's keep looking at our example:
![structured website example](../images/structured_website_example.png)

FlexBox gets its name for its ability to make the space between elements flexible. Essentially, `flex` allows us to control the spacing of elements in one direction, either horizontally or vertically.

In order for us to use `flex` on the blue boxes, we need to create a new container, that will treat all of the concert boxes as children.

```html
<body>
  <h1>Concerts in Denver</h1>
  <div class="concert-container">
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
  </div>
</body>
```

Now, let's add an inner display type of `flex` to our `concert-container` class.
```css
.concert-container {
  display: flex;
}
```
If you want to follow along, here's the CSS for the `concert` class:
```css
.concert {
  width: 22%;
  border: 2px solid black;
  background-color: lightblue;
  border-radius: 15px;
  padding: 5px 20px;
}
```

You might have noticed that our boxes are now sitting right next to each other! The inner display of the `concert-container` class is changing the way its children are behaving!

## WTFlex?

We can clearly see that `flex` has made a difference in our page, but let's try t