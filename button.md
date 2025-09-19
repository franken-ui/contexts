## Button

To apply this component, add the `.uk-btn` class and a modifier such as `.uk-btn-default` to an `<a>` or `<button>` element. Add the `disabled` attribute to a `<button>` element to disable the button.

```html
<a class="uk-btn uk-btn-default" href=""></a>

<button class="uk-btn uk-btn-default"></button>

<button class="uk-btn uk-btn-default" disabled></button>
```

### Example

```html
<div class="flex flex-wrap gap-2">
  <a class="uk-btn uk-btn-default" href="#">Link</a>
  <button class="uk-btn uk-btn-default">Button</button>
  <button class="uk-btn uk-btn-default" disabled>Disabled</button>
</div>
```

## Style modifiers

There are several style modifiers available. Just add one of the following classes to apply a different look.

| Class                 | Description                               |
| --------------------- | ----------------------------------------- |
| `.uk-btn-default`     | Default button style.                     |
| `.uk-btn-ghost`       | Applies a ghost style.                    |
| `.uk-btn-primary`     | Indicates the primary action.             |
| `.uk-btn-secondary`   | Indicates an important action.            |
| `.uk-btn-destructive` | Indicates a dangerous or negative action. |
| `.uk-btn-text`        | Applies an typographic style.             |
| `.uk-btn-link`        | Applies an plain link style.              |

```html
<button class="uk-btn uk-btn-primary"></button>
```

### Example

```html
<div class="flex flex-wrap items-center gap-2">
  <button class="uk-btn uk-btn-default">Default</button>
  <button class="uk-btn uk-btn-ghost">Ghost</button>
  <button class="uk-btn uk-btn-primary">Primary</button>
  <button class="uk-btn uk-btn-secondary">Secondary</button>
  <button class="uk-btn uk-btn-destructive">Destructive</button>
  <button class="uk-btn uk-btn-text">Text</button>
</div>
```

## Size modifiers

There are several size modifiers available. Just add one of the following classes to make the button smaller or larger.

| Class        | Description               |
| ------------ | ------------------------- |
| `.uk-btn-xs` | Applies extra small size. |
| `.uk-btn-sm` | Applies small size.       |
| `.uk-btn-md` | Applies medium size.      |
| `.uk-btn-lg` | Applies large size.       |

### Example

```html
<div class="flex flex-wrap gap-2">
  <button class="uk-btn uk-btn-default uk-btn-xs">xs</button>
  <button class="uk-btn uk-btn-primary uk-btn-xs">xs</button>
  <button class="uk-btn uk-btn-secondary uk-btn-xs">xs</button>
</div>

<div class="mt-4 flex flex-wrap gap-2">
  <button class="uk-btn uk-btn-default uk-btn-sm">sm</button>
  <button class="uk-btn uk-btn-primary uk-btn-sm">sm</button>
  <button class="uk-btn uk-btn-secondary uk-btn-sm">sm</button>
</div>

<div class="mt-4 flex flex-wrap gap-2">
  <button class="uk-btn uk-btn-default uk-btn-md">md</button>
  <button class="uk-btn uk-btn-primary uk-btn-md">md</button>
  <button class="uk-btn uk-btn-secondary uk-btn-md">md</button>
</div>

<div class="mt-4 flex flex-wrap gap-2">
  <button class="uk-btn uk-btn-default uk-btn-lg">lg</button>
  <button class="uk-btn uk-btn-primary uk-btn-lg">lg</button>
  <button class="uk-btn uk-btn-secondary uk-btn-lg">lg</button>
</div>
```

## Width modifiers

You can use Tailwind CSS utility classes alongside button classes and the it will follow its width.

### Example

```html
<div class="flex flex-col gap-2">
  <button class="uk-btn uk-btn-default w-40">w-40</button>
  <button class="uk-btn uk-btn-primary w-44">w-44</button>
  <button class="uk-btn uk-btn-secondary w-48">w-48</button>
  <button class="uk-btn uk-btn-ghost w-52">w-52</button>
  <button class="uk-btn uk-btn-destructive w-full">w-full</button>
</div>
```

## Icon

Use `.uk-btn-icon` class to create an icon button, which can be used for social icons or toolbars.

### Example

```html
<div class="flex gap-x-2">
  <button class="uk-btn uk-btn-default uk-btn-icon">
    <uk-icon icon="copy"></uk-icon>
  </button>
  <button class="uk-btn uk-btn-default uk-btn-icon">
    <uk-icon icon="file"></uk-icon>
  </button>
  <button class="uk-btn uk-btn-default uk-btn-icon">
    <uk-icon icon="trash"></uk-icon>
  </button>
</div>
```

## Group

To create a button group, add the `.uk-btn-group` class to a `<div>` element around the buttons. That's it! No further markup is needed.

### Example

```html
<div>
  <div class="uk-btn-group">
    <button class="uk-btn uk-btn-secondary">Button</button>
    <button class="uk-btn uk-btn-secondary">Button</button>
    <button class="uk-btn uk-btn-secondary">Button</button>
  </div>
</div>

<div class="mt-4">
  <div class="uk-btn-group">
    <button class="uk-btn uk-btn-primary">Button</button>
    <button class="uk-btn uk-btn-primary">Button</button>
    <button class="uk-btn uk-btn-primary">Button</button>
  </div>
</div>

<div class="mt-4">
  <div class="uk-btn-group">
    <button class="uk-btn uk-btn-destructive">Button</button>
    <button class="uk-btn uk-btn-destructive">Button</button>
    <button class="uk-btn uk-btn-destructive">Button</button>
  </div>
</div>
```

## Button with dropdowns

A button can be used to trigger a dropdown menu from the [Dropdown component](https://franken-ui.dev/docs/2.1/dropdown).

```html
<!-- A button toggling a dropdown -->
<button class="uk-btn uk-btn-default" type="button"></button>
<div data-uk-dropdown></div>
```

### Example

```html
<div class="uk-inline">
  <button class="uk-btn uk-btn-default" type="button">Dropdown</button>
  <div
    class="uk-drop uk-dropdown min-w-52"
    data-uk-dropdown="animation: uk-anmt-slide-top-sm"
  >
    <ul class="uk-nav uk-dropdown-nav">
      <li class="uk-active"><a href="#">Active</a></li>
      <li><a href="#">Item</a></li>
      <li class="uk-nav-header">Header</li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li class="uk-nav-divider"></li>
      <li><a href="#">Item</a></li>
    </ul>
  </div>
</div>
```
