## Input time

The Input Time component is a web component built from scratch to allow users to easily select time in a 12-hour format, while outputting the selected time in a 24-hour format. To get started, simply use the `<uk-input-time>` markup in your HTML code.

### Example

```html
<div class="h-10">
  <uk-input-time></uk-input-time>
</div>
```

## Capturing values

There are several ways to capture values from the `<uk-input-time>` component. The simplest approach is to add a `name` attribute to the component. When you do this, a hidden input field with the specified name will be automatically generated, allowing you to easily capture the selected value on your server.

```html
<uk-input-time name="time"></uk-input-time>
```

## Prepopulating values

To prepopulate the Input Time component with an existing value, simply pass the `value` attribute with a 24-hour time format. To prepopulate with current time, just use the `now` attribute and it will automatically set the current time as the default value.

```html
<uk-input-time now></uk-input-time>
```

### Example

```html
<div class="h-10">
  <uk-input-time value="20:00"></uk-input-time>
</div>

<div class="mt-4 h-10">
  <uk-input-time now></uk-input-time>
</div>
```

## Size modifiers

There are several size modifiers available. Just add one of the following classes to the `cls-custom` attribute to make the input smaller or larger.

| Class         | Description               |
| ------------- | ------------------------- |
| `.uk-form-xs` | Applies extra small size. |
| `.uk-form-sm` | Applies small size.       |
| `.uk-form-md` | Applies medium size.      |
| `.uk-form-lg` | Applies large size.       |

### Example

```html
<div class="mt-4 h-7">
  <uk-input-time cls-custom="uk-form-xs"></uk-input-time>
</div>

<div class="mt-4 h-8">
  <uk-input-time cls-custom="uk-form-sm"></uk-input-time>
</div>

<div class="mt-4 h-12">
  <uk-input-time cls-custom="uk-form-md"></uk-input-time>
</div>

<div class="mt-4 h-14">
  <uk-input-time cls-custom="uk-form-lg"></uk-input-time>
</div>
```

## Disable input

To prevent user input, add the `disabled` attribute to the `<uk-input-time>` element. This will disable all input fields, making it impossible for users to enter or modify time.

### Example

```html
<div class="h-10">
  <uk-input-time disabled></uk-input-time>
</div>
```

## Error state

To indicate an error state in the form, simply add the `.uk-form-destructive` class to the `cls-custom` attribute. This will apply a "destructive" state to the component, providing visual feedback to the user.

### Example

```html
<div class="space-y-2">
  <label class="uk-form-label text-destructive">Time</label>
  <div class="uk-form-controls">
    <uk-input-time cls-custom="uk-form-destructive"></uk-input-time>
  </div>
  <p class="uk-form-help text-destructive">This field is required.</p>
</div>
```

## Preventing layout shift

When loading Web Components, there may be a brief delay before the content is fully rendered. This can result in a flash of unstyled content or unprocessed templates. To mitigate this issue, consider setting a predefined height on the parent element to prevent layout shift and ensure a smooth user experience.

```html
<div class="h-10">
  <uk-input-time>...</uk-input-time>
</div>
```

## Internationalization

### Example

```html
<div class="h-10">
  <uk-input-time value="20:00" i18n="am: FM; pm: EM"></uk-input-time>
</div>
```

## Available options

| Name | Description              |
| ---- | ------------------------ |
| `am` | Lets you customize "am". |
| `pm` | Lets you customize "pm". |

## Attributes

The following attributes are available for this component:

| Name                     | Type    | Default | Description                                                                      |
| ------------------------ | ------- | ------- | -------------------------------------------------------------------------------- |
| `force-prevent-rerender` | Boolean | false   | Forcefully prevents component rerendering.                                       |
| `autofocus`              | Boolean | false   | Automatically focuses on the first input field when the component is rendered.   |
| `cls-custom`             | String  |         | Allows you to add custom CSS classes.                                            |
| `disabled`               | Boolean | false   | Disables all input fields, making the entire component read-only.                |
| `name`                   | String  |         | Defines the name of the input, allowing you to capture its value on your server. |
| `now`                    | Boolean | false   | Automatically set the current time as the default value.                         |
| `value`                  | String  |         | A time in 24-hour format that will be prepopulated in the input field.           |

## Events

The Input Time component triggers the following events on elements with this component attached:

| Name                  | Description                                                                           |
| --------------------- | ------------------------------------------------------------------------------------- |
| `uk-input-time:input` | Fired after the value has changed, providing an opportunity to respond to user input. |
