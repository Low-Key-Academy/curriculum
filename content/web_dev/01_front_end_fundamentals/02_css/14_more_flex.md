# More FlexBox

So far, we've changed the spacing of elements in one direction, but let's explore how `flex` gives us a lot of power with just three key properties: `justify-content`, `align-items`, and `flex-direction`.

## My, How Cartesian of You

FlexBox works by setting up two axes, horizontal and vertical, x and y. By default, the x axis is the **main axis**. 

To change spacing on the main axis, we change the `justify-content` property. We saw it in action in the last page. Some valid values are `space-between`, `space-evenly`, and `space-around`.

However, sometimes we need to modify the behavior of the **cross axis**. For instance, we might have three elements that have different heights. They look good horizontally now that we've added a value to the `justify-content` property, but we want each element to align with their siblings. To modify the elements along the cross axis, we modify the `align-items` property.

Finally, to swap the main and cross axes, we can override the `flex-direction` property. By default, `flex-direction` is set to `row`, which ensures that the x axis is the main axis. If we set `flex-direction` to `column`, the y axis becomes the main axis and the x axis becomes the cross axis. This is useful for vertical spacing, especially within an element that has a preset height.

