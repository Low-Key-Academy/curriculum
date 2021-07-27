# I Feel Pretty

It's time to learn how to use CSS in our own HTML files and learn about some basic properties we have control over.

## Adding CSS to HTML

One of the quickest and easiest ways to add CSS to your HTML file is by using the `style` element. It looks something like this:

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        font-family: 'Times New Roman', serif;
        color: red;
        font-weight: bold;
      }
    </style>
  </head>
  <body>
    <h1>Hello World</h1>
    <p>This is a super interesting bit of text that could use some spicing up.</p>
  </body>
</html>
```

Notice how the `style` element goes between the `head` tags. Within the `style` tags, we can freely write CSS code without worrying about HTML syntax rules!

## Taking the Training Wheels Off
It's time to add some flair to your own website. Start by opening the band website you built and do the following.

1. Add a `style` tag in the `head`
1. Change the text color of all the paragraphs using the `color` property
    - What colors are available to you?
1. Change the font of all the headers to `sans-serif` using the `font-family` property
    - What fonts do you have available to you?
1. Change the width of any images to `250px` using the `width` property
    - What happens if you also change the `height`?
1. Add a background color to the entire list using the `background-color` property
1. Now make all the list items orange
1. Change the background color of the whole page
    - What selector should you use? Which selectors *can* you use?