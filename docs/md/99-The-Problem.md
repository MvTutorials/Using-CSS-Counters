---
title: Using CSS Counters
subtitle: Numbering elements not in an ordered list
month: December 2024
organization: HTM-Elves
repo: Using-CSS-Counters
---
<section
  id="the-problem"
  aria-labelledby="the-problem"
  data-item="The Problem"
>
  <h2><a href="#the-problem">The Problem</a></h2>

  In this tutorial, I will show you how to use [CSS counters](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_counter_styles/Using_CSS_counters) to number the link elements in a navigation menu.

  Imagine that you have an `<ol>` element with the following structure:

```html-#
<ol>
  <li><a href="#beginning">Beginning</a></li>
  <li><a href="#middle">Middle</a></li>
  <li><a href="#end">End</a></li>
</ol>
```

You've used an ordered list, because you want the list items to be numbered. When you apply your best CSS styling, you really want the items to appear like this:

![What you want](images/expected.webp)

Instead, the numbers for each list item appear outside the `<li>` elements, like this:

![What you get](images/actual.webp)

How can you fix this?

</section>
