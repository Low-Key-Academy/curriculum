# Display

Now that we understand the box model a bit more, we need to learn the final piece of the puzzle for creating the layout we see in our example here:
![structured website example](../images/structured_website_example.png)

So far, we've played around with boxes and what's called "outer display" (`inline` and `block`). Outer display defines how an element behaves relative to its siblings and parents. However, if we want to really yield the full power of CSS layout, we need to master inner display.

## Looking Within

So far, when we've wrapped our contents in `div`s, our elements have behaved the same way as they would if they were just in the `body`. The only difference is that our elements are now confined within the space available in their parent `div`. Modern sites however, have more complex needs. For instance, `block` and `inline` elements alone can't help us achieve the image above very easily. We need the 3 blue boxes to behave differently than plain text in a blog site.

It would be really nice if we could get the blue boxes to go next to each other like `inline` elements, respect the full box model like `block` elements, and flow "responsively" based on the size of the page (to account for phones and tablets). Inner display helps us achieve all these goals.

Contrary to outer display, inner display defines how an element's children will behave. Lucky for us, there are two commonly used inner display types that solve our problems with relative ease.