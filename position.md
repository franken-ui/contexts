## Position

To apply this component, add one of the `.uk-position-*` classes to a block element. When using this component to place content on top of an image, add the `.uk-inline` class to a container element around the image and the element to create a position context.

| Class                 | Description                          |
| --------------------- | ------------------------------------ |
| `.uk-position-top`    | Positions the element at the top.    |
| `.uk-position-left`   | Positions the element at the left.   |
| `.uk-position-right`  | Positions the element at the right.  |
| `.uk-position-bottom` | Positions the element at the bottom. |

```html
<div class="uk-inline">
  <!-- Place any content, like an image, here -->

  <div class="uk-position-center"></div>
</div>
```

### Example

```html
<div class="uk-margin uk-inline">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div class="uk-position-top bg-white/80 p-4 text-center">Top</div>
  <div class="uk-position-bottom bg-white/80 p-4 text-center">Bottom</div>
  <div class="uk-position-left flex items-center bg-white/80 p-4">Left</div>
  <div class="uk-position-right flex items-center bg-white/80 p-4">Right</div>
</div>
```

### X and Y directions

You can also apply more specific positions that won't spread over one side of the parent container by adding one of the following classes.

| Class                        | Description                                              |
| ---------------------------- | -------------------------------------------------------- |
| `.uk-position-top-left`      | Positions the element at the top left.                   |
| `.uk-position-top-center`    | Positions the element at the top center.                 |
| `.uk-position-top-right`     | Positions the element at the top right.                  |
| `.uk-position-center`        | Positions the element vertically centered in the middle. |
| `.uk-position-center-left`   | Positions the element vertically centered on the left.   |
| `.uk-position-center-right`  | Positions the element vertically centered on the right.  |
| `.uk-position-bottom-left`   | Positions the element at the bottom left.                |
| `.uk-position-bottom-center` | Positions the element at the bottom center.              |
| `.uk-position-bottom-right`  | Positions the element at the bottom right.               |

```html
<div class="uk-position-top-right"></div>
```

### Example

```html
<div class="uk-inline">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div class="uk-position-top-left bg-white/80 p-4">Top Left</div>
  <div class="uk-position-top-center bg-white/80 p-4">Top Center</div>
  <div class="uk-position-top-right bg-white/80 p-4">Top Right</div>
  <div class="uk-position-center-left bg-white/80 p-4">Center Left</div>
  <div class="uk-position-center bg-white/80 p-4">Center</div>
  <div class="uk-position-center-right bg-white/80 p-4">Center Right</div>
  <div class="uk-position-bottom-left bg-white/80 p-4">Bottom Left</div>
  <div class="uk-position-bottom-center bg-white/80 p-4">Bottom Center</div>
  <div class="uk-position-bottom-right bg-white/80 p-4">Bottom Right</div>
</div>
```

### Center

You can also apply more specific positions that won't spread over one side of the parent container by adding one of the following classes.

| Class                            | Description                                             |
| -------------------------------- | ------------------------------------------------------- |
| `.uk-position-center-horizontal` | Positions the element at the center from top to bottom. |
| `.uk-position-center-vertical`   | Positions the element at the center from left to right. |

```html
<div class="uk-position-center-horizontal"></div>
```

### Example

```html
<div class="uk-inline">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div class="uk-position-center-horizontal bg-white/80 p-4">Horizontal</div>
  <div class="uk-position-center-vertical bg-white/80 p-4">Vertical</div>
</div>
```

### Cover

If you want a position element to cover its container, just add the `.uk-position-cover` class.

```html
<div class="uk-position-cover"></div>
```

### Example

```html
<div class="uk-inline">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div
    class="uk-position-cover flex items-center justify-center bg-white/80 p-4"
  >
    Cover
  </div>
</div>
```

### Outside

