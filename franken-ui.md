## Overview

Franken UI is an open-source library of UI components. Under the hood, it uses UIkit 3 and extended with LitElement. The design is based on shadcn/ui.

## With Tailwind CSS v4

If you'd like to use Tailwind CSS v4 alongside Franken UI, you can manually configure your `@theme` directives like so:

```css
@import "tailwindcss";
@import "franken-ui/css/franken-ui.css";

@theme {
  --color-background: hsl(var(--background));
  --color-foreground: hsl(var(--foreground));
  --color-muted: hsl(var(--muted));
  --color-muted-foreground: hsl(var(--muted-foreground));
  --color-card: hsl(var(--card));
  --color-card-foreground: hsl(var(--card-foreground));
  --color-popover: hsl(var(--popover));
  --color-popover-foreground: hsl(var(--popover-foreground));
  --color-border: hsl(var(--border) / var(--border-alpha, 1));
  --color-input: hsl(var(--input) / var(--input-alpha, 1));
  --color-primary: hsl(var(--primary));
  --color-primary-foreground: hsl(var(--primary-foreground));
  --color-secondary: hsl(var(--secondary));
  --color-secondary-foreground: hsl(var(--secondary-foreground));
  --color-accent: hsl(var(--accent));
  --color-accent-foreground: hsl(var(--accent-foreground));
  --color-destructive: hsl(var(--destructive) / var(--destructive-alpha, 1));
  --color-destructive-foreground: hsl(var(--destructive-foreground));
  --color-ring: hsl(var(--ring));

  --font-geist-sans: Geist Sans, ui-sans-serif, system-ui, sans-serif,
    "Apple Color Emoji", "Segoe UI Emoji", Segoe UI Symbol, "Noto Color Emoji";
  --font-geist-mono: Geist Mono, ui-monospace, SFMono-Regular, Menlo, Monaco,
    Consolas, "Liberation Mono", "Courier New", monospace;
}
```

This will allow you to use utilities like `bg-primary`, `bg-muted`, and other custom utility classes within your project. Make sure to update your `vite.config.js` as well.

```js
import franken from "franken-ui/plugin-vite";
import { defineConfig } from "vite";

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

Note: If you choose to use Franken UI alongside Tailwind CSS v4, make sure to set `preflight` to `false` in your `vite.config.js`, as Tailwind already includes this feature. You also need to set `layer` to `true` to make the class hirarchy equal. Adding components inside `layerExceptions` will disable CSS layering for those components, placing them at the highest level of hierarchy.