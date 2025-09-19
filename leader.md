## Leader

A leader, also known as a dot leader or a tab leader, is a repeating pattern used to visually connect content across horizontal spaces. It is most commonly used for restaurant menus, between the meals and prices, and for tables of contents, between titles and page numbers.

To apply this component, add the `data-uk-leader` attribute to the element on the left. A line of characters, by default dots, will then fill the remaining space between the item and its adjacent element.

```html
<div data-uk-leader></div>
```

### Example

```html
<div class="flex gap-x-2">
  <div class="flex-1" data-uk-leader>Lorem ipsum dolor sit amet</div>
  <div>$20.90</div>
</div>
```

## Fill character

To change the dot to any custom character, just add the `fill: STRING` option to the attribute.

```html
<div data-uk-leader="fill: -"></div>
```

### Example

```html
<div class="flex gap-x-2">
  <div class="flex-1" data-uk-leader="fill: -">Lorem ipsum dolor sit amet</div>
  <div>$20.90</div>
</div>
```

Note: The default fill character can be set through CSS variable.

```css
.uk-leader-fill-content::before {
  content: ".";
}

:root {
  --uk-leader-fill-content: ".";
}
```

## Responsive

It's possible to disable the leader for different device widths by applying the `media` option to the attribute and adding the appropriate viewport width. Add a number in pixels, for example `media: 640`, or a breakpoint, for example `media: @m`. The leader will be shown from the specified viewport width and upwards, but not below.

```html
<div data-uk-leader="media: @m"></div>
```

## Component options

Any of these options can be applied to the component attribute. Separate multiple options with a semicolon. [Learn more](https://franken-ui.dev/docs/2.1/javascript#component-configuration)

| Option  | Value                   | Default | Description                                                                                                                                                |
| ------- | ----------------------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `fill`  | String                  |         | Optional fill character.                                                                                                                                   |
| `media` | Boolean, Number, String | `false` | Condition for the space filling - a width as integer (e.g. 640) or a breakpoint (e.g. @s, @m, @l, @xl) or any valid media query (e.g. (min-width: 900px)). |

## JavaScript

Learn more about [JavaScript components](https://franken-ui.dev/docs/2.1/javascript#programmatic-use).

### Initialization

```javascript
UIkit.leader(element, options);
```
