# Introduction to HTML

<!-- 
  Objectives
  - Understand the purpose of HTML
  - Learn about tags and elements
  - Understand the anatomy of an HTML document
  - Learn how to create and view an HTML file?
-->

HTML, or **Hyper Text Markup Language** is one of the 3 main programming languages web browsers are designed to understand. HTML defines the structure and content of a web page. While the contents of a web page might look pretty boring without CSS, HTML is the backbone of every front end on the internet.

## Anatomy of an HTML File

HTML is composed of a series of **elements**, many of which can be nested to create the structure of a web page. In turn, elements are composed of **tags**, which give the browser more information about how to handle the contents within the element. To understand this better, let's take a look at a very basic HTML document.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>
    <h1>Hello World</h1>
  </body>
</html>
```

Let's break this down into smaller chunks. First, notice the `<!DOCTYPE html>` tag. The browser is going to read this HTML page top-to-bottom, left-to-right. This line tells the browser that it's reading an HTML page. This is necessary because there are other markup languages that look a heck of a lot like HTML (XML, for instance). In a lot of ways, this tag is an anomaly. It doesn't really follow the same rules as most other tags in HTML because it is meant to be a marker, not to be confused by people or machines.

Next, let's look at the second line: `<html lang="en">`. This is the opening tag of our **html element**. Now, if we look at the last line, we can see the closing tag: `</html>`.