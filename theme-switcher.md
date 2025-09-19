## Theme switcher

To implement the Theme Switcher, you'll need to make some modifications to your HTML code to allow users to change their preferences.

**1.** Start by setting a default theme and mode in the `<head>` tag of your HTML by checking the user's preference:

```html
<script>
  const htmlElement = document.documentElement;

  const __FRANKEN__ = JSON.parse(localStorage.getItem("__FRANKEN__") || "{}");

  if (
    __FRANKEN__.mode === "dark" ||
    (!__FRANKEN__.mode &&
      window.matchMedia("(prefers-color-scheme: dark)").matches)
  ) {
    htmlElement.classList.add("dark");
  } else {
    htmlElement.classList.remove("dark");
  }

  htmlElement.classList.add(__FRANKEN__.theme || "uk-theme-neutral");
  htmlElement.classList.add(__FRANKEN__.radii || "uk-radii-md");
  htmlElement.classList.add(__FRANKEN__.shadows || "uk-shadows-sm");
  htmlElement.classList.add(__FRANKEN__.font || "uk-font-sm");
  htmlElement.classList.add(__FRANKEN__.chart || "uk-chart-default");
</script>
```

This will first check if a user previously set the theme color preference manually using local storage, and as a fallback, it will either set dark or light mode based on the browser's color scheme preference.

Note: You can replace `uk-theme-neutral` with any of the 15 available themes you want as the default.

**2\.** Ensure that your `<body>` tag includes the classes `bg-background` and `text-foreground` to apply the proper background and text colors that automatically adapt to the currently set theme.

```html
<!doctype html>
<html lang="en">
  <head>
    <!-- ... -->
  </head>
  <body class="bg-background text-foreground">
    <!-- ... -->
  </body>
</html>
```

**3\.** You can now use the `<uk-theme-switcher>` markup in your HTML code with one `<select hidden></select>` tag as items reference and place it however you like.

### Example

```html
<uk-theme-switcher>
  <select hidden>
    <optgroup data-key="theme" label="Theme">
      <option data-hex="#52525b" value="uk-theme-zinc">Zinc</option>
      <option data-hex="#64748b" value="uk-theme-slate">Slate</option>
      <option data-hex="#78716c" value="uk-theme-stone">Stone</option>
      <option data-hex="#6b7280" value="uk-theme-gray">Gray</option>
      <option data-hex="#737373" value="uk-theme-neutral" selected>
        Neutral
      </option>
      <option data-hex="#dc2626" value="uk-theme-red">Red</option>
      <option data-hex="#e11d48" value="uk-theme-rose">Rose</option>
      <option data-hex="#f97316" value="uk-theme-orange">Orange</option>
      <option data-hex="#65a30d" value="uk-theme-green">Green</option>
      <option data-hex="#2563eb" value="uk-theme-blue">Blue</option>
      <option data-hex="#facc15" value="uk-theme-yellow">Yellow</option>
      <option data-hex="#7c3aed" value="uk-theme-violet">Violet</option>
      <option data-hex="#d97706" value="uk-theme-amber">Amber</option>
      <option data-hex="#9333ea" value="uk-theme-purple">Purple</option>
      <option data-hex="#0d9488" value="uk-theme-teal">Teal</option>
    </optgroup>
  </select>
</uk-theme-switcher>
```

## Custom palette

