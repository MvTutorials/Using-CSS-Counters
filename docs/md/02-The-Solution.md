<!-- The Solution -->
<section
  id="the-solution"
  aria-labelledby="the-solution"
  data-item="The Solution"
>
  <h2><a href="#the-solution">The Solution</a></h2>

The solution is to use a [CSS counter](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_counter_styles/Using_CSS_counters). You'll need to do four things:

1. Declare a counter and give it an initial value
2. Increment the counter for each element that should be numbered
3. Display the newly-incremented value in the numbered element. This is usually done using the `content` of a `::before` pseudo-element
4. Add `". "` as decoration in the `content` of the `::before` pseudo-element.

Taking the CSS that is used for the rest of the styling as given, you can add this rule:

```css-#
ol {
  counter-reset: item 0;

  a::before {
    counter-increment: item 1;
    content: counter(item) ". ";
  }
}
```

This almost solves the problem:

![The link elements are now numbered](images/almost.webp)

<details class="tip" open>
<summary>Default values</summary>
The default value for `counter-reset` is `0`, and the default value for `counter-increment` is `1`, so the less explicit CSS below has exactly the same effect.

```css-#
ol {
  counter-reset: item;

  a::before {
    counter-increment: item;
    content: counter(item) ". ";
  }
}
```

</details>

## Hiding the built-in numbering system

To obtain the effect you want, you now need to hide the built-in numbering system for `<ol>` items:

```css-#
<i>ol {
  counter-reset: item;</i>
  <b>list-style-type: none;</b><i>

  a::before {
    counter-increment: item;
    content: counter(item) ". ";
  }
}</i>
```

</section>