There are two classes to center elements outside on the left and right of the parent container. This is useful to position the [Slidenav component](https://franken-ui.dev/docs/2.1/slidenav) outside of a [Slideshow](https://franken-ui.dev/docs/2.1/slideshow) or [Slider](https://franken-ui.dev/docs/2.1/slider) component.

| Class                           | Description                                                     |
| ------------------------------- | --------------------------------------------------------------- |
| `.uk-position-center-left-out`  | Positions the element vertically centered outside on the left.  |
| `.uk-position-center-right-out` | Positions the element vertically centered outside on the right. |

Note: Once the outside positioned element sticks out of the viewport to the right, it will cause a horizontal scrollbar. You can use the visibility utility classes to hide the outside positioned element on a smaller viewports and show an inside positioned element instead.

```html
<div class="uk-position-center-left-out"></div>
```

### Example

```html
<div class="mx-auto w-3/4">
  <div class="uk-inline">
    <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

    <div class="uk-position-center-left-out bg-black/80 p-4 text-white">
      Out
    </div>
    <div class="uk-position-center-right-out bg-black/80 p-4 text-white">
      Out
    </div>
  </div>
</div>
```

## Small modifier

To apply a small margin to positioned elements, add the `.uk-position-sm` class.

```html
<div class="uk-position-center uk-position-sm"></div>
```

### Example

```html
<div class="uk-inline">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div class="uk-position-top-left uk-position-sm bg-white/80 p-4">
    Top Left
  </div>
  <div class="uk-position-top-center uk-position-sm bg-white/80 p-4">
    Top Center
  </div>
  <div class="uk-position-top-right uk-position-sm bg-white/80 p-4">
    Top Right
  </div>
  <div class="uk-position-center-left uk-position-sm bg-white/80 p-4">
    Center Left
  </div>
  <div class="uk-position-center uk-position-sm bg-white/80 p-4">Center</div>
  <div class="uk-position-center-right uk-position-sm bg-white/80 p-4">
    Center Right
  </div>
  <div class="uk-position-bottom-left uk-position-sm bg-white/80 p-4">
    Bottom Left
  </div>
  <div class="uk-position-bottom-center uk-position-sm bg-white/80 p-4">
    Bottom Center
  </div>
  <div class="uk-position-bottom-right uk-position-sm bg-white/80 p-4">
    Bottom Right
  </div>
</div>

<div class="uk-inline mt-4">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div class="uk-position-toptext-center uk-position-sm bg-white/80 p-4">
    Top
  </div>
  <div class="uk-position-bottomtext-center uk-position-sm bg-white/80 p-4">
    Bottom
  </div>
  <div
    class="uk-position-left uk-position-sm flex items-center bg-white/80 p-4"
  >
    Left
  </div>
  <div
    class="uk-position-right uk-position-sm flex items-center bg-white/80 p-4"
  >
    Right
  </div>
</div>

<div class="uk-inline mt-4">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div
    class="uk-position-cover uk-position-sm flex items-center justify-center bg-white/80 p-4"
  >
    Cover
  </div>
</div>

<div class="mx-auto mt-4 w-3/4">
  <div class="uk-inline">
    <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

    <div
      class="uk-position-center-left-out uk-position-sm bg-black/80 p-4 text-white"
    >
      Out
    </div>
    <div
      class="uk-position-center-right-out uk-position-sm bg-black/80 p-4 text-white"
    >
      Out
    </div>
  </div>
</div>
```

## Medium modifier

To apply a medium margin to positioned elements, add the `.uk-position-md` class.

```html
<div class="uk-position-center uk-position-md"></div>
```

### Example

```html
<div class="uk-inline">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div class="uk-position-top-left uk-position-md bg-white/80 p-4">
    Top Left
  </div>
  <div class="uk-position-top-center uk-position-md bg-white/80 p-4">
    Top Center
  </div>
  <div class="uk-position-top-right uk-position-md bg-white/80 p-4">
    Top Right
  </div>
  <div class="uk-position-center-left uk-position-md bg-white/80 p-4">
    Center Left
  </div>
  <div class="uk-position-center uk-position-md bg-white/80 p-4">Center</div>
  <div class="uk-position-center-right uk-position-md bg-white/80 p-4">
    Center Right
  </div>
  <div class="uk-position-bottom-left uk-position-md bg-white/80 p-4">
    Bottom Left
  </div>
  <div class="uk-position-bottom-center uk-position-md bg-white/80 p-4">
    Bottom Center
  </div>
  <div class="uk-position-bottom-right uk-position-md bg-white/80 p-4">
    Bottom Right
  </div>
</div>

<div class="uk-inline mt-4">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div class="uk-position-toptext-center uk-position-md bg-white/80 p-4">
    Top
  </div>
  <div class="uk-position-bottomtext-center uk-position-md bg-white/80 p-4">
    Bottom
  </div>
  <div
    class="uk-position-left uk-position-md flex items-center bg-white/80 p-4"
  >
    Left
  </div>
  <div
    class="uk-position-right uk-position-md flex items-center bg-white/80 p-4"
  >
    Right
  </div>
</div>

<div class="uk-inline mt-4">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div
    class="uk-position-cover uk-position-md flex items-center justify-center bg-white/80 p-4"
  >
    Cover
  </div>
</div>

<div class="mx-auto mt-4 w-3/4">
  <div class="uk-inline">
    <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

    <div
      class="uk-position-center-left-out uk-position-md bg-black/80 p-4 text-white"
    >
      Out
    </div>
    <div
      class="uk-position-center-right-out uk-position-md bg-black/80 p-4 text-white"
    >
      Out
    </div>
  </div>
</div>
```

## Large modifier

To apply a large margin to positioned elements, add the `.uk-position-lg` class.

```html
<div class="uk-position-lg uk-position-center"></div>
```

### Example

```html
<div class="uk-inline">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div class="uk-position-top-left uk-position-lg bg-white/80 p-4">
    Top Left
  </div>
  <div class="uk-position-top-center uk-position-lg bg-white/80 p-4">
    Top Center
  </div>
  <div class="uk-position-top-right uk-position-lg bg-white/80 p-4">
    Top Right
  </div>
  <div class="uk-position-center-left uk-position-lg bg-white/80 p-4">
    Center Left
  </div>
  <div class="uk-position-center uk-position-lg bg-white/80 p-4">Center</div>
  <div class="uk-position-center-right uk-position-lg bg-white/80 p-4">
    Center Right
  </div>
  <div class="uk-position-bottom-left uk-position-lg bg-white/80 p-4">
    Bottom Left
  </div>
  <div class="uk-position-bottom-center uk-position-lg bg-white/80 p-4">
    Bottom Center
  </div>
  <div class="uk-position-bottom-right uk-position-lg bg-white/80 p-4">
    Bottom Right
  </div>
</div>

<div class="uk-inline mt-4">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div class="uk-position-toptext-center uk-position-lg bg-white/80 p-4">
    Top
  </div>
  <div class="uk-position-bottomtext-center uk-position-lg bg-white/80 p-4">
    Bottom
  </div>
  <div
    class="uk-position-left uk-position-lg flex items-center bg-white/80 p-4"
  >
    Left
  </div>
  <div
    class="uk-position-right uk-position-lg flex items-center bg-white/80 p-4"
  >
    Right
  </div>
</div>

<div class="uk-inline mt-4">
  <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

  <div
    class="uk-position-cover uk-position-lg flex items-center justify-center bg-white/80 p-4"
  >
    Cover
  </div>
</div>

<div class="mx-auto mt-4 w-1/2">
  <div class="uk-inline">
    <img src="/images/photo.jpg" width="1800" height="1200" alt="" />

    <div
      class="uk-position-center-left-out uk-position-lg bg-black/80 p-4 text-white"
    >
      Out
    </div>
    <div
      class="uk-position-center-right-out uk-position-lg bg-black/80 p-4 text-white"
    >
      Out
    </div>
  </div>
</div>
```

## Utility classes

This component features a number of general position utility classes:

| Class                   | Description                                   |
| ----------------------- | --------------------------------------------- |
| `.uk-position-relative` | Add this class to apply relative positioning. |
| `.uk-position-absolute` | Add this class to apply absolute positioning. |
| `.uk-position-fixed`    | Add this class to apply fixed positioning.    |
| `.uk-position-z-index`  | Add this class to apply a z-index of 1.       |
