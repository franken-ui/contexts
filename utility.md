## Overflow

These utilities provide different classes to modify an element's overflow behavior.

| Class                 | Description                                                                                                                                                           |
| --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `.uk-overflow-hidden` | Add this class to clip content that exceeds the dimensions of its container.                                                                                          |
| `.uk-overflow-auto`   | Add this class to create a container that provides a horizontal or vertical scrollbar whenever the elements content it are wider or higher than the container itself. |

Note: The `.uk-overflow-auto` class is useful when having to handle tables on a responsive website, which at some point would just get too big. It also works great on `<pre>` elements.

### Overflow Auto

Add the `uk-overflow-auto` attribute to expand an element's height to make it fill the remaining height of a parent container. It provides a vertical scrollbar if its content is higher than the expanded height.

### Example

```html
<div class="h-80">
  <div class="js-wrapper space-y-4">
    <p>Some content before the overflow auto container.</p>

    <div uk-overflow-auto="selContainer: .h-80; selContent: .js-wrapper">
      <div class="grid grid-cols-2 gap-4">
        <div>
          <img src="/images/light.jpg" width="1800" height="1200" alt="" />
        </div>
        <div>
          <img src="/images/dark.jpg" width="1800" height="1200" alt="" />
        </div>
        <div>
          <img src="/images/photo.jpg" width="1800" height="1200" alt="" />
        </div>
        <div>
          <img src="/images/photo2.jpg" width="1800" height="1200" alt="" />
        </div>
      </div>
    </div>

    <p>Some content after the overflow auto container.</p>
  </div>
</div>
```

It's often used within the [Modal component](https://franken-ui.dev/docs/2.1/modal).

```html
<div id="my-id" uk-modal>
  <div class="uk-modal-dialog" uk-overflow-auto></div>
</div>
```

### Example

```html
<a class="uk-btn uk-btn-default" href="#modal-overflow" data-uk-toggle>
  Open
</a>

<div id="modal-overflow" data-uk-modal>
  <div class="uk-modal-dialog">
    <button
      class="uk-modal-close absolute right-4 top-4"
      type="button"
      data-uk-close
    ></button>

    <div class="uk-modal-header">
      <h2 class="uk-modal-title">Headline</h2>
    </div>

    <div class="uk-modal-body space-y-4" data-uk-overflow-auto>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
        commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
        velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
        occaecat cupidatat non proident, sunt in culpa qui officia deserunt
        mollit anim id est laborum.
      </p>
    </div>

    <div class="uk-modal-footer uk-text-right">
      <button class="uk-modal-close uk-btn uk-btn-default mr-2" type="button">
        Cancel
      </button>
      <button class="uk-btn uk-btn-primary" type="button">Save</button>
    </div>
  </div>
</div>
```

