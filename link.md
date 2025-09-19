## Link

To apply this component, add the `.uk-link` class to an `<a>` element.

### Example

```html
<a class="uk-link" href="#">Link</a>
```

## Muted modifier

If you want the link to apply a muted style instead, just add the `.uk-link-muted` class to the anchor element. You can also add the class to a parent element, and it will be applied to all `<a>` elements inside it.

```html
<a class="uk-link-muted" href="#"></a>
```

### Example

```html
<a class="uk-link-muted" href="#">Link</a>

<p class="uk-link-muted mt-4">
  Lorem ipsum <a href="#">dolor sit</a> amet, consectetur adipiscing elit, sed
  do <a href="#">eiusmod</a> tempor incididunt ut
  <a href="#">labore et</a> dolore magna aliqua.
</p>
```

## Text modifier

To make a link appear like body text and apply a hover effect, add the `.uk-link-text` class to the anchor element. You can also add the class to a parent element, and it will be applied to all `<a>` elements inside it. This is useful for link lists in the page footer.

```html
<a class="uk-link-text" href="#"></a>
```

### Example

```html
<ul class="uk-link-text uk-list">
  <li><a href="#">Link</a></li>
  <li><a href="#">Link</a></li>
  <li><a href="#">Link</a></li>
</ul>
```

## Reset modifier

To reset a link's color, so that it inherits the color from its parent, add the `.uk-link-reset` class. There won't be any hover effect at all. This is useful for links inside heading elements. You can also add the class to a parent element, and it will be applied to all `<a>` elements inside it.

### Example

```html
<a class="uk-link-reset" href="#">Link</a>

<h3 class="uk-h3">
  <a class="uk-link-reset" href="#">Heading</a>
</h3>
```

## Toggle

To use an anchor as a parent element and apply the link style on one of its child elements, just add the `.uk-link-toggle` class to the parent element and one of the `.uk-link-*` classes to the child element. For instance, you can link the whole card and still have the hover effect on the heading.

```html
<a class="uk-link-toggle" href="#">
  <span class="uk-link-text"></span>
</a>
```

### Example

```html
<a href class="uk-card uk-card-body uk-link-toggle block max-w-sm">
  <h3 class="uk-card-title">
    <span class="uk-link-text">Heading</span>
  </h3>
  <p class="mt-4">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua.
  </p>
</a>
```
