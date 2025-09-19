## Calendar

You can build your calendar manually using server-side rendering with the following classes, or use our web components that have been built from scratch with the `<uk-calendar>` markup.

### Manual server-side rendering

Use the following classes to create your calendar:

| Class            | Description                                                                     |
| ---------------- | ------------------------------------------------------------------------------- |
| `uk-cal`         | The calendar wrapper                                                            |
| `uk-cal-oom`     | For dates that are out-of-month                                                 |
| `uk-active`      | To show the active date                                                         |
| `uk-disabled`    | To disable a date (add `disabled` attribute to the button for full disablement) |
| `uk-cal-marked`  | To add an indicator for "marked dates" (dates with events)                      |
| `uk-cal-divider` | To add a divider between calendar weeks.                                        |

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <div class="uk-cal uk-cal-divider">
      <table>
        <thead>
          <tr>
            <th>Su</th>
            <th>Mo</th>
            <th>Tu</th>
            <th>We</th>
            <th>Th</th>
            <th>Fr</th>
            <th>Sa</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="uk-cal-oom">
              <button>28</button>
            </td>
            <td class="uk-cal-oom">
              <button>29</button>
            </td>
            <td class="uk-cal-oom">
              <button>30</button>
            </td>
            <td class="uk-cal-oom">
              <button>31</button>
            </td>
            <td class="uk-active">
              <button>1</button>
            </td>
            <td>
              <button>2</button>
            </td>
            <td class="uk-disabled">
              <button disabled>3</button>
            </td>
          </tr>
          <tr>
            <td>
              <button>4</button>
            </td>
            <td class="uk-cal-marked">
              <button>5</button>
            </td>
            <td>
              <button>6</button>
            </td>
            <td>
              <button>7</button>
            </td>
            <td>
              <button>8</button>
            </td>
            <td>
              <button>9</button>
            </td>
            <td>
              <button>10</button>
            </td>
          </tr>
          <tr>
            <td><button>11</button></td>
            <td><button>12</button></td>
            <td><button>13</button></td>
            <td><button>14</button></td>
            <td><button>15</button></td>
            <td><button>16</button></td>
            <td><button>17</button></td>
          </tr>
          <tr>
            <td><button>18</button></td>
            <td><button>19</button></td>
            <td><button>20</button></td>
            <td><button>21</button></td>
            <td><button>22</button></td>
            <td><button>23</button></td>
            <td><button>24</button></td>
          </tr>
          <tr>
            <td><button>25</button></td>
            <td><button>26</button></td>
            <td><button>27</button></td>
            <td><button>28</button></td>
            <td><button>29</button></td>
            <td><button>30</button></td>
            <td><button>31</button></td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</div>
```

### Web components

Alternatively, you can use our web components with the `<uk-calendar>` markup.

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar></uk-calendar>
  </div>
</div>
```

## Setting the current day

To automatically set today's date as the active date in the calendar, use the `today` attribute. This will highlight the current day in the calendar, making it easy for users to quickly identify the current date.

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar today></uk-calendar>
  </div>
</div>
```

By default, this attribute is set to `false`, meaning today's date will not be automatically highlighted.

## Enabling month and year selection

To allow month and year selection, use the `jumpable` attribute. This will enable a dropdown menu for selecting the month and a text input field for entering the year, allowing users to quickly "jump" to a specific date.

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar jumpable></uk-calendar>
  </div>
</div>
```

By default, this attribute is set to `false`, meaning the calendar will not provide month and year selection options.

## Setting the starting day of the week

To customize the starting day of the week in the calendar, use the `starts-with` attribute. This allows you to specify whether the week should start on Sunday (0) or Monday (1). By default, the week starts on Sunday (0).

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar starts-with="1"></uk-calendar>
  </div>
</div>
```

## Disabling specific dates

To disable specific dates in the calendar, use the `disabled-dates` attribute. This attribute accepts a comma-separated list of dates. Please note that dates must be in the format `YYYY-MM-DD` (e.g. `2022-07-25`). Dates that do not follow this format will be ignored and a console error will be thrown. The calendar will still render, but the invalid dates will not be disabled.

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar
      disabled-dates="2022-07-25,2022-08-01,2022-08-15"
      view-date="2022-07-01"
    ></uk-calendar>
  </div>
</div>
```

## Marking specific dates

To add an indicator to specific dates in the calendar, use the `marked-dates` attribute. This attribute accepts a comma-separated list of dates. Please note that dates must be in the format `YYYY-MM-DD` (e.g. `2022-07-25`). Dates that do not follow this format will be ignored and a console error will be thrown. The calendar will still render, but the invalid dates will not be marked.

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar
      marked-dates="2022-07-25,2022-08-01,2022-08-15"
      view-date="2022-07-01"
    ></uk-calendar>
  </div>
