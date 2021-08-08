# Modifying Boxes

For each of the boxes that make up the box model (margin box, border box, padding box, and content box), we can set the value of each and every side of the box. For instance, we can choose to have a border just on the top or bottom of the element. Additionally, we can put a margin just on the left side or padding on just the right. We have total control over each side of each box. One way to modify a box is to modify the individual side.

```css
.box-fun {
  margin-left: 10px;
  padding-top: 5px;
  border-bottom: 1px dotted black;
}
```

We can see that each property has a `-top`, `-right`, `-bottom`, and `-left` variant. We can also see that borders seem to be more complex, but we'll get back to that.

The problem with applying styles to each individual side is that there's a ton of code to write. Imagine if we needed to modify all four sides of each box! Thankfully, CSS can handle cases where we want to modify more than one side at a time.

```css
.box-fun {
  margin: 10px 20px;
  padding: 5px 10px 15px 5px;
  border: 1px solid black;
}
```

## Top, Right, Bottom, Left

If we just use the `margin`, `padding`, or `border` property, the value can take on more meaning! In this example, elements with the class `box-fun` will have a 10px tall margin on the top and bottom of the element and a 20px margin on the left and right. That's way more convenient than having to set each of those individually!

Here's how it works.
  - If the value contains **1** size, the size will be applied to all sides
  - If the value contains **2** sizes, the first size will be applied to the top and bottom and the second size will be applied to the left and right
  - If the value contains **4** sizes, the first size will be applied to the top, the second will be applied to the right, the third will be applied to the bottom, and the fourth will be applied to the left.

Don't worry too much about memorizing this though. Messing up is cheap! All we have to do if we get it wrong is change a value and reload the page. Just know that you don't have to change individual sides if you don't want to, and you shouldn't worry about using the additional property variants unless you have to!

## Borders

The border property adheres to the some of same rules, but instead of being able to specify the size of all four sides individually, we instead are allowed to modify `border-width`, `border-style`, and `border-color` respectively.

It makes sense this way. Typically, if we're adding a border, we don't want it to have different sizes on different sides. Also, we usually need it to be visible, so it's nice to be able to set the color. Border style just gives us a handful of different border types like `solid`, `dotted`, `dashed`, and more!