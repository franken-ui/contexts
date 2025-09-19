## Installation

There are two ways to get started with Franken UI:

1. **CDN Installation** - Perfect for beginners and quick prototyping.
2. **NPM Installation** - Recommended for Tailwind CSS or Vite-based setups, there are two ways to install via NPM: as a Tailwind CSS plugin or as a Vite plugin.

## Via CDN

Perfect for beginners, the simplest installation can be done using CDN:

```html
<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/franken-ui@latest/dist/css/core.min.css"
/>
```

For stability in production, it's recommended that you hardcode the latest version in the CDN link. Once you're done, you may now proceed adding [JavaScript](https://franken-ui.dev/docs/2.1/javascript).

## Quickstart template

Use this quickstart template to get started with your project immediately.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>Franken UI</title>
    <link rel="preconnect" href="https://rsms.me/" />
    <link rel="stylesheet" href="https://rsms.me/inter/inter.css" />

    <style>
      :root {
        font-family: Inter, sans-serif;
        font-feature-settings: "liga" 1, "calt" 1;
      }
      @supports (font-variation-settings: normal) {
        :root {
          font-family: InterVariable, sans-serif;
        }
      }
    </style>

    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/franken-ui@next/dist/css/core.min.css"
    />
    <link
      rel="stylesheet"
      href="https://cdn.jsdelivr.net/npm/franken-ui@next/dist/css/utilities.min.css"
    />

    <script>
      const htmlElement = document.documentElement;

      const __FRANKEN__ = JSON.parse(
        localStorage.getItem("__FRANKEN__") || "{}"
      );

      if (
        __FRANKEN__.mode === "dark" ||
        (!__FRANKEN__.mode &&
          window.matchMedia("(prefers-color-scheme: dark)").matches)
      ) {
        htmlElement.classList.add("dark");
      } else {
        htmlElement.classList.remove("dark");
      }

      htmlElement.classList.add(__FRANKEN__.theme || "uk-theme-zinc");
      htmlElement.classList.add(__FRANKEN__.radii || "uk-radii-md");
      htmlElement.classList.add(__FRANKEN__.shadows || "uk-shadows-sm");
      htmlElement.classList.add(__FRANKEN__.font || "uk-font-sm");
      htmlElement.classList.add(__FRANKEN__.chart || "uk-chart-default");
    </script>

    <script
      type="module"
      src="https://cdn.jsdelivr.net/npm/franken-ui@next/dist/js/core.iife.js"
    ></script>
  </head>
  <body class="bg-background text-foreground">
    <!-- START CODING HERE -->

    <script
      type="module"
      src="https://cdn.jsdelivr.net/npm/franken-ui@next/dist/js/icon.iife.js"
    ></script>

    <!-- <script
      type="module"
      src="https://cdn.jsdelivr.net/npm/franken-ui@next/dist/js/chart.iife.js"
    ></script> -->
  </body>
</html>
```

## Via NPM (Tailwind CSS v3 Plugin)

Franken UI was initially designed as a Tailwind CSS plugin, which means it can be seamlessly integrated into any existing Tailwind CSS project. To get started, you first need to make sure that you have a [working Tailwind CSS project](https://v3.tailwindcss.com/docs/installation) installed and that you also have Node and NPM installed on your machine.

Start by installing PostCSS and the latest version of Franken UI using NPM:

```sh
npm install postcss franken-ui
```

Next, run the `npx franken-ui init -p` command.

```sh
npx franken-ui init -p
```

This command will automatically generate and configure both `tailwindcss.config.js` and `postcss.config.cjs` for you. If you already have a Tailwind CSS or PostCSS configuration in place, the command will refuse to create a new one. This ensures that your existing configuration isn't accidentally overwritten.

If you have trouble running the command, you can always refer to the [source code](https://github.com/franken-ui/ui/tree/master/src/lib/cli/init/stubs) and grab the right configuration you need.

Once you're done, you may now proceed adding [JavaScript](https://franken-ui.dev/docs/2.1/javascript).

## Via NPM (Vite Plugin)

First, install the latest version of Franken UI using NPM:

```sh
npm install franken-ui
```

Next, configure your `vite.config.js` file to use the Franken UI plugin.

```js
import franken from "franken-ui/plugin-vite";
import { defineConfig } from "vite";

export default defineConfig({
  plugins: [
    franken({
      preflight: true,
    }),
  ],
});
```

Once the plugin is configured, import the `franken-ui.css` file into your main CSS file:

```css
@import "franken-ui/css/franken-ui.css";
```

Alternatively, you can pull Franken UI CSS directly from the `node_modules` directory.

```html
<link rel="stylesheet" href="node_modules/franken-ui/dist/css/franken-ui.css" />
```

Note: Franken UI compiles CSS behind the scenes, so make sure to import the Vite plugin at the top of your vite.config.js file or second, right before any other CSS plugins, to avoid issues when importing it into your CSS file.

Once you're done, you may now proceed adding [JavaScript](https://franken-ui.dev/docs/2.1/javascript).
