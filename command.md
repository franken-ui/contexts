## Command

The Command component is a web component built from scratch to allow developers to bind a keyboard shortcut and toggle a modal.

To get started, simply use the `<uk-command>` markup in your HTML code with one `<select hidden></select>` tag as items reference.

```html
<uk-command>
  <select hidden>
    <optgroup label="Suggestions">
      <option data-icon="calendar" value="/path/to/calendar">Calendar</option>
      <option data-icon="smile" value="/path/to/search-emoji">
        Search Emoji
      </option>
      <option data-icon="calculator" disabled value="/path/to/calculator">
        Calculator
      </option>
    </optgroup>
    <optgroup label="Settings">
      <option data-icon="user" value="/path/to/profile">Profile</option>
      <option data-icon="credit-card" value="/path/to/billing">Billing</option>
      <option data-icon="settings" value="/path/to/settings">Settings</option>
    </optgroup>
  </select>
</uk-command>
```

## Binding a keyboard shortcut

By default, no keyboard shortcuts are bound. To enable a keyboard shortcut, simply add the `key` attribute to your Command component.

### Example

```html
<div class="text-muted-foreground text-center">
  Press <kbd class="uk-kbd">⌘ J</kbd>
</div>

<uk-command key="j">
  <select hidden>
    <optgroup label="Suggestions">
      <option data-icon="calendar" value="/path/to/calendar">Calendar</option>
      <option data-icon="smile" value="/path/to/search-emoji">
        Search Emoji
      </option>
      <option data-icon="calculator" disabled value="/path/to/calculator">
        Calculator
      </option>
    </optgroup>
    <optgroup label="Settings">
      <option data-icon="user" value="/path/to/profile">Profile</option>
      <option data-icon="credit-card" value="/path/to/billing">Billing</option>
      <option data-icon="settings" value="/path/to/settings">Settings</option>
    </optgroup>
  </select>
</uk-command>
```

## Using a toggle

Since we are using the UIkit modal behind the scenes, we can use any element to toggle a Command component. To start, simply add the toggle attribute to the `<uk-command>` element. Then, you can use an `<a>` element linked to the toggle ID like this: `<a href="#TOGGLE" uk-toggle>`. If you are using another element, such as a button, just add the `uk-toggle="target: #TOGGLE"` attribute to toggle the Command component.

### Example

```html
<button
  class="uk-btn uk-btn-default mr-2"
  type="button"
  data-uk-toggle="target: #cmd2"
>
  Open
</button>

<a href="#cmd2" data-uk-toggle>Open</a>

<uk-command toggle="cmd2">
  <select hidden>
    <optgroup label="Suggestions">
      <option data-icon="calendar" value="/path/to/calendar">Calendar</option>
      <option data-icon="smile" value="/path/to/search-emoji">
        Search Emoji
      </option>
      <option data-icon="calculator" disabled value="/path/to/calculator">
        Calculator
      </option>
    </optgroup>
    <optgroup label="Settings">
      <option data-icon="user" value="/path/to/profile">Profile</option>
      <option data-icon="credit-card" value="/path/to/billing">Billing</option>
      <option data-icon="settings" value="/path/to/settings">Settings</option>
    </optgroup>
  </select>
</uk-command>
```

## Programmatic navigation

By default, the command palette component does not perform any action when an item is selected or clicked. This allows for flexibility in handling user input. To respond to user input, you need to manually attach an event listener to the component specifically to the `uk-command:select` event.

To get started, assign an ID to your command component and attach an event listener to it.

### Example

```html
<button
  class="uk-btn uk-btn-default"
  type="button"
  data-uk-toggle="target: #programmatic_navigation"
>
  Open
</button>

<uk-command id="cmd-demo" toggle="programmatic_navigation">
  <select hidden>
    <optgroup label="Suggestions">
      <option data-icon="calendar" value="/path/to/calendar">Calendar</option>
      <option data-icon="smile" value="/path/to/search-emoji">
        Search Emoji
      </option>
      <option data-icon="calculator" disabled value="/path/to/calculator">
        Calculator
      </option>
    </optgroup>
    <optgroup label="Settings">
      <option data-icon="user" value="/path/to/profile">Profile</option>
      <option data-icon="credit-card" value="/path/to/billing">Billing</option>
      <option data-icon="settings" value="/path/to/settings">Settings</option>
    </optgroup>
  </select>
</uk-command>

<script>
  const el = document.getElementById("cmd-demo");

  el?.addEventListener("uk-command:click", (e) => {
    console.log(e.detail.value.value);

    // location.href = e.detail.value.value;
  });
</script>
```

You can try out this example by checking your browser's developer console. When you select an item from the command palette, the selected value will be logged to the console. From there, you can handle the value as needed to respond to the user's input.

## Customizing searchable keywords

Sometimes, there are elements that have related keywords that may be slightly off or awkward when included as anchor tags. For these use cases, we can leverage the `data-keywords` attribute.

For example, if we have a "Form" link but also want it to appear when users search for terms like "checkbox," "input," "toggle switch," etc., we can simply add a comma-separated list of terms like this: `data-keywords="checkbox,input,radio"`

```html
<uk-command>
  <select hidden>
    <optgroup label="Components">
      <option data-keywords="checkbox,input,radio" value="/path/to/form">
        Form
      </option>
    </optgroup>
  </select>
</uk-command>
```

## Grouping related items

To group related elements, simply use the `optgroup` tag and items will be automatically sorted and grouped with headers.

```html
<uk-command>
  <select hidden>
    <optgroup label="Suggestions">
      <!-- ... -->
    </optgroup>
    <optgroup label="Settings">
      <!-- ... -->
    </optgroup>
  </select>
</uk-command>
```

## Disabling an item

Sometimes, we may want to disable items. To do this, simply use the `disabled` attribute, and the item will be automatically disabled.

```html
<uk-command>
  <select hidden>
    <optgroup label="Suggestions">
      <option data-icon="calculator" disabled value="/path/to/calculator">
        Calculator
      </option>
    </optgroup>
  </select>
</uk-command>
```

## Attributes

The following attributes are available for this component:

| Name                     | Type    | Default | Description                                                                                                                                               |
| ------------------------ | ------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `force-prevent-rerender` | Boolean | false   | Forcefully prevents component rerendering.                                                                                                                |
| `key`                    | Sring   |         | Assign a keyboard shortcut.                                                                                                                               |
| `placeholder`            | String  | Search  | The placeholder for the input.                                                                                                                            |
| `toggle`                 | String  |         | Behind the scenes, this will be used as the ID of the modal. It is useful for manually toggling the Command component using an `<a>` or a `<button>` tag. |

## Events

The Command component triggers the following events on elements with this component attached:

| Name                | Description                                                                                     |
| ------------------- | ----------------------------------------------------------------------------------------------- |
| `uk-command:select` | Fired after an item was selected or clicked, providing an opportunity to respond to user input. |
