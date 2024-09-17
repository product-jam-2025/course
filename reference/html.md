# HTML

HTML stands for HyperText Markup Language. It is used to "mark up" content with *meaning* and *structure*. It is the foundation of the web.

With HTML, content (images, text, data, etc) is *annotated* as *elements* defined by *tags*, which are names surrounded by `<` and `>`.

- [Primary reference on HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)

**If you have no prior experience in HTML, or, you want to refresh your knowledge, then you can take the following free course at Codecademy:**

- [Learn HTML on Codecademy](https://www.codecademy.com/learn/learn-html)

## Basic example

```html
<html>

  <head>
    <meta charset=utf-8>
    <title>My Page</title>
    <link rel="stylesheet" href="index.css" />
  </head>

  <body>
    <div id="main">
      <h1>My Heading</h1>
      <div>
        <p class="text-section">
          Here is <a href="https://example.com">link</a>.
        </p>
      </div>
    </div>
    <script src="index.js"></script>
  </body>

</html>
```
