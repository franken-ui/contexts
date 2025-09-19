## Cover

To have an image cover its parent element, add the `.uk-cover-container` class to the parent and the `data-uk-cover` attribute to the image.

```html
<div class="uk-cover-container">
  <img src="" alt="" data-uk-cover />
</div>
```

Note: To position content on top of the covering element, use the [Position component](https://franken-ui.dev/docs/2.1/position).

### Example

```html
<div class="uk-cover-container h-80">
  <img src="/images/dark.jpg" alt="" data-uk-cover />
</div>
```

## Video

To create a video that covers its parent container, add the `data-uk-cover` attribute to a video. Wrap a container element around the video and add the `.uk-cover-container` class to clip the content.

The Cover component inherits all properties from the [Video component](https://franken-ui.dev/docs/2.1/video) which means videos are muted and play automatically. The video will pause whenever it's not visible and resume once it becomes visible again.

```html
<div class="uk-cover-container">
  <video data-uk-cover></video>
</div>
```

### Example

```html
<div class="uk-cover-container h-80">
  <video
    src="http://commondatastorage.googleapis.com/gtv-videos-bucket/sample/BigBuckBunny.mp4"
    loop
    muted
    playsinline
    data-uk-cover
  ></video>
</div>
```

## Iframe

To apply the Cover component to an iframe, you need to add the `data-uk-cover` attribute to the iframe. Now add the `.uk-cover-container` class to a container element around the iframe to clip the content.

```html
<div class="uk-cover-container">
  <iframe src="" data-uk-cover></iframe>
</div>
```

### Example

```html
<div class="uk-cover-container h-80">
  <iframe
    src="https://www.youtube-nocookie.com/embed/aqz-KE-bpKQ?autoplay=1&amp;controls=0&amp;showinfo=0&amp;rel=0&amp;loop=1&amp;modestbranding=1&amp;wmode=transparent"
    width="1920"
    height="1080"
    allowfullscreen
    data-uk-cover
  ></iframe>
</div>
```

## Responsive height

To add responsive behavior to your cover image, you need to create an invisible `<canvas>` element and assign `width` and `height` values to it, according to the aspect ratio you want the covered area to have. That way it will adapt the responsive behavior of the image.

```html
<div class="uk-cover-container">
  <canvas width="" height=""></canvas>
  <img src="" alt="" data-uk-cover />
</div>
```

### Example

```html
<div class="uk-cover-container">
  <canvas width="400" height="200"></canvas>
  <img src="/images/dark.jpg" alt="" data-uk-cover />
</div>
```

## Component options

Any of these options can be applied to the component attribute. Separate multiple options with a semicolon. [Learn more](https://franken-ui.dev/docs/2.1/javascript#component-configuration)

| Option     | Value   | Default | Description                           |
| ---------- | ------- | ------- | ------------------------------------- |
| `automute` | Boolean | true    | Tries to automute the iframe's video. |
| `width`    | Number  |         | The element's width.                  |
| `height`   | Number  |         | The element's height.                 |

## JavaScript

Learn more about [JavaScript components](https://franken-ui.dev/docs/2.1/javascript).

### Initialization

```javascript
UIkit.cover(element, options);
```
