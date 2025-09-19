## Nav

To apply this component, use the following classes.

| Class         | Description                                                                                                      |
| ------------- | ---------------------------------------------------------------------------------------------------------------- |
| `.uk-nav`     | Add this class to a `<ul>` element to define the Nav component. Use `<a>` elements as nav items within the list. |
| `.uk-active ` | Add this class to a list item to apply an active state to a menu item.                                           |

```html
<ul class="uk-nav">
  <li class="uk-active"><a href=""></a></li>
  <li><a href=""></a></li>
</ul>
```

### Example

```html
<div class="max-w-sm">
  <ul class="uk-nav uk-nav-default">
    <li class="uk-active"><a href="#">Active</a></li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
  </ul>
</div>
```

Note: By default, the nav has no styling. That's why it is important to add a modifier class. In our example we are using the `.uk-nav-default` class.

## Nested navs

Add the `.uk-parent` class to an item to turn it into a parent. Add the `.uk-nav-sub` class to a `<ul>` element inside the item to create the subnav.

```html
<ul class="uk-nav">
  <li class="uk-parent">
    <a href=""></a>
    <ul class="uk-nav-sub">
      <li><a href=""></a></li>
      <li>
        <a href=""></a>
        <ul>
          ...
        </ul>
      </li>
    </ul>
  </li>
</ul>
```

### Example

```html
<div class="max-w-sm">
  <ul class="uk-nav uk-nav-default">
    <li class="uk-active"><a href="#">Active</a></li>
    <li class="uk-parent">
      <a href="#">Parent</a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li>
          <a href="#">Sub item</a>
          <ul>
            <li><a href="#">Sub item</a></li>
            <li><a href="#">Sub item</a></li>
          </ul>
        </li>
      </ul>
    </li>
  </ul>
</div>
```

## Accordion

By default, child menu items are always visible. To apply an accordion effect, just add the `data-uk-nav` attribute to the main `<ul>`.

Note: The attribute automatically sets the `.uk-nav` class, so you don't have to apply it manually.

```html
<ul data-uk-nav>
  ...
</ul>
```

### Example

```html
<div class="max-w-sm">
  <ul class="uk-nav-default" data-uk-nav>
    <li class="uk-active"><a href="#">Active</a></li>
    <li class="uk-parent">
      <a href="#">Parent</a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li>
          <a href="#">Sub item</a>
          <ul>
            <li><a href="#">Sub item</a></li>
            <li><a href="#">Sub item</a></li>
          </ul>
        </li>
      </ul>
    </li>
    <li class="uk-parent">
      <a href="#">Parent</a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li><a href="#">Sub item</a></li>
      </ul>
    </li>
  </ul>
</div>
```

### Parent icon

To create a parent icon, just add the `data-uk-nav-parent-icon` attribute to a `<span>` element.

```html
<ul data-uk-nav>
  <li>
    <a href="">Parent <span data-uk-nav-parent-icon></span></a>
    ...
  </li>
</ul>
```

### Example

```html
<div class="max-w-sm">
  <ul class="uk-nav-default" data-uk-nav>
    <li class="uk-active"><a href="#">Active</a></li>
    <li class="uk-parent">
      <a href="#">Parent <span data-uk-nav-parent-icon></span></a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li>
          <a href="#">Sub item</a>
          <ul>
            <li><a href="#">Sub item</a></li>
            <li><a href="#">Sub item</a></li>
          </ul>
        </li>
      </ul>
    </li>
    <li class="uk-parent">
      <a href="#">Parent <span data-uk-nav-parent-icon></span></a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li><a href="#">Sub item</a></li>
      </ul>
    </li>
  </ul>
</div>
```

### Multiple open subnavs

When clicking on a parent item, an open one will close, allowing only one open nested list at a time. To allow multiple open subnavs, just add the `multiple: true` option to the attribute.

```html
<ul data-uk-nav="multiple: true">
  ...
</ul>
```

### Example

```html
<div class="max-w-sm">
  <ul class="uk-nav-default" data-uk-nav="multiple: true">
    <li class="uk-active"><a href="#">Active</a></li>
    <li class="uk-parent">
      <a href="#">Parent <span data-uk-nav-parent-icon></span></a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li>
          <a href="#">Sub item</a>
          <ul>
            <li><a href="#">Sub item</a></li>
            <li><a href="#">Sub item</a></li>
          </ul>
        </li>
      </ul>
    </li>
    <li class="uk-parent">
      <a href="#">Parent <span data-uk-nav-parent-icon></span></a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li><a href="#">Sub item</a></li>
      </ul>
    </li>
  </ul>
</div>
```

