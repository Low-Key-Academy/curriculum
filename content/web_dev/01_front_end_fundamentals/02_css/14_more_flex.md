# More FlexBox

So far, we've changed the spacing of elements in one direction, but let's explore how `flex` gives us a lot of power with just three key properties: `justify-content`, `align-items`, and `flex-direction`.

## My, How Cartesian of You

FlexBox works by setting up two axes, the **main axis** and the **cross axis**. By default, the main axis is the horizontal, or x-axis.

To change how the space between elements behaves on the main axis, we change the `justify-content` property. We saw it in action in the last page. Some valid values are `space-between`, `space-evenly`, and `space-around`.

However, sometimes we need to modify the behavior of the **cross axis**. For instance, we might have three child elements in our flex container that have different heights. They're behaving the way we want them to on the main axis now that we've added a value to the `justify-content` property, but we want each element to **align** with its siblings.

To change **alignment** on the cross axis, we just need to change the `align-items` property. This alignment works on the **cross axis**. For instance, we might want our flex children to align so that the center of each element is aligned with each other, or we might want the tops or bottoms of the elements to line up with each other. Some valid values for this property are: `start`, `end`, `center`, and `stretch`. Why not just use "top" and "bottom"? Because of the `flex-direction` property!

The `flex-direction` property allows us to switch axes. This would allow us to flexibly control the spacing between items vertically and align them horizontally. If we set `flex-direction` to `column` (the default is `row`), the y axis becomes the main axis and the x axis becomes the cross axis.

