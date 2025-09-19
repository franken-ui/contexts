## Dropdown

The Dropdown component is aim-aware. This means the dropdown stays open as long as the mouse pointer moves towards the dropdown. An additional delay ensures that the dropdown stays open even if the mouse pointer shortly moves in another direction. A dropdown closes immediately if another menu item is hovered.

A dropdown is an example of the [drop](https://franken-ui.dev/docs/2.1/drop) that provides its [own styling](https://github.com/uikit/uikit/issues/2237). Any content, like a button, can toggle a dropdown. Just add the `data-uk-dropdown` attribute to a block element following the toggle.

### Example

```html
<button class="uk-btn uk-btn-default mr-2" type="button">Hover</button>
<div class="uk-drop uk-dropdown min-w-52" data-uk-dropdown>
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

<button class="uk-btn uk-btn-default" type="button">Click</button>
<div class="uk-drop uk-dropdown min-w-52" data-uk-dropdown="mode: click">
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