## Header and divider

Add one of the following classes to a list item to create a header or a divider between items.

| Element           | Description                                                                  |
| ----------------- | ---------------------------------------------------------------------------- |
| `.uk-nav-header`  | Add this class to a `<li>` element to create a header.                       |
| `.uk-nav-divider` | Add this class to a `<li>` element to create a divider separating nav items. |

```html
<li class="uk-nav-header"></li>

<li class="uk-nav-divider"></li>
```

### Example

```html
<div class="max-w-sm">
  <ul class="uk-nav uk-nav-default">
    <li class="uk-nav-header">Header</li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
    <li class="uk-nav-divider"></li>
    <li><a href="#">Item</a></li>
  </ul>
</div>
```

## Subtitle

Add the `.uk-nav-subtitle` class to a `div` element to create an item subtitled.

```html
<ul class="uk-nav">
  <li>
    <a href="">
      <div>
        Item
        <div class="uk-nav-subtitle">
          Subtitle lorem ipsum dolor sit amet, consectetur adipiscing elit, sed
          do.
        </div>
      </div>
    </a>
  </li>
</ul>
```

### Example

```html
<div class="max-w-sm">
  <ul class="uk-nav uk-nav-default">
    <li class="uk-active">
      <a href="#"
        ><div>
          Active
          <div class="uk-nav-subtitle">
            Subtitle lorem ipsum dolor sit amet, consectetur adipiscing elit,
            sed do.
          </div>
        </div></a
      >
    </li>
    <li>
      <a href="#"
        ><div>
          Item
          <div class="uk-nav-subtitle">
            Subtitle lorem ipsum dolor sit amet, consectetur adipiscing elit,
            sed do.
          </div>
        </div></a
      >
    </li>
    <li>
      <a href="#"
        ><div>
          Item
          <div class="uk-nav-subtitle">
            Subtitle lorem ipsum dolor sit amet, consectetur adipiscing elit,
            sed do.
          </div>
        </div></a
      >
    </li>
    <li>
      <a href="#"
        ><div>
          Item
          <div class="uk-nav-subtitle">
            Subtitle lorem ipsum dolor sit amet, consectetur adipiscing elit,
            sed do.
          </div>
        </div></a
      >
    </li>
  </ul>
</div>
```

## Default modifier

Add the `.uk-nav-default` class to give the nav its default style. You can place the nav inside cards or anywhere else in your content.

```html
<ul class="uk-nav uk-nav-default">
  ...
</ul>
```

### Example

```html
<div class="uk-card uk-card-body max-w-sm">
  <ul class="uk-nav-default" data-uk-nav>
    <li class="uk-active"><a href="#">Active</a></li>
    <li class="uk-parent">
      <a href="#">Parent <span data-uk-nav-parent-icon></span></a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li><a href="#">Sub item</a></li>
      </ul>
    </li>
    <li class="uk-parent">
      <a href="#">Parent <span data-uk-nav-parent-icon></span></a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li><a href="#">Sub item</a></li>
      </ul>
    </li>
    <li class="uk-nav-header">Header</li>
    <li>
      <a href="#">
        <uk-icon class="mr-2" icon="table"></uk-icon>
        Item
      </a>
    </li>
    <li>
      <a href="#">
        <uk-icon class="mr-2" icon="bell"></uk-icon>
        Item
      </a>
    </li>
    <li class="uk-nav-divider"></li>
    <li>
      <a href="#">
        <uk-icon class="mr-2" icon="trash"></uk-icon>
        Item
      </a>
    </li>
  </ul>
</div>
```

## Primary modifier

Add the `.uk-nav-primary` class to give the nav a more distinct styling, for example when placing it inside a modal.

```html
<ul class="uk-nav uk-nav-primary">
  ...
</ul>
```

### Example

```html
<div class="max-w-sm">
  <ul class="uk-nav-primary" data-uk-nav>
    <li class="uk-active"><a href="#">Active</a></li>
    <li class="uk-parent">
      <a href="#">Parent <span data-uk-nav-parent-icon></span></a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li><a href="#">Sub item</a></li>
      </ul>
    </li>
    <li class="uk-parent">
      <a href="#">Parent <span data-uk-nav-parent-icon></span></a>
      <ul class="uk-nav-sub">
        <li><a href="#">Sub item</a></li>
        <li><a href="#">Sub item</a></li>
      </ul>
    </li>
    <li><a href="#">Item</a></li>
  </ul>
</div>
```

## Secondary modifier

Add the `.uk-nav-secondary` class to have an extra style if the nav has subtitles.

```html
<ul class="uk-nav uk-nav-secondary">
  ...
</ul>
```

