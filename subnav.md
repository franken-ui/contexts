## Subnav

To apply this component, use the following classes. To align a subnav, for example to horizontally center it, you can use utility classes from Tailwind CSS.

| Class         | Description                                                                                                         |
| ------------- | ------------------------------------------------------------------------------------------------------------------- |
| `.uk-subnav`  | Add this class to a `<ul>` element to define the Subnav component. Use `<a>` elements as nav items within the list. |
| `.uk-active ` | Add this class to a list item to apply an active state.                                                             |

To add list items without a link, use a `<span>` element instead of an `<a>`. Alternatively, disable an `<a>` element by adding the `.uk-disabled` class to the `<li>` element and remove the `href` attribute from the anchor to make it inaccessible through keyboard navigation.

```html
<ul class="uk-subnav">
  <li class="uk-active"><a href=""></a></li>
  <li><a href=""></a></li>
  <li><span></span></li>
</ul>
```

### Example

```html
<ul class="uk-subnav">
  <li><a href="#">Active</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
</ul>
```

## Style modifiers

Add one of the following classes for additional styles.

| Class                    | Description               |
| ------------------------ | ------------------------- |
| `.uk-subnav-primary`     | Adds a primary style.     |
| `.uk-subnav-secondary`   | Adds a secondary style.   |
| `.uk-subnav-destructive` | Adds a destructive style. |

### Example

```html
<ul class="uk-subnav uk-subnav-primary">
  <li class="uk-active"><a href="#">Active</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><span class="opacity-50">Disabled</span></li>
</ul>

<ul class="uk-subnav uk-subnav-secondary mt-4">
  <li class="uk-active"><a href="#">Active</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><span class="opacity-50">Disabled</span></li>
</ul>

<ul class="uk-subnav uk-subnav-destructive mt-4">
  <li class="uk-active"><a href="#">Active</a></li>
  <li><a href="#">Item</a></li>
  <li><a href="#">Item</a></li>
  <li><span class="opacity-50">Disabled</span></li>
</ul>
```

## Subnav and Dropdown

You can also use a dropdown from the [Dropdown component](https://franken-ui.dev/docs/2.1/dropdown) with a subnav.

```html
<ul class="uk-subnav">
  <li>
    <!-- This is the menu item toggling the dropdown -->
    <a href=""></a>

    <!-- This is the dropdown -->
    <div data-uk-dropdown="mode: click">
      <ul class="uk-dropdown-nav uk-nav">
        ...
      </ul>
    </div>
  </li>
</ul>
```

### Example

```html
<ul class="uk-subnav uk-subnav-primary">
  <li class="uk-active"><a href="#">Active</a></li>
  <li><a href="#">Item</a></li>
  <li>
    <a href>
      <span class="mr-2">More</span>
      <uk-icon icon="chevron-down"></uk-icon>
    </a>
    <div class="uk-drop min-w-52" data-uk-dropdown="mode: click">
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
  </li>
</ul>
```
