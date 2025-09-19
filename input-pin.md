## Input pin

The Input PIN component is a web component built from scratch to allow users to input a sequence of one-character alphanumeric inputs. This is particularly useful in scenarios such as:

- Entering a verification code sent via SMS or email
- Authenticating with a two-factor authentication system
- Creating a secure password or passphrase

To get started, simply use the `<uk-input-pin>` markup in your HTML code.

### Example

```html
<uk-input-pin></uk-input-pin>
```

## Capturing values

There are several ways to capture values from the `<uk-input-pin>` component. The simplest approach is to add a `name` attribute to the component. When you do this, a hidden input field with the specified name will be automatically generated, allowing you to easily capture the selected value on your server.

```html
<uk-input-pin name="pin"></uk-input-pin>
```

## Customize length

By default, the Input PIN component is set to accept 6 characters. However, you can easily customize this by adding the `length` attribute to the `<uk-input-pin>` element. Simply specify the desired length as a numerical value, and the component will automatically adjust to accommodate the specified number of inputs.

### Example

```html
<uk-input-pin length="4"></uk-input-pin>
```

## Separated input

By default, the input fields in the Input PIN component are displayed adjacent to each other. To add visual separation between each input, simply add the `.uk-input-pin-separated` class to the `cls-custom` attribute. This will add gaps between each input, making it easier for users to distinguish between individual characters.

### Example

```html
<uk-input-pin cls-custom="uk-input-pin-separated"></uk-input-pin>
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
<div class="h-7">
  <uk-input-pin cls-custom="uk-form-xs"></uk-input-pin>
</div>

<div class="mt-4 h-8">
  <uk-input-pin cls-custom="uk-form-sm"></uk-input-pin>
</div>

<div class="mt-4 h-12">
  <uk-input-pin cls-custom="uk-form-md"></uk-input-pin>
</div>

<div class="mt-4 h-14">
  <uk-input-pin cls-custom="uk-form-lg"></uk-input-pin>
</div>
```

## Disable input

To prevent user input, add the `disabled` attribute to the `<uk-input-pin>` element. This will disable all input fields, making it impossible for users to enter or modify the PIN sequence.

### Example

```html
<uk-input-pin disabled></uk-input-pin>
```

## Error state

To indicate an error state in the form, simply add the `.uk-form-destructive` class to the `cls-custom` attribute. This will apply a "destructive" state to the component, providing visual feedback to the user.

### Example

```html
<div class="space-y-2">
  <label class="uk-form-label text-destructive">PIN</label>
  <div class="uk-form-controls">
    <uk-input-pin cls-custom="uk-form-destructive"></uk-input-pin>
  </div>
  <p class="uk-form-help text-destructive">This field is required.</p>
</div>
```

## Preventing layout shift

When loading Web Components, there may be a brief delay before the content is fully rendered. This can result in a flash of unstyled content or unprocessed templates. To mitigate this issue, consider setting a predefined height on the parent element to prevent layout shift and ensure a smooth user experience.

```html
<div class="h-10">
  <uk-input-pin>...</uk-input-pin>
</div>
```

## Attributes

The following attributes are available for this component:

| Name                     | Type    | Default | Description                                                                          |
| ------------------------ | ------- | ------- | ------------------------------------------------------------------------------------ |
| `force-prevent-rerender` | Boolean | false   | Forcefully prevents component rerendering.                                           |
| `autofocus`              | Boolean | false   | Automatically focuses on the first input field when the component is rendered.       |
| `cls-custom`             | String  |         | Allows you to add custom CSS classes.                                                |
| `disabled`               | Boolean | false   | Disables all input fields, making the entire component read-only.                    |
| `length`                 | String  | 6       | Specifies the number of input fields, determining the length of the PIN sequence.    |
| `name`                   | String  |         | Defines the name of the PIN input, allowing you to capture its value on your server. |

## Events

The Input PIN component triggers the following events on elements with this component attached:

| Name                 | Description                                                                           |
| -------------------- | ------------------------------------------------------------------------------------- |
| `uk-input-pin:input` | Fired after the value has changed, providing an opportunity to respond to user input. |
