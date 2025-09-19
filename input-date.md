## Input date

The Input Date component is a web component built from scratch to allow users to easily select date and time. To get started, simply use the `<uk-input-date>` markup in your HTML code.

### Example

```html
<div class="h-10">
  <uk-input-date cls-custom="uk-input-fake"></uk-input-date>
</div>
```

## Styling

The `<uk-input-date>` component is intentionally unstyled by default, allowing you to easily customize its appearance to fit your needs.

To add custom styles, use the `cls-custom` attribute. This attribute accepts two formats:

- A JSON-stringified object
- A valid `key: value; foo: bar;` format

If you pass only class names, they will be applied directly to the button inside the component.

### Example

```html
<!-- Unstyled -->
<div class="h-10">
  <uk-input-date></uk-input-date>
</div>

<!-- Custom -->
<div class="h-10">
  <uk-input-date
    cls-custom="button: bg-lime-500 text-lime-50 w-full flex justify-between; icon: bg-orange-500 text-orange-50; dropdown: bg-purple-500 text-purple-50; calendar: bg-cyan-900 text-cyan-50; time: bg-emerald-500 text-emerald-900"
    icon="calendar"
    with-time
  >
  </uk-input-date>
</div>
```

## Capturing values

There are several ways to capture values from the `<uk-input-date>` component. The simplest approach is to add a `name` attribute to the component. When you do this, a hidden input field with the specified name will be automatically generated, allowing you to easily capture the selected value on your server.

```html
<uk-input-date name="date"></uk-input-date>
```

## Prepopulating values

To prepopulate the Input Date component with an existing value, simply pass the `value` attribute with a `YYYY-MM-DD` or `YYYY-MM-DDTHH:MM` format. To prepopulate with current date and time, just use the `today` attribute and it will automatically set the current date and time as the default value.

```html
<uk-input-date today></uk-input-date>
```

### Example

```html
<div class="h-10">
  <uk-input-date
    cls-custom="uk-input-fake"
    value="2023-06-30T20:00"
    with-time
  ></uk-input-date>
</div>

<div class="mt-4 h-10">
  <uk-input-date cls-custom="uk-input-fake" today with-time></uk-input-date>
</div>
```

## Customize display format

To customize the display format, you can use the following parsing tokens and pass them to the `display-format` attribute.

| Input |     Example      |            Description            |
| :---: | :--------------: | :-------------------------------: |
|  YY   |        01        |          Two-digit year           |
| YYYY  |       2001       |          Four-digit year          |
|   M   |       1-12       |       Month, beginning at 1       |
|  MM   |      01-12       |          Month, 2-digits          |
|  MMM  |     Jan-Dec      |    The abbreviated month name     |
| MMMM  | January-December |        The full month name        |
|  ddd  |    Mon - Sun     |   The abbreviated weekday name    |
| DDDD  | Monday - Sunday  |       The full weekday name       |
|   D   |       1-31       |           Day of month            |
|  DD   |      01-31       |      Day of month, 2-digits       |
|   H   |       0-23       |               Hours               |
|  HH   |      00-23       |          Hours, 2-digits          |
|   h   |       1-12       |       Hours, 12-hour clock        |
|  hh   |      01-12       |  Hours, 12-hour clock, 2-digits   |
|   m   |       0-59       |              Minutes              |
|  mm   |      00-59       |         Minutes, 2-digits         |
|   A   |      AM PM       | Post or ante meridiem, upper-case |
|   a   |      am pm       | Post or ante meridiem, lower-case |
|  Do   |    1st - 31st    |     Day of Month with ordinal     |

```html
<uk-input-date display-format="YYYY/MM/DD"></uk-input-date>
```

## Position

