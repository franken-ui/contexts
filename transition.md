## Transition

To toggle a transition on hover or focus, add the `.uk-transition-toggle` class to a parent element. Also add `tabindex="0"` to make the animation focusable through keyboard navigation and on touch devices. Add one of the `.uk-transition-*` classes to any child element to apply the actual effect.

| Class                                                                                                                                           | Description                                                                        |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `.uk-transition-fade`                                                                                                                           | Lets the element fade in                                                           |
| `.uk-transition-scale-up`<br /> `.uk-transition-scale-down`                                                                                     | The element scales up or down.                                                     |
| `.uk-transition-slide-top`<br /> `.uk-transition-slide-bottom`<br /> `.uk-transition-slide-left`<br /> `.uk-transition-slide-right`             | Lets the element slide in from the top                                             |
| `.uk-transition-slide-top-sm`<br /> `.uk-transition-slide-bottom-sm`<br /> `.uk-transition-slide-left-sm`<br /> `.uk-transition-slide-right-sm` | The element slides in from the top, bottom, left or right with a smaller distance. |
| `.uk-transition-slide-top-md`<br /> `.uk-transition-slide-bottom-md`<br /> `.uk-transition-slide-left-md`<br /> `.uk-transition-slide-right-md` | The element slides in from the top, bottom, left or right with a medium distance.  |

```html
<div class="uk-transition-toggle" tabindex="0">
  <div class="uk-transition-fade"></div>
</div>
```

### Example

```html
<div class="grid grid-cols-2 gap-4 sm:grid-cols-3">
  <div class="text-center">
    <div class="uk-transition-toggle uk-inline-clip" tabindex="0">
      <img src="/images/dark.jpg" width="1800" height="1200" alt="" />
      <div
        class="uk-position-cover uk-position-sm uk-transition-fade bg-white/80 p-4"
      >
        <p class="uk-h4">Fade</p>
      </div>
    </div>
    <p class="uk-h3 mt-4">Fade</p>
  </div>
  <div class="text-center">
    <div class="uk-transition-toggle uk-inline-clip" tabindex="0">
      <img src="/images/dark.jpg" width="1800" height="1200" alt="" />
      <div
        class="uk-position-bottom uk-transition-slide-bottom bg-white/80 p-4"
      >
        <p class="uk-h4">Bottom</p>
      </div>
    </div>
    <p class="uk-h3 mt-4">Bottom</p>
  </div>
  <div class="text-center">
    <div class="uk-transition-toggle uk-inline-clip" tabindex="0">
      <img src="/images/dark.jpg" width="1800" height="1200" alt="" />
      <div class="uk-position-center">
        <span class="uk-transition-fade text-white">
          <uk-icon icon="plus"></uk-icon>
        </span>
      </div>
    </div>
    <p class="uk-h3 mt-4">Icon</p>
  </div>
  <div class="text-center">
    <div class="uk-transition-toggle uk-inline-clip" tabindex="0">
      <img src="/images/dark.jpg" width="1800" height="1200" alt="" />
      <img
        class="uk-position-cover uk-transition-scale-up"
        src="/images/light.jpg"
        alt=""
      />
    </div>
    <p class="uk-h3 mt-4">2 Images</p>
  </div>
  <div class="text-center">
    <div class="uk-transition-toggle uk-inline-clip" tabindex="0">
      <img
        class="uk-transition-scale-up uk-transition-opaque"
        src="/images/dark.jpg"
        width="1800"
        height="1200"
        alt=""
      />
    </div>
    <p class="uk-h3 mt-4">Scale Up Image</p>
  </div>
  <div class="text-center">
    <div class="uk-transition-toggle uk-inline-clip" tabindex="0">
      <img src="/images/dark.jpg" width="1800" height="1200" alt="" />
      <div class="uk-position-center">
        <div class="uk-transition-slide-top-sm">
          <h4 class="text-white">Headline</h4>
        </div>
        <div class="uk-transition-slide-bottom-sm">
          <h4 class="text-white">Subheadline</h4>
        </div>
      </div>
    </div>
    <p class="uk-h3 mt-4">Small Top + Bottom</p>
  </div>
</div>
```
