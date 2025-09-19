## Stepper

To create a stepper, just add the `.uk-stepper` class to a `<ul>` tag.

```html
<ul class="uk-stepper uk-stepper-default">
  <li>
    <a href="#">Personal Info</a>
  </li>
  <li>
    <a href="#">Account Info</a>
  </li>
  <li>
    <a href="#">Confirmation</a>
  </li>
</ul>
```

### Example

```html
<ul class="uk-stepper uk-stepper-default">
  <li>
    <a href="#">Personal Info</a>
  </li>
  <li>
    <a href="#">Account Info</a>
  </li>
  <li>
    <a href="#">Confirmation</a>
  </li>
</ul>
```

## Active modifier

This example can be used to highlight the current step in the stepper, indicating which step is actively being worked on.

Note: When you add the `.uk-active` class to one of your `li` tags, the previous `li` tags will automatically change colors.

### Example

```html
<ul class="uk-stepper uk-stepper-default">
  <li>
    <a href="#">Personal Info</a>
  </li>
  <li class="uk-active">
    <a href="#">Account Info</a>
  </li>
  <li>
    <a href="#">Confirmation</a>
  </li>
</ul>
```

## Checked modifier

To show a checkmark when the step has been finished, add the `.uk-stepper-checked` to one of your `li` tag.

### Example

```html
<ul class="uk-stepper uk-stepper-default">
  <li class="uk-stepper-checked">
    <a href="#">Personal Info</a>
  </li>
  <li class="uk-active">
    <a href="#">Account Info</a>
  </li>
  <li>
    <a href="#">Confirmation</a>
  </li>
</ul>
```

## Counter modifier

This example can be used to display step numbers within the stepper, helping to indicate the sequence of steps. Each li tag will be numbered to show its position in the progression.

### Example

```html
<ul class="uk-stepper uk-stepper-default uk-stepper-counter">
  <li class="uk-stepper-checked">
    <a href="#">Personal Info</a>
  </li>
  <li class="uk-active">
    <a href="#">Account Info</a>
  </li>
  <li>
    <a href="#">Confirmation</a>
  </li>
</ul>
```