</div>
```

## Setting the view date

To customize the initial view date of the calendar, use the `view-date` attribute. By default, the calendar will display the current date. To set a custom view date, provide a date in the format `YYYY-MM-DD` (e.g. `2023-06-30`). This will cause the calendar to display the specified month and year.

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar view-date="2023-06-30"></uk-calendar>
  </div>
</div>
```

## Setting the minimum and maximum date

To set the minimum and maximum date that can be selected in the calendar, use the `min` and `max` attributes. These attributes accept dates in the format `YYYY-MM-DD` (e.g. `2022-07-25`).

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar
      min="2022-01-01"
      max="2022-12-31"
      view-date="2022-07-01"
    ></uk-calendar>
  </div>
</div>
```

## Setting the current value

To set the current value of the calendar, use the `value` attribute. This attribute accepts a date in the format `YYYY-MM-DD` (e.g. `2020-05-06`). Please note that this attribute takes precedence over `view-date` and `today`, so setting `value` will override any settings made with those attributes.

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar value="2022-07-01"></uk-calendar>
  </div>
</div>
```

## Capturing values

There are several ways to capture values from the `<uk-calendar>` component. The simplest approach is to add a `name` attribute to the component. When you do this, a hidden input field with the specified name will be automatically generated, allowing you to easily capture the selected value on your server.

```html
<uk-calendar name="calendar"></uk-calendar>
```

This is useful when you need to include the calendar component in a form and capture the selected date as part of the form submission.

## Internationalization

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar
      i18n="weekdays: Sunnudagur, Mánadagur, Týsdagur, Mikudagur, Hósdagur, Fríggjadagur, Leygardagur; months: Januar, Februar, Mars, Apríl, Mai, Juni, Juli, August, September, Oktobur, November, Desember"
      value="2022-07-01"
      jumpable
    ></uk-calendar>
  </div>
</div>
```

## Available options

| Name       | Description                                                          |
| ---------- | -------------------------------------------------------------------- |
| `weekdays` | A comma-separated list of days of the week, starting from Sunday.    |
| `months`   | A comma-separated list of months of the year, starting from January. |

## Custom classes

To add custom classes, use the `cls-custom` attribute. This attribute accepts two formats:

- A JSON-stringified object
- A valid `key: value; foo: bar;` format

If you pass only class names, they will be applied directly to the calendar component.

### Example

```html
<div class="flex justify-center">
  <div class="uk-rounded uk-shadow border border-border p-3">
    <uk-calendar
      cls-custom="uk-cal-divider"
      disabled-dates="2022-07-25,2022-08-01,2022-08-15"
      view-date="2022-07-01"
    ></uk-calendar>
  </div>
</div>
```

## Attributes

The following attributes are available for this component:

| Name                     | Type    | Default    | Description                                                                                                   |
| ------------------------ | ------- | ---------- | ------------------------------------------------------------------------------------------------------------- |
| `force-prevent-rerender` | Boolean | false      | Forcefully prevents component rerendering.                                                                    |
| `weekday-abbr-length`    | String  | 3          | Customize the length of weekday abbreviations (e.g., Monday → Mon).                                           |
| `today`                  | Boolean | false      | Automatically sets today as the active date.                                                                  |
| `jumpable`               | Boolean | false      | Allows user to select a month and type a year for the calendar to "jump" to a specific date.                  |
| `starts-with`            | String  | 0 (Sunday) | Sets the starting day of the week. Either "0" (Sunday) or "1" (Monday).                                       |
| `disabled-dates`         | String  |            | A comma-separated list of dates to disable. Dates must be in the format YYYY-MM-DD.                           |
| `marked-dates`           | String  |            | A comma-separated list of dates to add an indicator. Dates must be in the format YYYY-MM-DD.                  |
| `view-date`              | String  |            | Sets the initial view date of the calendar. Dates must be in the format YYYY-MM-DD.                           |
| `min`                    | String  |            | Sets the minimum date that can be selected. Dates must be in the format YYYY-MM-DD.                           |
| `max`                    | String  |            | Sets the maximum date that can be selected. Dates must be in the format YYYY-MM-DD.                           |
| `value`                  | String  |            | Sets the current value of the calendar. Dates must be in the format YYYY-MM-DD.                               |
| `name`                   | String  |            | Sets the name of the hidden input field, allowing the calendar's value to be submitted with a form.           |
| `cls-custom`             | String  |            | Allows you to add custom CSS classes.                                                                         |
| `i18n`                   | String  |            | Enables internationalization. Please see [Internationalization](#internationalization) for available options. |

## Events

The Calendar component triggers the following events on elements with this component attached:

| Name                 | Description                         |
| -------------------- | ----------------------------------- |
| `uk-calendar:change` | Fired when active date has changed. |
