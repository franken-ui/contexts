## Avatar

To get started with the Avatar component, simply wrap your image inside the `.uk-avatar` and `.uk-avatar-image` classes.

### Example

```html
<div class="flex justify-center">
  <div class="uk-avatar">
    <div class="uk-avatar-image">
      <img
        src="https://mighty.tools/mockmind-api/content/human/45.jpg"
        alt=""
      />
    </div>
  </div>
</div>
```

## Rounded

To create a circular avatar, simply apply the `uk-avatar-rounded` class to the wrapper.

### Example

```html
<div class="flex justify-center gap-x-2">
  <div class="uk-avatar uk-avatar-rounded bg-secondary">
    <div class="uk-avatar-image">
      <img
        src="https://mighty.tools/mockmind-api/content/human/120.jpg"
        alt="Maria"
      />
    </div>
  </div>
</div>
```

## Bordered

To add a border around your avatar, include the `uk-avatar-bordered` class along with any other modifiers you like.

### Example

```html
<div class="flex items-center justify-center gap-x-2">
  <div class="uk-avatar uk-avatar-bordered">
    <div class="uk-avatar-image">
      <img
        src="https://mighty.tools/mockmind-api/content/human/67.jpg"
        alt=""
      />
    </div>
  </div>

  <div class="uk-avatar uk-avatar-rounded uk-avatar-bordered">
    <div class="uk-avatar-image">
      <img
        src="https://mighty.tools/mockmind-api/content/human/18.jpg"
        alt=""
      />
    </div>
  </div>
</div>
```

## Initials

If there's no image available, display initials using the `.uk-avatar-text` element. This is useful for fallback states or text-based avatars.

### Example

```html
<div class="flex justify-center gap-x-2">
  <div class="uk-avatar text-muted-foreground bg-muted">
    <div class="uk-avatar-text">RM</div>
  </div>

  <div class="uk-avatar uk-avatar-rounded text-muted-foreground bg-muted">
    <div class="uk-avatar-text">RM</div>
  </div>

  <div class="uk-avatar uk-avatar-bordered">
    <div class="uk-avatar-text">RM</div>
  </div>
</div>
```

## Dot indicator

To indicate status or notifications, you can add a small dot using the `uk-avatar-dot` class. Or, choose one of the following classes to reposition the dot indicator:

| Class                        | Position      |
| ---------------------------- | ------------- |
| `uk-avatar-dot-top`          | Top center    |
| `uk-avatar-dot-top-left`     | Top left      |
| `uk-avatar-dot-top-right`    | Top right     |
| `uk-avatar-dot-right`        | Right center  |
| `uk-avatar-dot-bottom`       | Bottom center |
| `uk-avatar-dot-bottom-left`  | Bottom left   |
| `uk-avatar-dot-bottom-right` | Bottom right  |
| `uk-avatar-dot-left`         | Left center   |

### Example

```html
<div class="flex items-center justify-center">
  <div class="uk-avatar uk-avatar-rounded uk-avatar-dot">
    <div class="uk-avatar-image">
      <img
        src="https://mighty.tools/mockmind-api/content/human/120.jpg"
        alt=""
      />
    </div>
  </div>
</div>
```

## Stacked

Stack multiple avatars together to represent a group or team. Use flex utilities and negative spacing to achieve the overlapping effect.

### Example

```html
<div class="flex items-center justify-center -space-x-4">
  <div class="uk-avatar uk-avatar-rounded uk-avatar-bordered">
    <div class="uk-avatar-image">
      <img
        src="https://mighty.tools/mockmind-api/content/human/120.jpg"
        alt=""
      />
    </div>
  </div>

  <div class="uk-avatar uk-avatar-rounded uk-avatar-bordered">
    <div class="uk-avatar-image">
      <img
        src="https://mighty.tools/mockmind-api/content/human/121.jpg"
        alt=""
      />
    </div>
  </div>

  <div class="uk-avatar uk-avatar-rounded uk-avatar-bordered">
    <div class="uk-avatar-image">
      <img
        src="https://mighty.tools/mockmind-api/content/human/122.jpg"
        alt=""
      />
    </div>
  </div>

  <div class="uk-avatar uk-avatar-rounded uk-avatar-bordered">
    <div class="uk-avatar-image">
      <img
        src="https://mighty.tools/mockmind-api/content/human/123.jpg"
        alt=""
      />
    </div>
  </div>

  <div
    class="uk-avatar uk-avatar-rounded uk-avatar-bordered bg-primary text-primary-foreground"
  >
    <div class="uk-avatar-text">+99</div>
  </div>
</div>
```
