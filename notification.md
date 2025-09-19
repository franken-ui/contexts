## Notification

The notification will not fade out but remain visible when you hover the message until you stop hovering. You can also close the notification by clicking it. To show notifications, the component provides a simple JavaScript API. The following code snippet gets you started.

### JavaScript

```javascript
UIkit.notification({
  message: "my-message!",
  status: "primary",
  pos: "top-right",
  timeout: 5000,
});

// Shortcuts
UIkit.notification("My message");
UIkit.notification("My message", status);
UIkit.notification("My message", {
  /* options */
});
```

### Example

```html
<button
  class="demo uk-btn uk-btn-default"
  type="button"
  onclick="UIkit.notification({message: 'Notification message'})"
>
  Click me
</button>
```

## HTML message

You can use HTML inside your notification message, like an icon from the Icon component.

```javascript
UIkit.notification("<uk-icon icon='rocket'></uk-icon> Message");
```

### Example

```html
<button
  class="demo uk-btn uk-btn-default"
  type="button"
  onclick="UIkit.notification({
      message: `<div class='flex items-center'><span class='flex-none mr-2'><uk-icon icon='rocket'></uk-icon></span> Message with an icon</div>`
  })"
>
  With icon
</button>
```

## Position

Add one of the following parameters to adjust the notification's position to different corners.

```javascript
UIkit.notification("...", { pos: "top-right" });
```

| Position        | Code                                                |
| --------------- | --------------------------------------------------- |
| `top-left`      | `UIkit.notification("...", {pos: 'top-left'})`      |
| `top-center`    | `UIkit.notification("...", {pos: 'top-center'})`    |
| `top-right`     | `UIkit.notification("...", {pos: 'top-right'})`     |
| `bottom-left`   | `UIkit.notification("...", {pos: 'bottom-left'})`   |
| `bottom-center` | `UIkit.notification("...", {pos: 'bottom-center'})` |
| `bottom-right`  | `UIkit.notification("...", {pos: 'bottom-right'})`  |

### Example

```html
<div class="flex flex-wrap gap-2">
  <button
    class="uk-btn uk-btn-default"
    type="button"
    onclick="UIkit.notification({message: 'Top Left', pos: 'top-left'})"
  >
    Top Left
  </button>
  <button
    class="uk-btn uk-btn-default"
    type="button"
    onclick="UIkit.notification({message: 'Top Center', pos: 'top-center'})"
  >
    Top Center
  </button>
  <button
    class="uk-btn uk-btn-default"
    type="button"
    onclick="UIkit.notification({message: 'Top Right', pos: 'top-right'})"
  >
    Top Right
  </button>
  <button
    class="uk-btn uk-btn-default"
    type="button"
    onclick="UIkit.notification({message: 'Bottom Left', pos: 'bottom-left'})"
  >
    Bottom Left
  </button>
  <button
    class="uk-btn uk-btn-default"
    type="button"
    onclick="UIkit.notification({message: 'Bottom Center', pos: 'bottom-center'})"
  >
    Bottom Center
  </button>
  <button
    class="uk-btn uk-btn-default"
    type="button"
    onclick="UIkit.notification({message: 'Bottom Right', pos: 'bottom-right'})"
  >
    Bottom Right
  </button>
</div>
```

## Destructive modifier

```javascript
UIkit.notification("...", { status: "destructive" });
```

### Example

```html
<button
  class="demo uk-btn uk-btn-default"
  type="button"
  onclick="UIkit.notification({message: 'Destructive message', status: 'destructive'})"
>
  Destructive
</button>
```

## Close all

You can close all open notifications by calling `UIkit.notification.closeAll()`.

### Example

```html
<button
  class="close uk-btn uk-btn-default"
  onclick="UIkit.notification.closeAll()"
>
  Close All
</button>
```

## Component options

Any of these options can be applied to the component attribute. Separate multiple options with a semicolon. [Learn more](https://franken-ui.dev/docs/2.1/javascript#component-configuration)

| Option     | Value  | Default      | Description                                                                                                   |
| ---------- | ------ | ------------ | ------------------------------------------------------------------------------------------------------------- |
| `message ` | String | `false`      | Notification message to show.                                                                                 |
| `status`   | String | `null`       | Notification status color.                                                                                    |
| `timeout`  | Number | `5000`       | Visibility duration until a notification disappears. If set to `0`, notification will not hide automatically. |
| `group`    | String |              | Useful, if you want to close all notifications in a specific group.                                           |
| `pos`      | String | `top-center` | Display corner.                                                                                               |

## JavaScript

Learn more about [JavaScript components](https://franken-ui.dev/docs/2.1/javascript#programmatic-use).

### Initialization

This is a `Functional Component` and may omit the element argument.

```javascript
UIkit.notification(options);
UIkit.notification(message, status);
```

### Events

The following events will be triggered on elements with this component attached:

| Name    | Description                                   |
| ------- | --------------------------------------------- |
| `close` | Fires after the notification has been closed. |

### Methods

The following methods are available for the component:

#### Close

```javascript
UIkit.notification(element).close(immediate);
```

Closes the notification.

| Name        | Type    | Default | Description                      |
| ----------- | ------- | ------- | -------------------------------- |
| `immediate` | Boolean | true    | Transition the notification out. |

## Accessibility

The Notification component automatically sets the appropriate WAI-ARIA role, states and properties.

- The _notification_ has the `alert` role.
