## Headings

Add one of the following classes to modify the size and style of headings. Usually, these classes would be used on heading elements, but they work also with any other element like a `div` element.

| Class    | Description                            |
| -------- | -------------------------------------- |
| `.uk-h1` | Add this class to apply an h1 heading. |
| `.uk-h2` | Add this class to apply an h2 heading. |
| `.uk-h3` | Add this class to apply an h3 heading. |
| `.uk-h4` | Add this class to apply an h4 heading. |

### Example

```html
<h1 class="uk-h1 mt-4">h1</h1>
<h1 class="uk-h2 mt-4">h2</h1>
<h1 class="uk-h3 mt-4">h3</h1>
<h1 class="uk-h4 mt-4">h4</h1>
```

## Hero

Add one of the following classes to apply hero headings. These classes are typically used to add a prominent message with a very large font size.

| Class          | Description                                      |
| -------------- | ------------------------------------------------ |
| `.uk-hero-sm`  | Add this class to apply a small-sized heading.   |
| `.uk-hero-md`  | Add this class to apply a medium-sized heading.  |
| `.uk-hero-lg`  | Add this class to apply a large-sized heading.   |
| `.uk-hero-xl`  | Add this class to apply a xlarge-sized heading.  |
| `.uk-hero-2xl` | Add this class to apply a 2xlarge-sized heading. |
| `.uk-hero-3xl` | Add this class to apply a 3xlarge-sized heading. |

### Example

```html
<h1 class="uk-hero-sm mt-4">Small</h1>
<h1 class="uk-hero-md mt-4">Medium</h1>
<h1 class="uk-hero-lg mt-4">Large</h1>
<h1 class="uk-hero-xl mt-4">XL</h1>
<h1 class="uk-hero-2xl mt-4">2XL</h1>
<h1 class="uk-hero-3xl mt-4">3XL</h1>
```

## Heading Styles

Add one of the following classes to modify the size and style of headings.

| Class                 | Description                                                      |
| --------------------- | ---------------------------------------------------------------- |
| `.uk-heading-divider` | Add this class to apply a divider to a heading.                  |
| `.uk-heading-line`    | Add this class to apply a vertically centered line to a heading. |
| `.uk-heading-bullet`  | Add this class to apply a bullet to a heading.                   |

### Example

```html
<h1 class="uk-hero-sm uk-heading-divider">Divider</h1>
<h1 class="uk-hero-sm uk-heading-line mt-4">
  <span>Line</span>
</h1>
<h1 class="uk-hero-sm uk-heading-line uk-text-right mt-4">
  <span>Line</span>
</h1>
<h1 class="uk-hero-sm uk-heading-line mt-4 text-center">
  <span>Line</span>
</h1>
<h1 class="uk-hero-sm uk-heading-bullet mt-4">Bullet</h1>
```

## Paragraph

### Example

```html
<p class="uk-paragraph">
  The king, seeing how much happier his subjects were, realized the error of his
  ways and repealed the joke tax.
</p>
```

## Blockquote

### Example

```html
<blockquote class="uk-blockquote">
  "After all," he said, "everyone enjoys a good joke, so it's only fair that
  they should pay for the privilege."
</blockquote>
```

## Inline code

### Example

```html
<code class="uk-codespan">franken-ui</code>
```

## Text

Franken UI offers various text utilities to style your text.

| Class               | Description                                                                                                          |
| ------------------- | -------------------------------------------------------------------------------------------------------------------- |
| `.uk-text-lead`     | <span class="uk-text-lead">Add this class to highlight text, for example in article subtitles.</span>                |
| `.uk-text-meta`     | <span class="uk-text-meta">Add this class to a paragraph that contains meta text about an article or similar.</span> |
| `.uk-text-sm`       | <span class="uk-text-sm">Add this class to apply a small font size.</span>                                           |
| `.uk-text-base`     | <span class="uk-text-base">Add this class to apply the default the font size.</span>                                 |
| `.uk-text-truncate` | Prevents text from wrapping into multiple lines, truncating it and displaying an ellipsis instead.                   |
| `.uk-text-break`    | Breaks strings, if their length exceeds the width of their container.                                                |

### Text background

To apply a gradient or background image to text, add the `.uk-text-background` class to a `<span>` element inside the text element. Styles that don't define a `background-image`, will apply the primary color.

```html
<h1><span class="uk-text-background"></span></h1>
```

### Example

```html
<h1 class="uk-hero-lg">
  <span
    class="uk-text-background"
    style="background-image: linear-gradient(90deg, #e4e405 0%, #f01ebb 100%)"
    >Franken UI</span
  >
</h1>
```
