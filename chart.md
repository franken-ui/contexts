## Chart

Under the hood, Franken UI uses [ApexCharts](https://apexcharts.com). Franken UI provides a thin layer of compatibility and serves as a glue between ApexCharts and shadcn/ui so you don't have to configure anything by yourself.

## JavaScript

There are several ways to use Chart—whether through CDN, Tailwind CSS v3, or Vite plugin—but in most cases, it's already included in as a first-party extension, so you don't need to install anything separately. Just choose the setup that fits your project best.

### Option 1: Using CDN

To include the Chart library via CDN, add the following to your HTML `<head>`:

```html
<script
  src="https://cdn.jsdelivr.net/npm/franken-ui@latest/dist/js/chart.iife.js"
  type="module"
></script>
```

For stability in production, it's recommended that you hardcode the latest version in the CDN link.
      

This method is the quickest way to get started, especially for prototypes or demos.

### Option 2: Using NPM

If you're building a modern app with a bundler, you can import the JavaScript file from `franken-ui` into your `app.js` file.

```javascript
import "franken-ui/js/chart.iife";
```

## CSS

Starting with version `2.1`, core styling has been removed from the default build. Styling is now handled through our first-party extension. If you're using the CDN version, no additional setup is needed—styles are already bundled.

### Tailwind CSS plugin

If you are using the Tailwind CSS plugin, edit your `tailwind.config.js` file.

```js
import franken from "franken-ui/shadcn-ui/preset-quick";
import chart from "franken-ui/extensions/chart";

/** @type {import('tailwindcss').Config} */
export default {
  presets: [
    franken({
      extensions: [
        [chart, {}],
      ],
    }),
  ],
};
```

### Vite plugin

If you are using the Vite plugin, edit your `vite.config.js` file.

```js
import { defineConfig } from "vite";
import franken from "franken-ui/plugin-vite";

export default defineConfig({
  plugins: [
    franken({
      preflight: false,
      layer: true,
      layerExceptions: ["chart"],
    }),
  ],
});
```

Once everything is configured, you may now use the `<uk-chart>` markup in your HTML code with one `<script type="application/json"></script>` tag as options reference.

## Reactivity

By default, the `<uk-chart>` component is not reactive. This is a deliberate design choice, as using [MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver) can be computationally expensive. As a result, changes to the referenced `<script type="application/json">` tag will not trigger an update.

To enable reactivity, simply add the `reactive` attribute to the `<uk-chart>` component. This will use [MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver) under the hood to monitor the `<script>` tag for changes.

```html
<uk-chart reactive>
  <!-- ... -->
</uk-chart>
```

## Attributes

| Name                     | Type    | Default | Description                                                                                                                                                |
| ------------------------ | ------- | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `force-prevent-rerender` | Boolean | false   | Forcefully prevents component rerendering.                                                                                                                 |
| `cls-custom`             | String  |         | Allows you to add custom CSS classes, which will be attached to the `<div>` tag.                                                                           |
| `reactive`               | Boolean | false   | Enables reactivity by using `MutationObserver` to monitor the referenced `<script>` element for changes, triggering updates to the `<uk-chart>` component. |
