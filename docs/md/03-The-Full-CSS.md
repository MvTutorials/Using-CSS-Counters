<!-- The Full CSS -->
<section
  id="the-full-css"
  aria-labelledby="the-full-css"
  data-item="The Full CSS"
>
  <h2><a href="#the-full-css">The Full CSS</a></h2>

Below is the full CSS that will produce the desired effect, for reference.

![The desired effect](images/expected.webp)

```css
body {
  margin: 0;
  padding: 0;
  min-height: 100vh;

  display: flex;
  justify-content: center;
  align-items: center;

  font-family: Helvetica, Arial, sans-serif;
  color: #ddd;
  background-color: #222;
}
ol {
  width: 8em;
  list-style-type: none;
  counter-reset: item 0;

  li {
    margin: 0.5em;
    border: 1px outset white;
    border-radius: 0.5em;
    box-sizing: border-box;
  }

  a {
    color: inherit;
    text-decoration: none;
    display: inline-block;
    padding: 0.5em;
    width: 100%;
    box-sizing: border-box;

    &::before {
      counter-increment: item 1;
      content: counter(item) ". ";
    }
  }
}
```

</section>