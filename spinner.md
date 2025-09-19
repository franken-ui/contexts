## Spinner

To create a spinner, add the `data-uk-spinner` attribute to a block element.

```html
<div data-uk-spinner></div>
```

### Example

```html
<div data-uk-spinner></div>
```

## Ratio

Add the `ratio: 3` parameter to the `data-uk-spinner` attribute to triple its size – or any other number, depending on how big you want the spinner to be.

```html
<div data-uk-spinner="ratio: 3"></div>
```

### Example

```html
<span class="mr-2" data-uk-spinner="ratio: 3"></span>
<span data-uk-spinner="ratio: 4.5"></span>
```

## Accessibility

The Spinner component automatically sets the appropriate WAI-ARIA roles, states and properties.

- The _spinner_ has the `status` role.
