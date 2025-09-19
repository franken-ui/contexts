## Alert

To apply this component, add the `data-uk-alert` attribute to a block element.

```html
<div class="uk-alert" data-uk-alert></div>
```

### Example

```html
<div class="uk-alert" data-uk-alert>
  Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
  incididunt ut labore et dolore magna aliqua.
</div>
```

## Close button

To create a close button and enable its functionality, add the `.uk-alert-close` class to a `<button>` or `<a>` element inside the alert box. To apply a close icon, add the `data-uk-close` attribute from the [Close component](https://franken-ui.dev/docs/2.1/close).

```html
<div class="uk-alert" data-uk-alert>
  <a href class="uk-alert-close"></a>
</div>
```

### Example

```html
<div class="uk-alert" data-uk-alert>
  <a href class="uk-alert-close" data-uk-close></a>
  <div class="uk-alert-title">Notice</div>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua.
  </p>
</div>
```

## Destructive modifier

Just add `.uk-alert-destructive` class to apply a different look.

### Example

```html
<div class="uk-alert uk-alert-destructive" data-uk-alert>
  <a href class="uk-alert-close" data-uk-close></a>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt.
  </p>
</div>
```

## Component options

Any of these options can be applied to the component attribute. Separate multiple options with a semicolon. [Learn more](https://franken-ui.dev/docs/2.1/javascript#component-configuration)

| Option      | Value        | Default           | Description                         |
| ----------- | ------------ | ----------------- | ----------------------------------- |
| `animation` | Boolean      | `true`            | Fade out or hide directly.          |
| `duration`  | Number       | `150`             | Animation duration in milliseconds. |
| `sel-close` | CSS selector | `.uk-alert-close` | The close trigger element.          |

`animation` is the _Primary_ option and its key may be omitted, if it's the only option in the attribute value.

```html
<span data-uk-toggle=".my-class"></span>
```

## JavaScript

Learn more about [JavaScript components](https://franken-ui.dev/docs/2.1/javascript#programmatic-use).

### Initialization

```javascript
UIkit.alert(element, options);
```

### Events

The following events will be triggered on elements with this component attached:

| Name         | Description                                                                                    |
| ------------ | ---------------------------------------------------------------------------------------------- |
| `beforehide` | Fires before an item is hidden. Can prevent hiding by calling `preventDefault()` on the event. |
| `hide`       | Fires after an item is hidden.                                                                 |

### Methods

The following methods are available for the component:

#### Close

```javascript
UIkit.alert(element).close();
```

Closes and removes the Alert.