### Example

```html
<div class="max-w-sm">
  <ul class="uk-nav uk-nav-secondary">
    <li>
      <a class="">
        <div class="flex">
          <uk-icon width="20" height="20" icon="bell"></uk-icon>
          <div class="ml-2">
            <p>Everything</p>
            <p class="text-sm text-muted-foreground">
              Email digest, mentions & all activity.
            </p>
          </div>
        </div>
      </a>
    </li>
    <li class="uk-active">
      <a class="">
        <div class="flex">
          <uk-icon width="20" height="20" icon="user"></uk-icon>
          <div class="ml-2">
            <p>Available</p>
            <p class="text-sm text-muted-foreground">
              Only mentions and comments.
            </p>
          </div>
        </div>
      </a>
    </li>
    <li>
      <a class="">
        <div class="flex">
          <uk-icon width="20" height="20" icon="eye-off"></uk-icon>
          <div class="ml-2">
            <p>Ignoring</p>
            <p class="text-sm text-muted-foreground">
              Turn off all notifications.
            </p>
          </div>
        </div>
      </a>
    </li>
  </ul>
</div>
```

## Nav in Dropdown

Add the `.uk-dropdown-nav` class to place a nav inside a default dropdown from the [Dropdown component](https://franken-ui.dev/docs/2.1/dropdown).

```html
<div data-uk-dropdown>
  <ul class="uk-dropdown-nav uk-nav">
    ...
  </ul>
</div>
```

### Example

```html
<button class="uk-btn uk-btn-default" type="button">Hover</button>
<div class="uk-drop min-w-52" data-uk-dropdown>
  <ul class="uk-nav uk-dropdown-nav">
    <li class="uk-active"><a href="#">Active</a></li>
    <li><a href="#">Item</a></li>
    <li class="uk-nav-header">Header</li>
    <li><a href="#">Item</a></li>
    <li><a href="#">Item</a></li>
    <li class="uk-nav-divider"></li>
    <li><a href="#">Item</a></li>
  </ul>
</div>
```

## Nav in offcanvas

A nav can be used inside an offcanvas from the [Offcanvas component](https://franken-ui.dev/docs/2.1/offcanvas). No modifier class needs to be added.

### Example

```html
<a href="#offcanvas-slide" class="uk-btn uk-btn-default" data-uk-toggle>
  Open
</a>

<div class="uk-offcanvas" id="offcanvas-slide" data-uk-offcanvas>
  <div class="uk-offcanvas-bar">
    <ul class="uk-nav uk-nav-primary">
      <li class="uk-active"><a href="#">Active</a></li>
      <li><a href="#">Item</a></li>
      <li class="uk-nav-header">Header</li>
      <li><a href="#">Item</a></li>
      <li><a href="#">Item</a></li>
      <li class="uk-nav-divider"></li>
      <li><a href="#">Item</a></li>
    </ul>
  </div>
</div>
```

## Component options

Any of these options can be applied to the component attribute. Separate multiple options with a semicolon. [Learn more](https://franken-ui.dev/docs/2.1/javascript#component-configuration)

| Option        | Value           | Default        | Description                                                                                |
| ------------- | --------------- | -------------- | ------------------------------------------------------------------------------------------ |
| `targets`     | CSS selector    | `> .uk-parent` | The element(s) to toggle.                                                                  |
| `toggle `     | CSS selector    | `> a`          | The toggle element(s).                                                                     |
| `content`     | CSS selector    | `> ul`         | The content element(s).                                                                    |
| `collapsible` | Boolean         | `true`         | Allow all items to be closed.                                                              |
| `multiple`    | Boolean         | `false`        | Allow multiple open items.                                                                 |
| `transition`  | String          | `ease`         | The transition to use.                                                                     |
| `animation`   | Boolean, String | `true`         | Space-separated names of [animations](https://franken-ui.dev/docs/2.1/animation). Comma-separated for animation out. |
| `duration`    | Number          | `200`          | The animation duration in milliseconds.                                                    |

## JavaScript

Learn more about [JavaScript components](https://franken-ui.dev/docs/2.1/javascript#programmatic-use).

### Initialization

```javascript
UIkit.nav(element, options);
```

### Methods

The following methods are available for the component:

#### Toggle

```javascript
UIkit.nav(element).toggle(index, animate);
```

Toggles the content pane.

| Name      | Type                 | Default | Description                                  |
| --------- | -------------------- | ------- | -------------------------------------------- |
| `index`   | String, Number, Node | 0       | Nav pane to toggle. 0 based index.           |
| `animate` | Boolean              | true    | Suppress opening animation by passing false. |
