# Box Practice

It's time to put all this knowledge of boxes to good use! Start by downloading [this project](../../../../curriculum_companions/web_dev/fe_fun/box_practice/index.html) and adding it to a folder called `box_practice` in your `dev` folder.

Now, open the file up in your browser and crack open those dev tools (stick to the "Elements" tab for this one).

1. Add a class called `box` to each `div` element.
1. Add a margin of `100px` to the top and bottom of each element using the `box` class.
    - What happens when you refresh the page?
    - Did you add margins to the left and right also? If so, try adding just `0px` on the left and right. Can you do this using the 2 value shorthand?
1. Change the margin on the `box` class to just use a bottom margin of `100px`.
    - How did the page change? What is the margin affecting?
1. Let's add some more space, change the margin on all `h2` and `p` elements to 30px on the top and bottom.
    - What changed? Can you inspect an `h2` element in your dev tools? 
    - Notice how the top margin isn't respected by the parent `div`, and not only that, neither is the bottom margin of the `p` element. Even weirder is that the space between the `h2` and `p` elements is only `30px`. What gives? We've run into collapsed "collapsed margins". Unless there's padding on the parent, there is nothing for the element's margin to push against. Also, when the margins of two siblings align, CSS just combines them and renders the biggest of the two. It's a weird quirk, but we have a solution!
1. Add a padding of `20px` to all sides of elements using the `box` class.
    - Use your inspector to see what's going on in the `box` class.
    - Notice how the height of the `box` elements is automatically expanding. Content will automatically grow in the vertical direction until the height of the element is reached. If there is no height set, the div can grow infinitely!
1. Add a `solid`, `1px` wide, `black` border to each element modified by the `box` class.
1. Add rounded edges to the box by setting `border-radius` to `15px`.
1. Add some horizontal space (`40px`) for the whole page using padding.
    - What element should we modify? What elements will work?
    - We like adding padding to the `body` tag. 
1. Resize your browser window. How does the content behave?

