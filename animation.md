## Animation

Add one of the `.uk-anmt-*` classes to any element. The animation is shown when the class is added, so usually immediately on page load. To show the animation at another point, for example when the element enters the viewport, you would add the class using JavaScript — with the [Scrollspy component](https://franken-ui.dev/docs/2.1/scrollspy) for instance. This is what happens in many of UIkit's components that make use of animations. All animations themselves are implemented with CSS, so they do not require JavaScript to play.

| Class                                                                                                                | Description                                                                                                                            |
| -------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| `.uk-anmt-fade`                                                                                                      | The element fades in.                                                                                                                  |
| `.uk-anmt-scale-up`<br/> `.uk-anmt-scale-down`                                                                       | The element fades in and scales up or down.                                                                                            |
| `.uk-anmt-slide-top`<br/> `.uk-anmt-slide-bottom`<br/> `.uk-anmt-slide-left`<br/> `.uk-anmt-slide-right`             | The element fades and slides in from the top, bottom, left or right by its own height or width.                                        |
| `.uk-anmt-slide-top-sm`<br/> `.uk-anmt-slide-bottom-sm`<br/> `.uk-anmt-slide-left-sm`<br/> `.uk-anmt-slide-right-sm` | The element fades and slides in from the top, bottom, left or right with a smaller distance which is specified by a fixed pixel value. |
| `.uk-anmt-slide-top-md`<br/> `.uk-anmt-slide-bottom-md`<br/> `.uk-anmt-slide-left-md`<br/> `.uk-anmt-slide-right-md` | The element fades and slides in from the top, bottom, left or right with a medium distance which is specified by a fixed pixel value.  |
| `.uk-anmt-kenburns`                                                                                                  | The element scales very slowly up without fading in.                                                                                   |
| `.uk-anmt-shake`                                                                                                     | The element shakes.                                                                                                                    |
| `.uk-anmt-stroke`                                                                                                    | The SVG element strokes are drawn.                                                                                                     |

To toggle an animation on hover or focus, add the `.uk-anmt-toggle` class to a parent element. Also add `tab to make the animation focusable through keyboard navigation and on touch devices.

```html
<div class="uk-anmt-toggle" tabindex="0">
  <div class="uk-anmt-fade"></div>
</div>
```

### Example

```html
<div class="grid grid-cols-2 gap-4">
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-fade bg-muted p-4 text-muted-foreground">
      <p class="text-center">Fade</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-scale-up bg-muted p-4 text-muted-foreground">
      <p class="text-center">Scale Up</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-scale-down bg-muted p-4 text-muted-foreground">
      <p class="text-center">Scale Down</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-shake bg-muted p-4 text-muted-foreground">
      <p class="text-center">Shake</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-left bg-muted p-4 text-muted-foreground">
      <p class="text-center">Left</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-top bg-muted p-4 text-muted-foreground">
      <p class="text-center">Top</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-bottom bg-muted p-4 text-muted-foreground">
      <p class="text-center">Bottom</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-right bg-muted p-4 text-muted-foreground">
      <p class="text-center">Right</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-left-sm bg-muted p-4 text-muted-foreground">
      <p class="text-center">Left Small</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-top-sm bg-muted p-4 text-muted-foreground">
      <p class="text-center">Top Small</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-bottom-sm bg-muted p-4 text-muted-foreground">
      <p class="text-center">Bottom Small</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-right-sm bg-muted p-4 text-muted-foreground">
      <p class="text-center">Right Small</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-left-md bg-muted p-4 text-muted-foreground">
      <p class="text-center">Left Medium</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-top-md bg-muted p-4 text-muted-foreground">
      <p class="text-center">Top Medium</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-bottom-md bg-muted p-4 text-muted-foreground">
      <p class="text-center">Bottom Medium</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-slide-right-md bg-muted p-4 text-muted-foreground">
      <p class="text-center">Right Medium</p>
    </div>
  </div>
</div>
```

## Reverse modifier

By default, all animations are incoming. To reverse any animation, add the `.uk-anmt-reverse` class.

```html
<div class="uk-anmt-fade uk-anmt-reverse"></div>
```

### Example

```html
<div class="grid grid-cols-2 gap-4">
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-fade uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Fade</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-scale-up uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Scale Up</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-scale-down uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Scale Down</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-shake uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Shake</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-left uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Left</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-top uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Top</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-bottom uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Bottom</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-right uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Right</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-left-sm uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Left Small</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-top-sm uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Top Small</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-bottom-sm uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Bottom Small</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-right-sm uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Right Small</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-left-md uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Left Medium</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-top-md uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Top Medium</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-bottom-md uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Bottom Medium</p>
    </div>
  </div>
  <div class="uk-anmt-toggle" tabindex="0">
    <div
      class="uk-anmt-slide-right-md uk-anmt-reverse bg-muted p-4 text-muted-foreground"
    >
      <p class="text-center">Right Medium</p>
    </div>
  </div>
</div>
```

## Fast modifier

To play animations at a faster speed, add the `.uk-anmt-fast` class to the element.

```html
<div class="uk-anmt-fade uk-anmt-fast"></div>
```

### Example

```html
<div class="grid grid-cols-2 gap-4">
  <div class="uk-anmt-toggle" tabindex="0">
    <div class="uk-anmt-fade uk-anmt-fast bg-muted p-4 text-muted-foreground">
      <p class="text-center">Fade</p>
    </div>
  </div>
</div>
```

## Origin modifiers

By default, scaling animations originate from the center. To modify this behavior, add one of the `.uk-transform-origin-*` classes.

```html
<div class="uk-anmt-scale-up uk-transform-origin-bottom-right"></div>
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

## Ken Burns

To add a simple Ken Burns effect, add the `.uk-anmt-kenburns` class to any image. You can also apply the `.uk-anmt-reverse` or one of the `.uk-transform-origin-*` classes to modify the effect.

```html
<img class="uk-anmt-kenburns" src="" width="" height="" alt="" />
```

By default, the animation starts on page load. In this example we used the [Scrollspy](https://franken-ui.dev/docs/2.1/scrollspy) component, to toggle the effect when the image enters the view.

### Example

```html
<div class="grid gap-4 md:grid-cols-2">
  <div>
    <div class="uk-overflow-hidden">
      <img
        src="/images/dark.jpg"
        width="1800"
        height="1200"
        alt="Example image"
        data-uk-scrollspy="cls: uk-anmt-kenburns; repeat: true"
      />
    </div>
  </div>
  <div>
    <div class="uk-overflow-hidden">
      <img
        src="/images/dark.jpg"
        width="1800"
        height="1200"
        alt="Example image"
        class="uk-anmt-reverse uk-transform-origin-top-right"
        data-uk-scrollspy="cls: uk-anmt-kenburns; repeat: true"
      />
    </div>
  </div>
</div>
```

## SVG Strokes

The Animation component can be used to animate SVG strokes. The effect looks like the SVG strokes are drawn before your eyes. The SVG image has to be injected into the markup as an inline SVG. This can be done manually or using the [SVG component](https://franken-ui.dev/docs/2.1/svg).

The following example shows how to add the inline SVG manually. Since you have to know the exact length of the stroke, UIkit requires you to set the length in the custom property `--uk-anmt-stroke`. In this example the stroke length is `46`.

```html
<svg
  class="uk-anmt-stroke"
  style="--uk-anmt-stroke: 46;"
  viewBox="0 0 20 20"
  xmlns="http://www.w3.org/2000/svg"
>
  <path fill="none" stroke="#000" stroke-width="1" d="" />
</svg>
```

A much easier way is to use the [SVG component](https://franken-ui.dev/docs/2.1/svg) by adding `uk-svg="stroke-animation: true"` to the image element. It will calculate the stroke length and add the `--uk-anmt-stroke` custom property automatically.

```html
<img src="" width="" height="" alt="" data-uk-svg="stroke-animation: true" />
```

### Example

```html
<div class="grid gap-4 md:grid-cols-2">
  <div class="uk-anmt-toggle flex justify-center" tabindex="0">
    <img
      class="uk-anmt-stroke"
      src="/images/strokes.svg"
      width="250"
      height="250"
      alt=""
      data-uk-svg="stroke-animation: true"
    />
  </div>
  <div class="uk-anmt-toggle flex justify-center" tabindex="0">
    <img
      class="uk-anmt-stroke uk-anmt-reverse"
      src="/images/strokes.svg"
      width="250"
      height="250"
      alt=""
      data-uk-svg="stroke-animation: true"
    />
  </div>
</div>
```
