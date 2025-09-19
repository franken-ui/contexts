## Icon

Place scalable vector icons anywhere in your content.

Under the hood, Franken UI use Lucide, a collection of open-source icons known for their beautiful and consistent design. With built-in options for size, stroke width, and other attributes, this component simplifies the process of incorporating iconography into your web applications.

## Usage

To use the icons in your project, simply add the `<uk-icon icon="icon_name">` component with the appropriate icon name to your HTML content. For example, to display the `a-arrow-down` icon, insert `<uk-icon icon="a-arrow-down"></uk-icon>` into your markup.

NOTE: Make sure to include the icon library script. For more details see the [installation instructions](https://franken-ui.dev/docs/2.1/javascript). Once that's done, you can now use the `<uk-icon icon="icon_name"></uk-icon>` tag anywhere in your HTML.

## Preventing layout shift

When loading Web Components, there may be a brief delay before the content is fully rendered. This can result in a flash of unstyled content or unprocessed templates. To mitigate this issue, consider setting a predefined height on the parent element to prevent layout shift and ensure a smooth user experience.

```html
<div class="size-4">
  <uk-icon icon="smile"></uk-icon>
</div>
```

## Attributes

| Name           | Type   | Default | Description                                                                      |
| -------------- | ------ | ------- | -------------------------------------------------------------------------------- |
| `cls-custom`   | String |         | Allows you to add custom CSS classes, which will be attached to the `<svg>` tag. |
| `icon`         | String |         | Specifies the icon you want to display.                                          |
| `stroke-width` | String | 2       | Customizes the stroke width of the icon.                                         |
| `height`       | String | 16      | Customizes the height of the icon.                                               |
| `width`        | String | 16      | Customizes the width of the icon.                                                |