Because the `<uk-input-date>` component uses the [Drop](https://franken-ui.dev/docs/2.1/drop) component under the hood, we can leverage its positioning capabilities and position our dropdown anywhere we want. To position it, just use the `drop` attribute with your drop options.

### Example

```html
<div class="h-10">
  <uk-input-date
    cls-custom="uk-btn uk-btn-default"
    drop="mode: click; pos: right-center"
  >
  </uk-input-date>
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
<div class="h-7">
  <uk-input-date cls-custom="uk-input-fake uk-form-xs"></uk-input-date>
</div>

<div class="mt-4 h-8">
  <uk-input-date cls-custom="uk-input-fake uk-form-sm"></uk-input-date>
</div>

<div class="mt-4 h-12">
  <uk-input-date cls-custom="uk-input-fake uk-form-md"></uk-input-date>
</div>

<div class="mt-4 h-14">
  <uk-input-date cls-custom="uk-input-fake uk-form-lg"></uk-input-date>
</div>
```

## Disable input

To prevent user input, add the `disabled` attribute to the `<uk-input-date>` element. This will disable the component, making it impossible for users to enter or modify its value.

### Example

```html
<div class="mt-4 h-10">
  <uk-input-date cls-custom="uk-input-fake" disabled></uk-input-date>
</div>
```

## Error state

To indicate an error state in the form, simply add the `.uk-form-destructive` class to the `cls-custom` attribute. This will apply a "destructive" state to the component, providing visual feedback to the user.

### Example

```html
<div class="space-y-2">
  <label class="uk-form-label text-destructive">Date</label>
  <div class="uk-form-controls">
    <uk-input-date
      cls-custom="uk-input-fake uk-form-destructive"
    ></uk-input-date>
  </div>
  <p class="uk-form-help text-destructive">This field is required.</p>
</div>
```

## Preventing layout shift

When loading Web Components, there may be a brief delay before the content is fully rendered. This can result in a flash of unstyled content or unprocessed templates. To mitigate this issue, consider setting a predefined height on the parent element to prevent layout shift and ensure a smooth user experience.

```html
<div class="h-10">
  <uk-input-date>...</uk-input-date>
</div>
```

## Internationalization

Because this component uses [Calendar](https://franken-ui.dev/docs/2.1/calendar#internationalization) and [Input Time](https://franken-ui.dev/docs/2.1/input-time#internationalization) under the hood, you can use and merge their `i18n` attributes. Please refer to their documentation for available options.

## Attributes

The following attributes are available for this component:

| Name                     | Type    | Default    | Description                                                                                                               |
| ------------------------ | ------- | ---------- | ------------------------------------------------------------------------------------------------------------------------- |
| `force-prevent-rerender` | Boolean | false      | Forcefully prevents component rerendering.                                                                                |
| `weekday-abbr-length`    | String  | 3          | Customize the length of weekday abbreviations (e.g., Monday → Mon).                                                       |
| `today`                  | Boolean | false      | Automatically sets today as the active date.                                                                              |
| `jumpable`               | Boolean | false      | Allows user to select a month and type a year for the calendar to "jump" to a specific date.                              |
| `starts-with`            | String  | 0 (Sunday) | Sets the starting day of the week. Either "0" (Sunday) or "1" (Monday).                                                   |
| `disabled-dates`         | String  |            | A comma-separated list of dates to disable. Dates must be in the format YYYY-MM-DD.                                       |
| `marked-dates`           | String  |            | A comma-separated list of dates to add an indicator. Dates must be in the format YYYY-MM-DD.                              |
| `view-date`              | String  |            | Sets the initial view date of the calendar. Dates must be in the format YYYY-MM-DD.                                       |
| `min`                    | String  |            | Sets the minimum date that can be selected. Date must be in the format YYYY-MM-DD.                                        |
| `max`                    | String  |            | Sets the maximum date that can be selected. Date must be in the format YYYY-MM-DD.                                        |
| `cls-custom`             | String  |            | Allows you to add custom CSS classes.                                                                                     |
| `disabled`               | Boolean | false      | Disables all input fields, making the entire component read-only.                                                         |
| `name`                   | String  |            | Defines the name of the input, allowing you to capture its value on your server.                                          |
| `value`                  | String  |            | A valid date time in `YYYY-MM-DD` or `YYYY-MM-DDTHH:MM` format that will be prepopulated in the input field.              |
| `i18n`                   | String  |            | Enables internationalization. Please see [Internationalization](#internationalization) for available options.             |
| `icon`                   | String  |            | Sets a customized icon. If no icon is passed, it will default to a calendar icon.                                         |
| `drop`                   | String  |            | Customize the dropping option for the dropdown. See [Drop](https://franken-ui.dev/docs/2.1/drop) component for more options.                    |
| `with-time`              | Boolean | false      | Allows inputting of time.                                                                                                 |
| `require-time`           | Boolean | false      | Requires time input. If user leaves it blank, it will prepopulate the current time.                                       |
| `display-format`         | String  |            | Customize the display format of the date. See [Customize display format](#customize-display-format) for available tokens. |

## Events

The Input Date component triggers the following events on elements with this component attached:

| Name                  | Description                                                                           |
| --------------------- | ------------------------------------------------------------------------------------- |
| `uk-input-date:input` | Fired after the value has changed, providing an opportunity to respond to user input. |