First, ensure that your `vite.config.js` file is configured to include your custom palette. For more information on how to do this, please refer to the [documentation](https://franken-ui.dev/docs/2.1/theming#custom-palette).

## Adding or removing themes

To add or remove theme options, simply add or remove `<option>` tags within the `<optgroup data-key="theme" label="Theme">` group. Each theme option should follow the format:

```html
<option data-hex="#dc2626" value="uk-theme-red">Red</option>
```

Where:

- The `data-hex` specifies the hex code for the theme preview.
- The `value` specifies the class name for the theme.
- The option text specifies the label for the theme.

## Radii

To allow users to customize radii, add an `<optgroup data-key="radii" label="Radii">` group within the `<select hidden>` tag. This group should contain `<option>` tags for each radii option, such as:

```html
<uk-theme-switcher>
  <select hidden>
    <optgroup data-key="theme" label="Theme">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="radii" label="Radii">
      <option value="uk-radii-none">None</option>
      <option value="uk-radii-sm">Small</option>
      <option value="uk-radii-md">Medium</option>
      <option value="uk-radii-lg">Large</option>
    </optgroup>
  </select>
</uk-theme-switcher>
```

## Shadows

Similarly, to allow users to customize shadows, add an `<optgroup data-key="shadows" label="Shadows">` group within the `<select hidden>` tag. This group should contain `<option>` tags for each shadow option, such as:

```html
<uk-theme-switcher>
  <select hidden>
    <optgroup data-key="theme" label="Theme">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="radii" label="Radii">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="shadows" label="Shadows">
      <option value="uk-shadows-none">None</option>
      <option value="uk-shadows-sm">Small</option>
      <option value="uk-shadows-md">Medium</option>
      <option value="uk-shadows-lg">Large</option>
    </optgroup>
  </select>
</uk-theme-switcher>
```

## Font

You can also allow users to customize font size, just add an `<optgroup data-key="font" label="Font">` group within the `<select hidden>` tag. This group should contain `<option>` tags for each font option, such as:

```html
<uk-theme-switcher>
  <select hidden>
    <optgroup data-key="theme" label="Theme">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="radii" label="Radii">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="shadows" label="Shadows">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="font" label="Font">
      <option value="uk-font-sm">Small</option>
      <option value="uk-font-base">Default</option>
    </optgroup>
  </select>
</uk-theme-switcher>
```

## Modes

To allow users to switch between light and dark modes, add an `<optgroup data-key="mode" label="Mode">` group within the `<select hidden>` tag. This group should contain `<option>` tags for each mode option, such as:

```html
<uk-theme-switcher>
  <select hidden>
    <optgroup data-key="theme" label="Theme">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="radii" label="Radii">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="shadows" label="Shadows">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="mode" label="Mode">
      <option data-icon="sun" value="light">Light</option>
      <option data-icon="moon" value="dark">Dark</option>
    </optgroup>
  </select>
</uk-theme-switcher>
```

## Charts

To allow users to switch between chart themes, add an `<optgroup data-key="chart" label="Chart">` group within the `<select hidden>` tag. This group should contain `<option>` tags for each chart theme option, such as:

```html
<uk-theme-switcher>
  <select hidden>
    <optgroup data-key="theme" label="Theme">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="radii" label="Radii">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="shadows" label="Shadows">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="mode" label="Mode">
      <!-- ... -->
    </optgroup>
    <optgroup data-key="chart" label="Chart">
      <option value="uk-chart-default" selected>
        Default
      </option>
      <option data-hex="#e76e50" value="uk-chart-palette">
        Palette
      </option>
      <option data-hex="#2563eb" value="uk-chart-sapphire">Sapphire</option>
      <option data-hex="#e21d48" value="uk-chart-ruby">Ruby</option>
      <option data-hex="#1dc355" value="uk-chart-emerald">Emerald</option>
      <option data-hex="#ad7c48" value="uk-chart-daylight">Daylight</option>
      <option data-hex="#959593" value="uk-chart-midnight">Midnight</option>
    </optgroup>
  </select>
</uk-theme-switcher>
```

Note: The values inside the `<option>` tags will be attached to the `<head>` tag, allowing for customization. However, the dark and light classes are exceptions and will be handled differently.

## Dropdown

You can use the [Drop](https://franken-ui.dev/docs/2.1/drop) component to display the Theme Switcher, providing a compact and convenient way to access theme options.

### Example

```html
<div class="uk-inline">
  <button class="uk-btn uk-btn-default">Open</button>
  <div
    class="uk-card uk-card-body uk-drop w-96"
    data-uk-drop="mode: click; offset: 8"
  >
    <uk-theme-switcher id="theme-switcher">
      <select hidden>
        <optgroup data-key="theme" label="Theme">
          <option data-hex="#d97706" value="uk-theme-amber">Amber</option>
          <option data-hex="#9333ea" value="uk-theme-purple">Purple</option>
          <option data-hex="#0d9488" value="uk-theme-teal">Teal</option>
        </optgroup>
      </select>
    </uk-theme-switcher>
  </div>
</div>
```

## Modal

Alternatively, you can also display the Theme Switcher inside a [Modal](https://franken-ui.dev/docs/2.1/modal) component.

### Example

```html
<a class="uk-btn uk-btn-default" href="#theme-switcher-modal" data-uk-toggle>
  Open
</a>

<div class="uk-modal" id="theme-switcher-modal" data-uk-modal>
  <div class="uk-modal-dialog">
    <button
      class="uk-modal-close absolute right-4 top-4"
      type="button"
      data-uk-close
    ></button>
    <div class="uk-modal-header">
      <div class="uk-modal-title">Customize</div>
    </div>
    <div class="uk-modal-body">
      <uk-theme-switcher id="theme-switcher">
        <select hidden>
          <optgroup data-key="theme" label="Theme">
            <option data-hex="#52525b" value="uk-theme-zinc">Zinc</option>

            <option data-hex="#64748b" value="uk-theme-slate">Slate</option>
            <option data-hex="#78716c" value="uk-theme-stone">Stone</option>
            <option data-hex="#6b7280" value="uk-theme-gray">Gray</option>
            <option data-hex="#737373" value="uk-theme-neutral" selected>
              Neutral
            </option>
            <option data-hex="#dc2626" value="uk-theme-red">Red</option>
            <option data-hex="#e11d48" value="uk-theme-rose">Rose</option>
            <option data-hex="#f97316" value="uk-theme-orange">Orange</option>
            <option data-hex="#65a30d" value="uk-theme-green">Green</option>
            <option data-hex="#2563eb" value="uk-theme-blue">Blue</option>
            <option data-hex="#facc15" value="uk-theme-yellow">Yellow</option>
            <option data-hex="#7c3aed" value="uk-theme-violet">Violet</option>
            <option data-hex="#d97706" value="uk-theme-amber">Amber</option>
            <option data-hex="#9333ea" value="uk-theme-purple">Purple</option>
            <option data-hex="#0d9488" value="uk-theme-teal">Teal</option>
          </optgroup>
          <optgroup data-key="radii" label="Radii">
            <option value="uk-radii-none">None</option>
            <option value="uk-radii-sm">Small</option>
            <option value="uk-radii-md" selected>Medium</option>
            <option value="uk-radii-lg">Large</option>
          </optgroup>
          <optgroup data-key="shadows" label="Shadows">
            <option value="uk-shadows-none">None</option>
            <option value="uk-shadows-sm" selected>Small</option>
            <option value="uk-shadows-md">Medium</option>
            <option value="uk-shadows-lg">Large</option>
          </optgroup>
          <optgroup data-key="font" label="Font">
            <option value="uk-font-sm" selected>Small</option>
            <option value="uk-font-base">Default</option>
          </optgroup>
          <optgroup data-key="mode" label="Mode">
            <option data-icon="sun" value="light">Light</option>
            <option data-icon="moon" value="dark">Dark</option>
          </optgroup>
        </select>
      </uk-theme-switcher>
    </div>
  </div>
</div>
```

## Internationalization

To customize language, you can now directly do it inside your markup. This allows for more flexibility and control over the text displayed to your users.

### Example

```html
<uk-theme-switcher>
  <select hidden>
    <optgroup data-key="theme" label="テーマ">
      <option data-hex="#52525b" value="uk-theme-zinc" selected>亜鉛</option>
      <option data-hex="#64748b" value="uk-theme-slate">スレート</option>
      <option data-hex="#78716c" value="uk-theme-stone">石</option>
      <option data-hex="#6b7280" value="uk-theme-gray">グレー</option>
      <option data-hex="#737373" value="uk-theme-neutral">中性</option>
      <option data-hex="#dc2626" value="uk-theme-red">赤</option>
      <option data-hex="#e11d48" value="uk-theme-rose">薔薇</option>
      <option data-hex="#f97316" value="uk-theme-orange">オレンジ</option>
      <option data-hex="#16a34a" value="uk-theme-green">緑</option>
      <option data-hex="#2563eb" value="uk-theme-blue">青</option>
      <option data-hex="#facc15" value="uk-theme-yellow">黄色</option>
      <option data-hex="#7c3aed" value="uk-theme-violet">バイオレット</option>
      <option data-hex="#d97706" value="uk-theme-amber">アンバー</option>
      <option data-hex="#9333ea" value="uk-theme-purple">パープル</option>
      <option data-hex="#0d9488" value="uk-theme-teal">ティール</option>
    </optgroup>
    <optgroup data-key="radii" label="半径">
      <option value="uk-radii-none">なし</option>
      <option value="uk-radii-sm">小さい</option>
      <option value="uk-radii-md" selected>中くらい</option>
      <option value="uk-radii-lg">大きい</option>
    </optgroup>
    <optgroup data-key="shadows" label="影">
      <option value="uk-shadows-none">なし</option>
      <option value="uk-shadows-sm" selected>小さい</option>
      <option value="uk-shadows-md">中くらい</option>
      <option value="uk-shadows-lg">大きい</option>
    </optgroup>
    <optgroup data-key="font" label="フォント">
      <option value="uk-font-sm" selected>小さい</option>
      <option value="uk-font-base">デフォルト</option>
    </optgroup>
    <optgroup data-key="mode" label="モード">
      <option data-icon="sun" value="light">ライト</option>
      <option data-icon="moon" value="dark">暗い</option>
    </optgroup>
  </select>
</uk-theme-switcher>
```

## Attributes

The following attributes are available for this component:

| Name                     | Type    | Default | Description                                |
| ------------------------ | ------- | ------- | ------------------------------------------ |
| `force-prevent-rerender` | Boolean | false   | Forcefully prevents component rerendering. |

## Events

The Theme Switcher component triggers the following events on elements with this component attached:

| Name                       | Description                       |
| -------------------------- | --------------------------------- |
| `uk-theme-switcher:change` | Fired when something has changed. |
