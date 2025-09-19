## Pagination

The Pagination component consists of button-like styled links, that are aligned side by side in a horizontal list.

| Class          | Description                                                                                                                    |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| `.uk-pgn`      | Add this class to a `<ul>` element to define the Pagination component. Use `<a>` elements as pagination items within the list. |
| `.uk-active`   | Add this class to a list item to apply an active state and use a `<span>` instead of an `<a>` element.                         |
| `.uk-disabled` | Add this class to a list item to apply a disabled state and use a `<span>` instead of an `<a>` element.                        |

To add an icon, just add the `data-uk-pgn-previous` or `data-uk-pgn-next` attribute to a `<span>` element inside a pagination item.

### Example

```html
<nav>
  <ul class="uk-pgn uk-pgn-default">
    <li>
      <a href="#">
        <span class="mr-2" data-uk-pgn-previous></span>
        Previous
      </a>
    </li>
    <li>
      <a href="#">Next <span class="ml-2" data-uk-pgn-next></span></a>
    </li>
  </ul>
</nav>

<nav class="mt-4" aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-default">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>
```

## Style modifiers

There are several style modifiers available. Just add one of the following classes to apply a different look.

| Class                 | Description               |
| --------------------- | ------------------------- |
| `.uk-pgn-default`     | Adds the default style.   |
| `.uk-pgn-primary`     | Adds a primary style.     |
| `.uk-pgn-secondary`   | Adds a secondary style.   |
| `.uk-pgn-destructive` | Adds a destructive style. |
| `.uk-pgn-ghost`       | Adds a ghost style.       |

### Example

```html
<nav aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-default">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>

<nav class="mt-4" aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-primary">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>

<nav class="mt-4" aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-secondary">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>

<nav class="mt-4" aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-destructive">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>

<nav class="mt-4" aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-ghost">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>
```

## Size modifiers

There are several size modifiers available. Just add one of the following classes to make the pagination smaller or larger.

| Class        | Description               |
| ------------ | ------------------------- |
| `.uk-pgn-xs` | Applies extra small size. |
| `.uk-pgn-sm` | Applies small size.       |
| `.uk-pgn-md` | Applies medium size.      |
| `.uk-pgn-lg` | Applies large size.       |

### Example

```html
<nav aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-xs uk-pgn-default">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>

<nav aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-sm uk-pgn-default mt-4">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>

<nav aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-md uk-pgn-default mt-4">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>

<nav aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-lg uk-pgn-default mt-4">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>
```

## Alignment

The Pagination component utilizes flexbox, so navigations can easily be aligned with Flex utility classes from Tailwind CSS.

```html
<ul class="uk-pgn justify-center">
  ...
</ul>
```

### Example

```html
<nav aria-label="Pagination">
  <ul class="uk-pgn uk-pgn-default justify-center">
    <li>
      <a href="#">
        <span data-uk-pgn-previous></span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">6</a></li>
    <li class="uk-active"><span aria-current="page">7</span></li>
    <li><a href="#">8</a></li>
    <li class="uk-disabled"><span>...</span></li>
    <li><a href="#">20</a></li>
    <li>
      <a href="#">
        <span data-uk-pgn-next></span>
      </a>
    </li>
  </ul>
</nav>

<nav>
  <ul class="uk-pgn uk-pgn-default mt-4 justify-around">
    <li>
      <a href="#">
        <span class="mr-2" data-uk-pgn-previous></span>
        Previous
      </a>
    </li>
    <li>
      <a href="#">Next <span class="ml-2" data-uk-pgn-next></span></a>
    </li>
  </ul>
</nav>
```

## Accessibility

The previous/next pagination adheres to the [button pattern](https://www.w3.org/WAI/ARIA/apg/patterns/button/) and automatically sets the appropriate WAI-ARIA roles, states and properties.

- The _prev/next pagination items_ have the `button` role and the `aria-label` property.

### Internationalization

The Pagination component uses the following translation strings. Learn more about [translating components](https://franken-ui.dev/docs/2.1/accessibility#internationalization).

| Key     | Default              | Description             |
| ------- | -------------------- | ----------------------- |
| `label` | `Next/Previous page` | `aria-label` attribute. |
