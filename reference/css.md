# CSS

CSS stands for Cascading Style Sheets. It is used to describe the *presentation* of a document that is marked up with HTML.

- [Primary reference on CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [More basics here](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics)

**If you have no prior experience in CSS, or, you want to refresh your knowledge, then you can take the following free courses at Codecademy:**

- [Learn CSS on Codecademy](https://www.codecademy.com/learn/learn-css)
- [Learn CSS: Flexbox and Grid](https://www.codecademy.com/learn/learn-css-flexbox-and-grid)

## Basic example

```css
body {
  background-color: #f5f5f5;
  color: #2d2c2c;
}

#container {
  width: 100%;
}

#main {
  margin: 0 auto;
}

h1, h2, h3 {
  text-decoration: underline;
}

.text-section {
  color: #555555;
}

a:hover {
  color: blueviolet;
}
```


## Layout and Breakpoints

- There are many ways to do Layout in CSS
  - We will use [Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox),
    - [ref.](https://tobiasahlin.com/blog/common-flexbox-patterns/)
    - [ref.](https://css-tricks.com/understanding-flex-grow-flex-shrink-and-flex-basis/)
  - You can also look into [Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout), which is another way of doing layout
- Media queries are used for conditional CSS, based on [device properties](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_media_queries)
  - We will look at media queries for [responsive design](https://www.browserstack.com/guide/what-are-css-and-media-query-breakpoints)

```css
#container {
  width: 100%;
  margin: 0 auto;
}

.row {
  display: flex;
  flex-wrap: wrap;
}

.item {
  flex-grow: 0;
  flex-basis: 100%;
  box-sizing: border-box;
}

/* adjustments for large screens, like laptops and desktops */
@media (min-width: 992px) {
  #container {
    width: 992px;
    margin: 0 auto;
  }
  .item {
    flex-basis: 25%;
  }
}
```
