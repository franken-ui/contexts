## Input tag

The Input Tag component is a web component built from scratch to allow users to easily create and manage a list of tags or keywords, such as categorizing items, assigning labels, or filtering content. This is particularly useful in scenarios such as:

- Tagging articles or blog posts
- Organizing products or inventory by category
- Building a custom filtering system for a dataset

To get started, simply use the `<uk-input-tag>` markup in your HTML code.

Note: While this component provides features to help manage tags, such as preventing duplicates and handling input validation, it is still a frontend component and can be tampered with by users. Therefore, it is essential to sanitize and validate user input on the server-side to ensure data integrity and security.

### Example

```html
<form>
  <uk-input-tag placeholder="Add a fruit"></uk-input-tag>
</form>
```

## Capturing values

There are several ways to capture values from the `<uk-input-tag>` component. The simplest approach is to add a `name` attribute to the component. When you do this, a hidden input field with the specified name will be automatically generated, allowing you to easily capture the selected value on your server.

```html
<uk-input-tag name="tags"></uk-input-tag>
```

## Prepopulating values

To prepopulate the Input Tag component with existing values, simply pass the `value` attribute with a comma-separated list of tag values. This allows you to initialize the component with a set of default tags, making it easier for users to build upon or edit existing data.

### Example

```html
<form>
  <uk-input-tag
    placeholder="Add a fruit"
    value="Apple,Mango,Lemon"
  ></uk-input-tag>
</form>
```

## State modifiers

You can customize the appearance of individual tags by setting the `state` attribute. By default, tags will use the `uk-tag-secondary` class. However, you can choose from a range of available options to change the tag's visual state, including:

| Style         | Class used              | Description               |
| ------------- | ----------------------- | ------------------------- |
| `primary`     | `.uk-label-primary`     | Adds a primary style.     |
| `secondary`   | `.uk-label-secondary`   | Adds a secondary style.   |
| `destructive` | `.uk-label-destructive` | Adds a destructive style. |

This allows you to add visual cues to your tags, making it easier to convey different types of information or categorizations.

### Example

```html
<form>
  <div>
    <uk-input-tag
      placeholder="Add a tag"
      state="primary"
      value="Featured,Recommended,Verified"
    ></uk-input-tag>
  </div>

  <div class="mt-4">
    <uk-input-tag
      placeholder="Add a tag"
      value="Category,Topic,Tag,Label,Filter"
    ></uk-input-tag>
  </div>

  <div class="mt-4">
    <uk-input-tag
      placeholder="Add a tag"
      state="destructive"
      value="Deprecated,Error,Unsupported"
    ></uk-input-tag>
  </div>
</form>
```

## Behavior

The Input Tag component provides intuitive mouse and keyboard interactions to facilitate easy tag management.

### Mouse Behavior

- Clicking on a tag name will remove it from the list and place its value in the input field, allowing you to edit the tag.
- Clicking the close icon on a tag will remove it from the list entirely.

### Keyboard Behavior

- When the input field is empty and you press the backspace key, the last tag in the list will be removed and its value will be placed in the input field, allowing you to edit or delete it.
- Pressing Enter or comma (,) key will add input value to the list of tags.

These interactions enable a seamless and efficient tagging experience.

## Slugifying tags

By default, user-submitted tags will be added exactly as they are entered. To automatically convert tags into a slug format (e.g., converting spaces to hyphens, removing special characters, etc.), simply add the `slugify` attribute to the `<uk-input-tag>` element. This ensures that tags are formatted consistently and are more suitable for use in URLs or other technical contexts.

### Example

```html
<form>
  <uk-input-tag
    placeholder="Add a tag"
    slugify
    value="fan-fiction"
  ></uk-input-tag>
</form>
```

Under the hood, we use the popular [slugify](https://github.com/simov/slugify) package to convert user-submitted tags into a slug format. To customize the slugification process, you can pass options using the slugify-options attribute. This attribute accepts either a JSON-stringified object or a valid `key: value; foo: bar;` format.

### Available Options

The following options are available for customizing the slugify behavior:

| Option        | Description                                                                                   | Default |
| ------------- | --------------------------------------------------------------------------------------------- | ------- |
| `replacement` | The replacement string used to replace spaces and other characters                            | -       |
| `remove`      | A valid regular expression pattern to remove from the tag                                     |         |
| `lower`       | A boolean indicating whether to convert the tag to lowercase                                  | true    |
| `strict`      | A boolean indicating whether to strip special characters except for the replacement character | true    |
| `locale`      | The language code of the locale to use for slugification                                      |         |
| `trim`        | A boolean indicating whether to trim leading and trailing replacement characters              | true    |

For more information about the [slugify](https://github.com/simov/slugify) package and its options, please refer to the [official documentation](https://github.com/simov/slugify).

## Disable input

To prevent user input, add the `disabled` attribute to the `<uk-input-tag>` element. This will disable input field, prevent tags editing and removal. Making it impossible for users to enter or modify tags.

### Example

```html
<form>
  <uk-input-tag
    placeholder="Add a tag"
    slugify
    value="Verified,Exclusive"
    state="primary"
    disabled
  ></uk-input-tag>
</form>
```

## Error state

To indicate an error state in the form, simply add the `.uk-form-destructive` class to the `cls-custom` attribute. This will apply a "destructive" state to the component, providing visual feedback to the user.

### Example

```html
<form class="space-y-1.5">
  <label class="uk-form-label text-destructive">Tags</label>
  <div class="uk-form-controls">
    <uk-input-tag
      cls-custom="uk-form-destructive"
      placeholder="Add a tag"
    ></uk-input-tag>
  </div>
  <p class="uk-form-help text-destructive">This field is required.</p>
</form>
```

## Preventing layout shift

When loading Web Components, a brief delay may cause a flash of unstyled content. To mitigate this issue, consider setting a predefined height on the parent element to prevent layout shift and ensure a smooth user experience.

```html
<div class="min-h-11">
  <uk-input-tag></uk-input-tag>
</div>
```

Please note that we used `min-h-*` because component might grow in height depending on the number of tags.

## Attributes

| Name                     | Type    | Default     | Description                                                                                                                                         |
| ------------------------ | ------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `force-prevent-rerender` | Boolean | false       | Forcefully prevents component rerendering.                                                                                                          |
| `cls-custom`             | String  |             | Allows you to add custom CSS classes.                                                                                                               |
| `disabled`               | Boolean | false       | Disables input field, making the entire component read-only.                                                                                        |
| `maxlength`              | String  | 20          | The maximum length of each tag before it can be added.                                                                                              |
| `minlength`              | String  | 1           | The minimum length of each tag before it can be added.                                                                                              |
| `name`                   | String  |             | The name of the input field, which allows you to capture the tags on your server. Note that the component will automatically append [] to the name. |
| `placeholder`            | String  |             | The placeholder text displayed in the input field.                                                                                                  |
| `slugify`                | Boolean | false       | A boolean indicating whether to slugify the input string before adding it as a tag.                                                                 |
| `slugify-options`        |         | false       | A string with `key: value` format or JSON-stringified options for customizing the slugify behavior.                                                 |
| `state`                  | String  | `secondary` | The visual state of the tags, which can be set to `primary`, `secondary`, or `destructive` to change their appearance.                              |
| `value`                  | String  |             | A comma-separated list of tags that will be prepopulated in the input field.                                                                        |

## Events

The Input Tag component triggers the following events on elements with this component attached:

| Name                 | Description                                                                           |
| -------------------- | ------------------------------------------------------------------------------------- |
| `uk-input-tag:input` | Fired after the value has changed, providing an opportunity to respond to user input. |
