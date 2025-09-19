## Input range

Input Range is a web component built from scratch to enable users to easily integrate customizable range sliders. With built-in support for keyboard navigation, ARIA attributes for accessibility, and a minimalist design.

To get started, simply use the `<uk-input-range>` markup in your HTML code.

### Example

```html
<div class="h-10">
  <uk-input-range></uk-input-range>
</div>
```

## Dual range

To enable dual range functionality (allowing you to select a range with both a minimum and maximum value), simply add the `multiple` attribute to your `<uk-input-range>` element. When this attribute is present, the component renders two knobs: one for the minimum value and one for the maximum value.

### Example

```html
<div class="h-10">
  <uk-input-range multiple></uk-input-range>
</div>
```

## Capturing values

There are several ways to capture values from the `<uk-input-range>` component. The simplest approach is to add a `name` attribute to the component. When you do this, a hidden input field with the specified name will be automatically generated, allowing you to easily capture the selected value on your server.

Note: When using the dual knob mode by including the `multiple` attribute, the component renders two hidden input fields—one for the lower value and one for the upper value. In this case, the name attribute is automatically appended with `[]` (e.g., `name="range[]"`) to indicate an array of values. This makes it straightforward to process both values on the server side.

```html
<uk-input-range name="range"></uk-input-range>
```

## Prepopulating values

Prepopulating the Input Range component is straightforward. Simply pass a value (or values) via the `value` attribute when declaring the component in your HTML. This is particularly useful when you need to display existing data that users can adjust or confirm.

Note: When using the dual knob mode, supply two values separated by a comma. The first value sets the lower bound, and the second value sets the upper bound.

### Example

```html
<div class="h-10">
  <uk-input-range value="75"></uk-input-range>
</div>

<div class="mt-4 h-10">
  <uk-input-range multiple value="20,80"></uk-input-range>
</div>
```

## Labeling

The `label` attribute allows you to display a label on each knob of the slider. This label can be used to show the current numeric value, or a custom text concatenated with the value.

### Example

```html
<div class="px-8">
  <div class="mt-10">
    <uk-input-range label></uk-input-range>
  </div>

  <div class="mt-10">
    <uk-input-range label="kg"></uk-input-range>
  </div>
</div>
```

Note: If you simply include the label attribute (or set it to true), the slider will display only the numeric value. Otherwise, label will be concatenated.

### Position

In addition to the `label`, you can control its position relative to the knob using the `label-position` attribute. This attribute accepts two values:

- `top` (default): The label appears above the knob.
- `bottom`: The label appears below the knob.

### Example

```html
<div class="px-8">
  <div class="mt-10">
    <uk-input-range label="kg"></uk-input-range>
  </div>

  <div class="mt-10">
    <uk-input-range label="kg" label-position="bottom"></uk-input-range>
  </div>
</div>
```

## Min and max

The `min` and `max` attributes define the range boundaries of the slider. They determine the lowest and highest possible values that can be selected.

### Example

```html
<div class="px-8">
  <div class="mt-10">
    <uk-input-range min="50" max="75" label></uk-input-range>
  </div>
</div>
```

## Step

The step attribute determines the interval at which the slider's value increments or decrements. This attribute mimics the behavior of the native HTML `<input type="range">`, ensuring that as you drag or use keyboard navigation, the value snaps to defined increments. For example, if the step is set to `0.5`, the slider will move in increments of `0.5` units, such as `0.0`, `0.5`, `1.0`, etc.

### Example

```html
<div class="px-8">
  <div class="mt-10">
    <uk-input-range label step="0.5"></uk-input-range>
  </div>

  <div class="mt-10">
    <uk-input-range label multiple step="0.5"></uk-input-range>
  </div>
</div>
```

## Disable input

To prevent user input, add the `disabled` attribute to the `<uk-input-range>` element. This will disable the component, making it impossible for users to enter or modify value.

### Example

```html
<div class="h-10">
  <uk-input-range disabled value="50"></uk-input-range>
</div>
```

## Attributes

The following attributes are available for this component:

| Name                     | Type            | Default | Description                                                                           |
| ------------------------ | --------------- | ------- | ------------------------------------------------------------------------------------- |
| `force-prevent-rerender` | Boolean         | false   | Forcefully prevents component rerendering.                                            |
| `name`                   | String          | `null`  | Specifies the name of the hidden input field for form submissions.                    |
| `disabled`               | Boolean         | `false` | Disables the slider, preventing user interaction.                                     |
| `multiple`               | Boolean         | `false` | Enables dual-knob mode for selecting a range of values.                               |
| `min`                    | String          | `0`     | Defines the minimum selectable value.                                                 |
| `max`                    | String          | `100`   | Defines the maximum selectable value.                                                 |
| `step`                   | String          | `1`     | Specifies the interval between selectable values.                                     |
| `label`                  | Boolean, String | `false` | Displays a value label above the knob (`true` for numbers, string for custom labels). |
| `label-position`         | String          | `top`   | Sets the position of the label relative to the knob.                                  |
| `value`                  | String          | `null`  | Defines the initial value (`"50.00"` for single, `"20.00,80.00"` for dual).           |

## Events

The Input Range component triggers the following events on elements with this component attached:

| Name                   | Description                                                                           |
| ---------------------- | ------------------------------------------------------------------------------------- |
| `uk-input-range:input` | Fired after the value has changed, providing an opportunity to respond to user input. |