You can change the target heights by adding the `selContainer` and `selContent` options to the attribute. [Learn more](https://franken-ui.dev/docs/2.1/javascript#component-configuration)

| Option          | Value  | Default            | Description                                                                       |
| --------------- | ------ | ------------------ | --------------------------------------------------------------------------------- |
| `sel-container` | String | `.uk-modal`        | CSS selector for the container element which provides the height.                 |
| `sel-content`   | String | `.uk-modal-dialog` | CSS selector for the element which wraps the inner content to provide its height. |

## Resize

These utilities provide different classes for resizing elements.

| Class                 | Description                                                |
| --------------------- | ---------------------------------------------------------- |
| `.uk-resize`          | Add this class to enable horizontal and vertical resizing. |
| `.uk-resize-vertical` | Add this class to enable only vertical resizing.           |

Grab and drag the bottom right corner of each box below to resize it.

### Example

```html
<div class="grid grid-cols-2 gap-4">
  <div>
    <pre
      class="uk-resize-vertical overflow-auto bg-muted font-geist-mono text-muted-foreground"
    >
            <code>
&lt;!-- Resize vertically --&gt;
&lt;div uk-grid&gt;
    &lt;div class="uk-width-1-2"&gt;…&lt;/div&gt;
    &lt;div class="uk-width-1-2"&gt;…&lt;/div&gt;
&lt;/div&gt;

&lt;div class="uk-child-width-1-2" uk-grid&gt;
    &lt;div&gt;&lt;/div&gt;
    &lt;div&gt;&lt;/div&gt;
&lt;/div&gt;
            </code>
        </pre>
  </div>
  <div>
    <pre
      class="uk-resize overflow-auto bg-muted font-geist-mono text-muted-foreground"
    >
            <code>
&lt;!-- Resize horizontally and vertically --&gt;
&lt;div uk-grid&gt;
    &lt;div class="uk-width-1-2"&gt;…&lt;/div&gt;
    &lt;div class="uk-width-1-2"&gt;…&lt;/div&gt;
&lt;/div&gt;

&lt;div class="uk-child-width-1-2" uk-grid&gt;
    &lt;div&gt;&lt;/div&gt;
    &lt;div&gt;&lt;/div&gt;
&lt;/div&gt;
            </code>
        </pre>
  </div>
</div>
```

## Inline

These classes are often used to create a position context on containers with an image as a child. The container keeps the same size as the image as well as the responsive behavior. That way content that is placed on top of the image with the [Position component](https://franken-ui.dev/docs/2.1/position) will not flow out of the image dimensions.

| Class             | Description                                                                                                            |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `.uk-inline`      | Add this class to apply inline-block behavior to an element, add a max-width of 100% and to create a position context. |
| `.uk-inline-clip` | Same as `.uk-inline`, it but also clips overflowing child elements.                                                    |

```html
<div class="uk-inline">
  <img src="" width="" height="" alt="" />
  <div class="uk-position-cover"></div>
</div>
```

### Example

```html
<div class="uk-inline">
  <img src="/images/photo.jpg" width="300" height="200" alt="" />
  <div
    class="uk-position-cover uk-position-sm flex items-center justify-center bg-white/80"
  >
    Overlay
  </div>
</div>
```

## Responsive objects

In UIkit `<img>`, `<canvas>`, `<audio>` and `<video>` elements adapt to the width of their parent container by default. To apply responsive behavior to iframes, add the `uk-responsive` attribute . For other elements or to apply a different behavior, just add one of the following classes.

| Class                   | Description                                                                                                                                                                                                                                                                                                |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `.uk-responsive-width`  | Add this class to apply the same responsive behavior to any other element. It adjusts the object's width according to its parent's width, keeping the original aspect ratio.                                                                                                                               |
| `.uk-responsive-height` | Add this class to adjust the object's height (instead of its width) according to its parent's height, keeping the original aspect ratio.                                                                                                                                                                   |
| `.uk-preserve-width`    | Add this class to avoid the default responsive behavior and preserve the original image dimensions. You can also add the class to a parent element and it will be applied to all relevant elements content it. If you are embedding Google Maps into your site, you may need this to fix the map's images. |

```html
<img class="uk-responsive-height" src="" width="" height="" alt="" />

<iframe src="" width="" height="" uk-responsive></iframe>
```

## Border radius

To modify the border radius of an element, like an image, add one of the following classes.

| Class            | Description                                    |
| ---------------- | ---------------------------------------------- |
| `.uk-rounded-sm` | Add this class to apply a small border radius. |
| `.uk-rounded`    | Add this class to apply a border radius.       |

### Example

```html
<div class="grid grid-cols-2 gap-4">
  <div class="uk-rounded-sm border border-border p-4">
    <p class="text-center">Small</p>
  </div>
  <div class="uk-rounded border border-border p-4">
    <p class="text-center">Medium</p>
  </div>
</div>
```

## Box shadow

You can apply different box shadows to elements. Just add one of the following classes.

| Class           | Description                                 |
| --------------- | ------------------------------------------- |
| `.uk-shadow-sm` | Add this class to apply a small box shadow. |
| `.uk-shadow`    | Add this class to apply a box shadow.       |

```html
<div class="uk-shadow-sm"></div>
```

### Example

```html
<div class="grid grid-cols-2 gap-4">
  <div class="uk-shadow-sm border border-border p-4">
    <p class="text-center">Small</p>
  </div>
  <div class="uk-shadow border border-border p-4">
    <p class="text-center">Medium</p>
  </div>
</div>
```

## Drop cap

With the `.uk-dropcap` class you can achieve a drop cap within a text by adding it directly to the `<p>` element.

### Example

```html
<p class="uk-dropcap">
  Dorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
  incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
  nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
  Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore
  eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt
  in culpa qui officia deserunt mollit anim id est laborum. Lorem ipsum dolor
  sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
  labore et dolore magna aliqua.
</p>
```

## Transform center

To center an element to itself, add the `uk-transform-center` class. This is particularly useful for absolute positioning.

### Example

```html
<div class="uk-inline">
  <img src="/images/light.jpg" width="1800" height="1200" alt="" />
  <a
    class="uk-btn uk-btn-primary uk-btn-icon uk-position-absolute uk-transform-center"
    style="left: 50%; top: 50%"
  >
    <uk-icon icon="plus"></uk-icon>
  </a>
</div>
```

## Transform origin

To modify the origin of an animation, like scaling, add one of the `uk-transform-origin-*` classes. This can be combined with the [Animation component](https://franken-ui.dev/docs/2.1/animation).

| Class                                | Description                                      |
| ------------------------------------ | ------------------------------------------------ |
| `.uk-transform-origin-top-left`      | The transition originates from the top left.     |
| `.uk-transform-origin-top-center`    | The transition originates from the top.          |
| `.uk-transform-origin-top-right`     | The transition originates from the top right.    |
| `.uk-transform-origin-center-left`   | The transition originates from the left.         |
| `.uk-transform-origin-center-right`  | The transition originates from the right.        |
| `.uk-transform-origin-bottom-left`   | The transition originates from the bottom left.  |
| `.uk-transform-origin-bottom-center` | The transition originates from the bottom.       |
| `.uk-transform-origin-bottom-right`  | The transition originates from the bottom right. |

```html
<div class="uk-animation-scale-up uk-transform-origin-bottom-right"></div>
```

### Example

```html
<div class="grid gap-4 md:grid-cols-3">
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-scale-up uk-transform-origin-bottom-right bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Bottom Right</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-scale-up uk-transform-origin-top-center bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Top Center</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-scale-up uk-transform-origin-bottom-center bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Bottom Center</p>
    </div>
  </div>
</div>
```

## Disabled

To disable the click behavior of any element, like a `<a>`, `<button>` or `<iframe>` element, add the `.uk-disabled` class.

### Example

```html
<a class="uk-disabled uk-btn uk-btn-default" href="#">Disabled</a>
```
