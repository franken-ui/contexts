## Sortable

Drag and drop an element to a new location within the sortable grid, while the other items adjust to fit. This is great, if you want to sort items like gallery or menu items, for example.

To apply this component, add the `data-uk-sortable` attribute to a container and create child elements.

```html
<div data-uk-sortable>
  <div></div>
  <div></div>
</div>
```

### Example

```html
<ul
  class="grid grid-cols-2 gap-4 md:grid-cols-4"
  data-uk-sortable="handle: .handle"
>
  <li>
    <div class="handle bg-muted p-4 text-center text-muted-foreground">
      Item 1
    </div>
  </li>
  <li>
    <div class="handle bg-muted p-4 text-center text-muted-foreground">
      Item 2
    </div>
  </li>
  <li>
    <div class="handle bg-muted p-4 text-center text-muted-foreground">
      Item 3
    </div>
  </li>
  <li>
    <div class="handle bg-muted p-4 text-center text-muted-foreground">
      Item 4
    </div>
  </li>
  <li>
    <div class="handle bg-muted p-4 text-center text-muted-foreground">
      Item 5
    </div>
  </li>
  <li>
    <div class="handle bg-muted p-4 text-center text-muted-foreground">
      Item 6
    </div>
  </li>
  <li>
    <div class="handle bg-muted p-4 text-center text-muted-foreground">
      Item 7
    </div>
  </li>
  <li>
    <div class="handle bg-muted p-4 text-center text-muted-foreground">
      Item 8
    </div>
  </li>
</ul>
```

## Handle

By default, the entire sortable element can be used for drag and drop sorting. To create a handle which will be used instead, just add the `handle: SELECTOR` option to the attribute and add the handle class to the element that you want to use as a handle.

```html
<ul data-uk-sortable="handle: .uk-sortable-handle">
  <li>
    <div class="uk-sortable-handle"></div>
    ...
  </li>
</ul>
```

### Example

```html
<ul
  class="grid grid-cols-2 gap-4 md:grid-cols-4"
  data-uk-sortable="handle: .uk-sortable-handle"
>
  <li>
    <div
      class="flex items-center justify-center bg-muted p-4 text-muted-foreground"
    >
      <span class="uk-sortable-handle mr-2">
        <uk-icon icon="move"></uk-icon>
      </span>
      Item 1
    </div>
  </li>
  <li>
    <div
      class="flex items-center justify-center bg-muted p-4 text-muted-foreground"
    >
      <span class="uk-sortable-handle mr-2">
        <uk-icon icon="move"></uk-icon>
      </span>
      Item 2
    </div>
  </li>
  <li>
    <div
      class="flex items-center justify-center bg-muted p-4 text-muted-foreground"
    >
      <span class="uk-sortable-handle mr-2">
        <uk-icon icon="move"></uk-icon>
      </span>
      Item 3
    </div>
  </li>
  <li>
    <div
      class="flex items-center justify-center bg-muted p-4 text-muted-foreground"
    >
      <span class="uk-sortable-handle mr-2">
        <uk-icon icon="move"></uk-icon>
      </span>
      Item 4
    </div>
  </li>
  <li>
    <div
      class="flex items-center justify-center bg-muted p-4 text-muted-foreground"
    >
      <span class="uk-sortable-handle mr-2">
        <uk-icon icon="move"></uk-icon>
      </span>
      Item 5
    </div>
  </li>
  <li>
    <div
      class="flex items-center justify-center bg-muted p-4 text-muted-foreground"
    >
      <span class="uk-sortable-handle mr-2">
        <uk-icon icon="move"></uk-icon>
      </span>
      Item 6
    </div>
  </li>
  <li>
    <div
      class="flex items-center justify-center bg-muted p-4 text-muted-foreground"
    >
      <span class="uk-sortable-handle mr-2">
        <uk-icon icon="move"></uk-icon>
      </span>
      Item 7
    </div>
  </li>
  <li>
    <div
      class="flex items-center justify-center bg-muted p-4 text-muted-foreground"
    >
      <span class="uk-sortable-handle mr-2">
        <uk-icon icon="move"></uk-icon>
      </span>
      Item 8
    </div>
  </li>
</ul>
```

## Group

To be able to sort items from one list to another, you can group them by adding the `group: GROUP-NAME` option to the `data-uk-sortable` attribute on each list.

