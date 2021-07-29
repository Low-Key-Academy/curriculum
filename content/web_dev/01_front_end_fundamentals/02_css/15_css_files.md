# CSS Files

We're about to go practice creating more advanced layouts, but before we do, let's make our CSS even better. So far, it's been convenient and easy to put our CSS inside our HTML files. However, most of the time, we actually want our CSS to live in its own file.

Why would we add extra work for ourselves if putting our CSS code in an HTML file is so convenient? Good question!

## Reusability

As engineers, our goal is usually to make computers do as much of the grunt-work as possible. Once our websites start having more than one page, we'll want a way for our CSS to affect every page. If we had to copy and paste our CSS into each new HTML file we create it would be a lot of work! Not to mention the nightmare we'd have to deal with if we wanted to change the CSS on a page. What if we want the CSS for all `h1` tags to change? We'd have to change it in every single HTML page!

Clearly this solution isn't scalable. Luckily, HTML has another trick up its sleeve: the `link` element. The `link` element goes in the `head` element so it can be loaded before the HTML contents get rendered. It allows us to have our HTML read from a CSS file, rather than having to put our styles in the HTML page. It looks something like this:
```html
<head>
  <link rel="stylesheet" type="text/css" href="my_css_file.css" />
</head>
```
If we include this link tag in all of our HTML pages, all we have to do is change the CSS in our CSS file and all of the HTML files will apply CSS from the same common location.

**A quick note on syntax**: We can see that the `link` tag is a self-closing tag that needs a few attributes: `rel`, `type`, and `href`. `rel` tells the browser that the file it's loading is related to the HTML as its stylesheet. `type` tells the browser that it's loading a text file full of CSS code. `href` tells the browser where to find the CSS file.

### Relative vs. Absolute Path

In the example above, we're telling our HTML page (and subsequently our browser) to find a file in the same folder as our HTML file called `my_css_file.css`. This is what's known as a **relative path**. It's relative because its location is *relative* to the location of the HTML file. The HTML file *has to rely on* its own location in your file system to find the location of the CSS file because there's no other indicator that it should look anywhere else.

However, we may wish to load CSS files from a known starting point, like the internet! Often times, these CSS files are our own creations, but sometimes they aren't. One common CSS file people use from the internet is called `normalize`; it aims to make your CSS behave consistently across different browsers. Using it might look something like this:

```html
<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/7.0.0/normalize.min.css" />
```

We can see that the `href` property has a full web URL, starting with `https://`. This tells the browser that instead of looking in your computer's file system, it should look on the web! This is known as an **absolute path** because no matter where your HTML file lives, the browser always knows how to find the CSS file based on an absolute starting point: the internet.
