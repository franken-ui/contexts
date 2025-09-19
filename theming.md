## Theming

Franken UI, just like shadcn/ui use a simple `background` and `foreground` convention for colors. The `background` variable is used for the background color of the component and the `foreground` variable is used for the text color.

The `background` suffix is omitted when the variable is used for the background color of the component.

Given the following CSS variables:

```css
--primary: 0 0% 9%;
--primary-foreground: 0 0% 98%;
```

The `background` color of the following component will be `hsl(var(--primary))` and the `foreground` color will be `hsl(var(--primary-foreground))`.

```html
<div class="bg-primary text-primary-foreground">Hello</div>
```

**CSS variables must be defined without color space function**. See the [Tailwind CSS documentation](https://v3.tailwindcss.com/docs/customizing-colors#using-css-variables) for more information.

## List of variables

Here's the list of variables available for customization:

**1\.** For default backgrounds

```css
--background: 0 0% 100%;
--foreground: 0 0% 4%;
```

**2\.** For muted backgrounds

```css
--muted: 0 0% 96%;
--muted-foreground: 0 0% 45%;
```

**3\.** Background color for cards

```css
--card: 0 0% 100%;
--card-foreground: 0 0% 4%;
```

**4\.** Background color for popovers

```css
--popover: 0 0% 100%;
--popover-foreground: 0 0% 4%;
```

**5\.** For border color

```css
--border: 0 0% 90%;
```

**6\.** Border color for inputs

```css
--input: 0 0% 90%;
```

**7\.** For primary colors

```css
--primary: 0 0% 9%;
--primary-foreground: 0 0% 98%;
```

**8\.** For secondary colors

```css
--secondary: 0 0% 96%;
--secondary-foreground: 0 0% 9%;
```

**9\.** For accents such as hover effects

```css
--accent: 0 0% 96%;
--accent-foreground: 0 0% 9%;
```

**10\.** For destructive actions

```css
--destructive: 357 100% 45%;
--destructive-foreground: 0 0% 100%;
```

**11\.** For focus ring

```css
--ring: 0 0% 63%;
```

## Adding new colors

To add new colors, simply add them to your main CSS file.

```css
:root {
  --warning: 38 92% 50%;
  --warning-foreground: 48 96% 89%;
}
 
.dark {
  --warning: 48 96% 89%;
  --warning-foreground: 38 92% 50%;
}
 
@theme {
  --color-warning: hsl(var(--warning));
  --color-warning-foreground: hsl(var(--warning-foreground));
}
```

You can now use the `warning` utility class in your components.

```html
<div class="bg-warning text-warning-foreground"></div>
```

## Custom palette

### Via CDN

**1.** Start by going to [https://ui.shadcn.com/colors](https://ui.shadcn.com/colors). Set the output format to **HSL** and pick your desired color. Use that color to assign values to the `--primary`, `--primary-foreground`, and `--ring` tokens. These tokens represent your main theme color, its contrasting foreground color, and the ring color for focus states.

**2.** Use the CSS snippet below as your starting point and replace the `*` with your theme name (e.g. `indigo`, `cyan`, `fuchsia`, etc.). You only need to update the values for `--primary`, `--primary-foreground`, and `--ring` for both light and dark modes, but you're free to customize everything else if needed.

```css
.uk-theme-emerald {
  --primary: 161.4 93.5% 30.4%;
  --primary-foreground: 151.8 81% 95.9%;
  --ring: 158.1 64.4% 51.6%;
}

.dark.uk-theme-emerald {
  --primary: 160.1 84.1% 39.4%;
  --primary-foreground: 151.8 81% 95.9%;
  --ring: 143.8 61.2% 20.2%;
}
```

Note: CDN theming only provides basic theming and won't customize checkboxes, radio buttons, or any other SVG-based background images, as colors need to be converted and injected (i.e., compiled). For advanced customization, please use the Vite plugin.

### Via NPM

**1.** Start by going to [https://ui.shadcn.com/colors](https://ui.shadcn.com/colors). Set the output format to **HSL** and pick your desired color. Use that color to assign values to the `--primary`, `--primary-foreground`, and `--ring` tokens. These tokens represent your main theme color, its contrasting foreground color, and the ring color for focus states.

**2.** Use the snippet below as your starting point and replace the `*` with your theme name (e.g. `indigo`, `cyan`, `fuchsia`, etc.). You only need to update the values for `--primary`, `--primary-foreground`, and `--ring` for both light and dark modes, but you're free to customize everything else if needed.

```javascript
'.uk-theme-*': {
  '--background': '0 0% 100%',
  '--foreground': '0 0% 4%',
  '--card': '0 0% 100%',
  '--card-foreground': '0 0% 4%',
  '--popover': '0 0% 100%',
  '--popover-foreground': '0 0% 4%',
  '--primary': '0 0% 9%',
  '--primary-foreground': '0 0% 98%',
  '--secondary': '0 0% 96%',
  '--secondary-foreground': '0 0% 9%',
  '--muted': '0 0% 96%',
  '--muted-foreground': '0 0% 45%',
  '--accent': '0 0% 96%',
  '--accent-foreground': '0 0% 9%',
  '--destructive': '357 100% 45%',
  '--destructive-foreground': '0 0% 100%',
  '--border': '0 0% 90%',
  '--input': '0 0% 90%',
  '--ring': '0 0% 63%'
},
'.dark.uk-theme-*': {
  '--background': '0 0% 4%',
  '--foreground': '0 0% 98%',
  '--card': '0 0% 9%',
  '--card-foreground': '0 0% 98%',
  '--popover': '0 0% 15%',
  '--popover-foreground': '0 0% 98%',
  '--primary': '0 0% 90%',
  '--primary-foreground': '0 0% 9%',
  '--secondary': '0 0% 15%',
  '--secondary-foreground': '0 0% 98%',
  '--muted': '0 0% 15%',
  '--muted-foreground': '0 0% 63%',
  '--accent': '0 0% 25%',
  '--accent-foreground': '0 0% 98%',
  '--destructive': '357 100% 45%',
  '--destructive-foreground': '0 0% 100%',
  '--border': '0 0% 100%',
  '--input': '0 0% 100%',
  '--ring': '0 0% 45%'
},
```

Note: If you're using the legacy color generators from version 2.0, make sure to include the following additional keys in **dark mode** for compatibility:

```js
.dark.uk-theme-* {
  '--destructive-alpha': '1',
  '--border-alpha': '1',
  '--input-alpha': '1'
}
```

**3.** Finally, configure your `vite.config.js` to add the custom palette. You will do this inside the `customPalette` option.

```js
import franken from "franken-ui/plugin-vite";
import tailwindcss from "@tailwindcss/vite";
import { defineConfig } from "vite";

export default defineConfig({
  plugins: [
    franken({
      customPalette: {
        ".uk-theme-emerald": {
          "--background": "0 0% 100%",
          "--foreground": "0 0% 4%",
          "--card": "0 0% 100%",
          "--card-foreground": "0 0% 4%",
          "--popover": "0 0% 100%",
          "--popover-foreground": "0 0% 4%",
          "--primary": "161.4 93.5% 30.4%",
          "--primary-foreground": "151.8 81% 95.9%",
          "--secondary": "0 0% 96%",
          "--secondary-foreground": "0 0% 9%",
          "--muted": "0 0% 96%",
          "--muted-foreground": "0 0% 45%",
          "--accent": "0 0% 96%",
          "--accent-foreground": "0 0% 9%",
          "--destructive": "357 100% 45%",
          "--destructive-foreground": "0 0% 100%",
          "--border": "0 0% 90%",
          "--input": "0 0% 90%",
          "--ring": "158.1 64.4% 51.6%",
        },
        ".dark.uk-theme-emerald": {
          "--background": "0 0% 4%",
          "--foreground": "0 0% 98%",
          "--card": "0 0% 9%",
          "--card-foreground": "0 0% 98%",
          "--popover": "0 0% 15%",
          "--popover-foreground": "0 0% 98%",
          "--primary": "160.1 84.1% 39.4%",
          "--primary-foreground": "151.8 81% 95.9%",
          "--secondary": "0 0% 15%",
          "--secondary-foreground": "0 0% 98%",
          "--muted": "0 0% 15%",
          "--muted-foreground": "0 0% 63%",
          "--accent": "0 0% 25%",
          "--accent-foreground": "0 0% 98%",
          "--destructive": "357 100% 45%",
          "--destructive-foreground": "0 0% 100%",
          "--border": "0 0% 100%",
          "--input": "0 0% 100%",
          "--ring": "143.8 61.2% 20.2%",
        },
      },
    }),
    tailwindcss(),
  ],
});
```

## Setting the default palette

To set your newly added palette as the default, simply update the script in your `<head>` tag to reference the new theme name, like so:

```html
<script>
  const htmlElement = document.documentElement;

  const __FRANKEN__ = JSON.parse(
    localStorage.getItem("__FRANKEN__") || "{}",
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

  htmlElement.classList.add(__FRANKEN__.theme || "uk-theme-emerald");
  htmlElement.classList.add(__FRANKEN__.radii || "uk-radii-md");
  htmlElement.classList.add(__FRANKEN__.shadows || "uk-shadows-sm");
  htmlElement.classList.add(__FRANKEN__.font || "uk-font-sm");
  htmlElement.classList.add(__FRANKEN__.chart || "uk-chart-default");
</script>
```

## Adding to theme switcher

To register your newly added palette with the [Theme Switcher](https://franken-ui.dev/docs/2.1/theme-switcher#custom-palette), please refer to the corresponding documentation or guide for step-by-step instructions on how to integrate it.