```html
<div data-uk-sortable="group: my-group">
  <div></div>
</div>

<div data-uk-sortable="group: my-group">
  <div></div>
</div>
```

### Example

```html
<div class="grid grid-cols-1 gap-4 md:grid-cols-3">
  <div class="uk-placeholder">
    <h4 class="uk-h4 mb-4">Group 1</h4>
    <div class="space-y-4" data-uk-sortable="group: sortable-group">
      <div class="bg-muted p-4 text-muted-foreground">Item 1</div>
      <div class="bg-muted p-4 text-muted-foreground">Item 2</div>
      <div class="bg-muted p-4 text-muted-foreground">Item 3</div>
      <div class="bg-muted p-4 text-muted-foreground">Item 4</div>
    </div>
  </div>
  <div class="uk-placeholder">
    <h4 class="uk-h4 mb-4">Group 2</h4>
    <div class="space-y-4" data-uk-sortable="group: sortable-group">
      <div class="bg-muted p-4 text-muted-foreground">Item 1</div>
      <div class="bg-muted p-4 text-muted-foreground">Item 2</div>
      <div class="bg-muted p-4 text-muted-foreground">Item 3</div>
      <div class="bg-muted p-4 text-muted-foreground">Item 4</div>
    </div>
  </div>
  <div class="uk-placeholder">
    <h4 class="uk-h4 mb-4">Empty Group</h4>
    <div class="space-y-4" data-uk-sortable="group: sortable-group"></div>
  </div>
</div>
```

## Custom class

You can also apply one or more custom classes to items when they are being dragged. To do so, add the `cls-custom: MY-CLASS` option to the attribute.

```html
<ul data-uk-sortable="cls-custom: my-class">
  ...
</ul>
```

### Example

```html
<ul class="max-w-sm space-y-4" data-uk-sortable="cls-custom: uk-placeholder">
  <li class="bg-muted p-4 text-muted-foreground">
    <a href="#">Item 1</a>
  </li>
  <li class="bg-muted p-4 text-muted-foreground">
    <a href="#">Item 2</a>
  </li>
  <li class="bg-muted p-4 text-muted-foreground">
    <a href="#">Item 3</a>
  </li>
  <li class="bg-muted p-4 text-muted-foreground">
    <a href="#">Item 4</a>
  </li>
</ul>
```

## Component options

Any of these options can be applied to the component attribute. Separate multiple options with a semicolon. [Learn more](https://franken-ui.dev/docs/2.1/javascript#component-configuration)

| Option            | Value           | Default                   | Description                                   |
| ----------------- | --------------- | ------------------------- | --------------------------------------------- |
| `group`           | String          |                           | The group                                     |
| `animation`       | String, Boolean | `slide`                   | Animation mode (`slide`, `false`).            |
| `duration`        | Number          | `250`                     | Animation duration in milliseconds.           |
| `threshold`       | Number          | `5`                       | Mouse move threshold before dragging starts.  |
| `cls-item`        | String          | `uk-sortable-item`        | The item class.                               |
| `cls-placeholder` | String          | `uk-sortable-placeholder` | The placeholder class.                        |
| `cls-drag`        | String          | `uk-sortable-drag`        | The ghost class.                              |
| `cls-drag-state`  | String          | `uk-drag`                 | The body's dragging class.                    |
| `cls-base`        | String          | `uk-sortable`             | The list's class.                             |
| `cls-no-drag`     | String          | `uk-sortable-nodrag`      | Disable dragging on elements with this class. |
| `cls-empty`       | String          | `uk-sortable-empty`       | The empty list class.                         |
| `cls-custom`      | String          |                           | The ghost's custom class.                     |
| `handle`          | String          | `false`                   | The handle selector.                          |

## JavaScript

Learn more about [JavaScript components](https://franken-ui.dev/docs/2.1/javascript#programmatic-use).

### Initialization

```javascript
UIkit.sortable(element, options);
```

### Events

The following events will be triggered on elements with this component attached:

| Name      | Description                              |
| --------- | ---------------------------------------- |
| `start`   | Fires after dragging starts.             |
| `stop`    | Fires after dragging stops.              |
| `moved`   | Fires after an element has been moved.   |
| `added`   | Fires after an element has been added.   |
| `removed` | Fires after an element has been removed. |
