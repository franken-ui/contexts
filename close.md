## Close

To apply this component, add the `data-uk-close` attribute to an `<a>` or `<button>` element.

```html
<button type="button" data-uk-close></button>

<a href="" data-uk-close></a>
```

### Example

```html
<button type="button" aria-label="Close" data-uk-close></button>
```

## Close in alerts

This is an example of how this component is used with an alert box from the [Alert component](https://franken-ui.dev/docs/2.1/alert).

```html
<div class="uk-alert" data-uk-alert>
  <a href class="uk-alert-close" data-uk-close></a>
</div>
```

### Example

```html
<div class="uk-alert" data-uk-alert>
  <button
    class="uk-alert-close"
    type="button"
    aria-label="Close"
    data-uk-close
  ></button>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt.
  </p>
</div>
```

## Close in drops

This is an example of how this component is used with the [Drop component](https://franken-ui.dev/docs/2.1/drop).

```html
<div data-uk-drop>
  <button class="uk-drop-close" type="button" data-uk-close></button>
</div>
```

### Example

```html
<div class="uk-inline">
  <button class="uk-btn uk-btn-default" type="button">Click</button>
  <div data-uk-drop="mode: click">
    <div class="uk-card uk-card-body">
      <button
        class="uk-drop-close"
        type="button"
        aria-label="Close"
        data-uk-close
      ></button>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt.
      </p>
    </div>
  </div>
</div>
```

## Close in modals

This is an example of how this component is used with the [Modal component](https://franken-ui.dev/docs/2.1/modal).

```html
<div id="modal" data-uk-modal>
  <div class="uk-modal-dialog uk-modal-body">
    <button
      class="uk-modal-close absolute right-4 top-4"
      type="button"
      data-uk-close
    ></button>
  </div>
</div>
```

### Example

```html
<a class="uk-btn uk-btn-default" href="#modal" data-uk-toggle> Open modal </a>

<div class="uk-modal uk-flex-top" id="modal" data-uk-modal>
  <div class="uk-modal-dialog uk-modal-body uk-margin-auto-vertical">
    <button
      class="uk-modal-close absolute right-4 top-4"
      type="button"
      aria-label="Close"
      data-uk-close
    ></button>
    <h2 class="uk-modal-title">Are you absolutely sure?</h2>
    <div class="my-4 text-sm text-muted-foreground">
      This action cannot be undone. This will permanently delete your account
      and remove your data from our servers.
    </div>
    <div class="flex justify-end">
      <button class="uk-modal-close uk-btn uk-btn-default mr-2" type="button">
        Cancel
      </button>
      <button class="uk-btn uk-btn-primary" type="button">Continue</button>
    </div>
  </div>
</div>
```

## Accessibility

The Close component automatically sets the appropriate WAI-ARIA roles and properties.

- The _close icon_ has the `aria-label` property, and if an `<a>` element is used, the `button` role.

### Internationalization

The Close component uses the following translation strings. Learn more about [translating components](https://franken-ui.dev/docs/2.1/accessibility).

| Key     | Default | Description             |
| ------- | ------- | ----------------------- |
| `label` | `Close` | `aria-label` attribute. |
