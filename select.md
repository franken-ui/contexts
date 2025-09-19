## Select

The custom select component is a web component built from scratch to enhance the native `<select>` tag. To get started, simply use the `<uk-select>` markup in your HTML code with one `<select hidden></select>` tag as options reference.

### Example

```html
<div class="h-10">
  <uk-select cls-custom="button: uk-input-fake w-full; dropdown: w-full">
    <select hidden>
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>
```

## Styling

The `<uk-select>` component is intentionally unstyled by default, allowing you to easily customize its appearance to fit your needs.

To add custom styles, use the `cls-custom` attribute. This attribute accepts two formats:

- A JSON-stringified object
- A valid `key: value; foo: bar;` format

If you pass only class names, they will be applied directly to the button inside the component.

### Example

```html
<!-- Unstyled -->
<div class="h-10">
  <uk-select placeholder="Unstyled">
    <select hidden>
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>

<!-- Custom -->
<div class="h-10">
  <uk-select
    cls-custom="button: bg-lime-500 text-lime-50 w-full flex justify-between; icon: bg-orange-500 text-orange-50; dropdown: bg-purple-500 text-purple-50 w-full;"
    icon="chevron-down"
  >
    <select hidden>
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>
```

## Capturing values

There are several ways to capture values from the `<uk-select>` component. The simplest approach is to add a `name` attribute to the component. When you do this, a hidden input field with the specified name will be automatically generated, allowing you to easily capture the selected value on your server.

### Example

```html
<div class="h-10">
  <uk-select
    cls-custom="button: uk-input-fake w-full; dropdown: w-full"
    name="option"
  >
    <select hidden>
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>
```

Note: If you don't specify a `value` attribute for an `<option>` tag, it will default to using its text content as the value instead.

## Parent icon

To add a parent icon, just add an `icon` attribute to the `<uk-select>` component. If you want to customize the icon, just pass a string name of the icon.

### Example

```html
<div class="h-10">
  <uk-select
    cls-custom="button: uk-input-fake justify-between w-full; dropdown: w-full"
    icon
  >
    <select hidden>
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>

<div class="mt-4 h-10">
  <uk-select
    cls-custom="button: uk-input-fake justify-between w-full; dropdown: w-full"
    icon="arrow-down"
  >
    <select hidden>
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>
```

## Options icon

To add icon to options, just add `data-icon` attribute with the name of the icon to your `<option>` tags.

### Example

```html
<div class="h-10">
  <uk-select cls-custom="button: uk-input-fake w-full; dropdown: w-full">
    <select hidden>
      <option data-icon="circle" value="option1">Option 1</option>
      <option data-icon="circle" value="option2">Option 2</option>
      <option data-icon="circle" value="option3">Option 3</option>
      <option data-icon="circle" value="option4">Option 4</option>
      <option data-icon="circle" value="option5">Option 5</option>
    </select>
  </uk-select>
</div>
```

## Position

Because the `<uk-select>` component uses the [Drop](https://franken-ui.dev/docs/2.1/drop) component under the hood, we can leverage its positioning capabilities and position our dropdown anywhere we want. To position it, just use the `drop` attribute with your drop options.

### Example

```html
<div class="h-10">
  <uk-select
    cls-custom="button: uk-btn uk-btn-default"
    drop="mode: click; pos: right-center"
    searchable
  >
    <select hidden>
      <option data-description="Can view and comment." value="viewer">
        Viewer
      </option>
      <option data-description="Can view, comment and edit." value="developer">
        Developer
      </option>
      <option
        data-description="Can view, comment and manage billing."
        value="billing"
      >
        Billing
      </option>
      <option data-description="Admin-level to all resources." value="owner">
        Owner
      </option>
    </select>
  </uk-select>
</div>
```

## Size modifiers

There are several size modifiers available. Just add one of the following classes to make the fake input smaller or larger.

| Class         | Description               |
| ------------- | ------------------------- |
| `.uk-form-xs` | Applies extra small size. |
| `.uk-form-sm` | Applies small size.       |
| `.uk-form-md` | Applies medium size.      |
| `.uk-form-lg` | Applies large size.       |

### Example

```html
<div class="mt-4 h-7">
  <uk-select
    cls-custom="button: uk-input-fake uk-form-xs w-full; dropdown: w-full"
  >
    <select hidden>
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>

<div class="mt-4 h-8">
  <uk-select
    cls-custom="button: uk-input-fake uk-form-sm w-full; dropdown: w-full"
  >
    <select hidden>
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>

<div class="mt-4 h-12">
  <uk-select
    cls-custom="button: uk-input-fake uk-form-md w-full; dropdown: w-full"
  >
    <select hidden>
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>

<div class="mt-4 h-14">
  <uk-select
    cls-custom="button: uk-input-fake uk-form-md w-full; dropdown: w-full"
  >
    <select hidden>
      <option value="option1">Option 1</option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>
```

## Adding header

To add a header to your custom select component, use the `<optgroup>` tag, which will be automatically converted into a dropdown header, providing a seamless developer experience.

### Example

```html
<div class="h-10">
  <uk-select cls-custom="button: uk-input-fake w-full; dropdown: w-full">
    <select hidden>
      <optgroup label="Letter A">
        <option value="apple">Apple</option>
        <option value="apricot">Apricot</option>
        <option value="avocado">Avocado</option>
        <option value="ackee">Ackee</option>
        <option value="asian_pear">Asian Pear</option>
        <option value="abiu">Abiu</option>
        <option value="ambarella">Ambarella</option>
      </optgroup>

      <optgroup label="Letter B">
        <option value="banana">Banana</option>
        <option value="blackberry">Blackberry</option>
        <option value="blueberry">Blueberry</option>
        <option value="boysenberry">Boysenberry</option>
        <option value="breadfruit">Breadfruit</option>
        <option value="bilberry">Bilberry</option>
        <option value="bael">Bael</option>
        <option value="black_sapote">Black Sapote</option>
      </optgroup>

      <optgroup label="Letter C">
        <option value="cherry">Cherry</option>
        <option value="coconut">Coconut</option>
        <option value="cranberry">Cranberry</option>
        <option value="cantaloupe">Cantaloupe</option>
        <option value="clementine">Clementine</option>
        <option value="cactus_pear">Cactus Pear</option>
        <option value="cherimoya">Cherimoya</option>
        <option value="cloudberry">Cloudberry</option>
        <option value="calamansi">Calamansi</option>
      </optgroup>

      <optgroup label="Letter D">
        <option value="date">Date</option>
        <option value="dragonfruit">Dragonfruit</option>
        <option value="durian">Durian</option>
        <option value="damson">Damson</option>
        <option value="dewberry">Dewberry</option>
        <option value="duku">Duku</option>
        <option value="dilly">Dilly</option>
      </optgroup>
    </select>
  </uk-select>
</div>
```

## Selecting multiple values

To enable the selection of multiple values, simply add the `multiple` attribute to the `<uk-select>` element. This will allow users to choose multiple options from the dropdown list.

### Example

```html
<div class="h-10">
  <uk-select
    cls-custom="button: uk-input-fake w-full; dropdown: w-full"
    multiple
  >
    <select hidden>
      <option value="python">Python Programming Language</option>
      <option value="javascript">JavaScript Programming Language</option>
      <option value="html">HTML Markup Language</option>
      <option value="css">CSS Styling Language</option>
      <option value="ruby">Ruby Programming Language</option>
      <option value="java">Java Programming Language</option>
      <option value="swift">Swift Programming Language</option>
      <option value="go">Go Programming Language</option>
    </select>
  </uk-select>
</div>
```

Note: When utilizing the `multiple` attribute, note that it will automatically append `[]` to the name of your input. This is particularly useful when your server expects multiple values, even if the user selects only one option. This ensures that your server-side logic can properly handle the input, regardless of the number of values selected.

## Prepopulating values

There are two ways to prepopulate values from the `<uk-select>` component. The simplest approach is to add a `selected` attribute to one or more of your `<option>` tags.

### Example

```html
<div class="space-y-1.5">
  <label class="uk-form-label">Select your planet</label>
  <div class="uk-form-controls">
    <div class="h-10">
      <uk-select cls-custom="button: uk-input-fake w-full; dropdown: w-full">
        <select hidden>
          <option>Mars</option>
          <option>Jupiter</option>
          <option>Saturn</option>
          <option selected>Earth</option>
        </select>
      </uk-select>
    </div>
  </div>
</div>

<div class="mt-4 space-y-1.5">
  <label class="uk-form-label">Select your cars</label>
  <div class="uk-form-controls">
    <div class="h-10">
      <uk-select
        cls-custom="button: uk-input-fake w-full; dropdown: w-full"
        multiple
      >
        <select hidden>
          <option selected>Mercedes-Benz</option>
          <option selected>Bentley</option>
          <option>Audi</option>
          <option selected>Porsche</option>
          <option selected>Lamborghini</option>
          <option>Ferrari</option>
        </select>
      </uk-select>
    </div>
  </div>
</div>
```

### Manually setting value

Alternatively, if setting `selected` on individual `<option>` elements is not feasible, you can use the `value` attribute on the `<uk-select>` tag to prepopulate it with default values. This attribute accepts a comma-separated list of values, allowing you to set multiple defaults, such as `value="Mercedes-Benz,Bentley,Porsche,Lamborghini"`.

### Example

```html
<div class="space-y-1.5">
  <label class="uk-form-label">Select your planet</label>
  <div class="uk-form-controls">
    <div class="h-10">
      <uk-select
        cls-custom="button: uk-input-fake w-full; dropdown: w-full"
        value="Earth"
      >
        <select hidden>
          <option>Mars</option>
          <option>Jupiter</option>
          <option>Saturn</option>
          <option>Earth</option>
        </select>
      </uk-select>
    </div>
  </div>
</div>

<div class="mt-4 space-y-1.5">
  <label class="uk-form-label">Select your cars</label>
  <div class="uk-form-controls">
    <div class="h-10">
      <uk-select
        cls-custom="button: uk-input-fake w-full; dropdown: w-full"
        multiple
        value="Mercedes-Benz,Bentley,Porsche,Lamborghini"
      >
        <select hidden>
          <option>Mercedes-Benz</option>
          <option>Bentley</option>
          <option>Audi</option>
          <option>Porsche</option>
          <option>Lamborghini</option>
          <option>Ferrari</option>
        </select>
      </uk-select>
    </div>
  </div>
</div>
```

Note: When both `value` and `selected` are used, the `value` attribute takes precedence. Therefore, it's recommended to use one method or the other to avoid conflicts.

## Disabling options

Similar to the native `<select>` tag, you can disable specific options in the custom select component by adding the `disabled` attribute to one or more of your `<option>` or `<optgroup>` tags. This allows you to prevent users from selecting certain options.

### Example

```html
<div class="space-y-1.5">
  <label class="uk-form-label">JavaScript Framework</label>
  <div class="uk-form-controls">
    <div class="h-10">
      <uk-select cls-custom="button: uk-input-fake w-full; dropdown: w-full">
        <select hidden>
          <option disabled>React</option>
          <option>Angular</option>
          <option>Astro</option>
          <option disabled>Ember.js</option>
          <option disabled>Backbone.js</option>
          <option disabled>jQuery</option>
          <option>Vue</option>
          <option>SvelteKit</option>
        </select>
      </uk-select>
    </div>
  </div>
  <p class="uk-form-help">Disabled options are library and not a framework.</p>
</div>

<div class="mt-4">
  <label class="uk-form-label">Select fruits</label>
  <div class="h-10">
    <uk-select
      cls-custom="button: uk-input-fake w-full; dropdown: w-full"
      multiple
    >
      <select hidden>
        <optgroup label="Letter A">
          <option value="apple">Apple</option>
          <option value="apricot">Apricot</option>
          <option value="avocado">Avocado</option>
          <option value="ackee">Ackee</option>
          <option value="asian_pear">Asian Pear</option>
          <option value="abiu">Abiu</option>
          <option value="ambarella">Ambarella</option>
        </optgroup>
        <optgroup label="Letter B" disabled>
          <option value="banana">Banana</option>
          <option value="blackberry">Blackberry</option>
          <option value="blueberry">Blueberry</option>
          <option value="boysenberry">Boysenberry</option>
          <option value="breadfruit">Breadfruit</option>
          <option value="bilberry">Bilberry</option>
          <option value="bael">Bael</option>
          <option value="black_sapote">Black Sapote</option>
        </optgroup>
        <optgroup label="Letter C">
          <option value="cherry">Cherry</option>
          <option value="coconut">Coconut</option>
          <option value="cranberry">Cranberry</option>
          <option value="cantaloupe">Cantaloupe</option>
          <option value="clementine">Clementine</option>
          <option value="cactus_pear">Cactus Pear</option>
          <option value="cherimoya">Cherimoya</option>
          <option value="cloudberry">Cloudberry</option>
          <option value="calamansi">Calamansi</option>
        </optgroup>
        <optgroup label="Letter D" disabled>
          <option value="date">Date</option>
          <option value="dragonfruit">Dragonfruit</option>
          <option value="durian">Durian</option>
          <option value="damson">Damson</option>
          <option value="dewberry">Dewberry</option>
          <option value="duku">Duku</option>
          <option value="dilly">Dilly</option>
        </optgroup>
      </select>
    </uk-select>
  </div>
</div>
```

## Reactivity

<span class="uk-label uk-label-destructive">Experimental</span> By default, the `<uk-select>` component is not reactive. This is a deliberate design choice, as using [MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver) can be computationally expensive. As a result, changes to the referenced `<select hidden>` element will not trigger an update.

To enable reactivity, simply add the `reactive` attribute to the `<uk-select>` component. This will use [MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver) under the hood to monitor the `<select hidden>` element for changes.

This feature is particularly useful when using libraries like HTMX, where you may need to dynamically update the options in the `<select hidden>` element based on user interactions, such as searching for data or fetching new options from the server.

```html
<uk-select reactive>
  <!-- ... -->
</uk-select>
```

## Searchable

To add a search box, simply add the `searchable` attribute. This will add an input field within the dropdown menu, enabling users to search for specific options. This feature is particularly useful when dealing with extensive lists, such as selecting a country from a long list of options.

### Example

```html
<div class="h-10">
  <uk-select
    cls-custom="button: uk-input-fake w-full; dropdown: w-full"
    placeholder="Select a country"
    searchable
  >
    <select hidden>
      <option value="Afghanistan">Afghanistan</option>
      <option value="Åland Islands">Åland Islands</option>
      <option value="Albania">Albania</option>
      <option value="Algeria">Algeria</option>
      <option value="American Samoa">American Samoa</option>
      <option value="Andorra">Andorra</option>
      <option value="Angola">Angola</option>
      <option value="Anguilla">Anguilla</option>
      <option value="Antarctica">Antarctica</option>
      <option value="Antigua and Barbuda">Antigua and Barbuda</option>
      <option value="Argentina">Argentina</option>
      <option value="Armenia">Armenia</option>
      <option value="Aruba">Aruba</option>
      <option value="Australia">Australia</option>
      <option value="Austria">Austria</option>
      <option value="Azerbaijan">Azerbaijan</option>
      <option value="Bahamas">Bahamas</option>
      <option value="Bahrain">Bahrain</option>
      <option value="Bangladesh">Bangladesh</option>
      <option value="Barbados">Barbados</option>
      <option value="Belarus">Belarus</option>
      <option value="Belgium">Belgium</option>
      <option value="Belize">Belize</option>
      <option value="Benin">Benin</option>
      <option value="Bermuda">Bermuda</option>
      <option value="Bhutan">Bhutan</option>
      <option value="Bolivia">Bolivia</option>
      <option value="Bosnia and Herzegovina">Bosnia and Herzegovina</option>
      <option value="Botswana">Botswana</option>
      <option value="Bouvet Island">Bouvet Island</option>
      <option value="Brazil">Brazil</option>
      <option value="British Indian Ocean Territory">
        British Indian Ocean Territory
      </option>
      <option value="Brunei Darussalam">Brunei Darussalam</option>
      <option value="Bulgaria">Bulgaria</option>
      <option value="Burkina Faso">Burkina Faso</option>
      <option value="Burundi">Burundi</option>
      <option value="Cambodia">Cambodia</option>
      <option value="Cameroon">Cameroon</option>
      <option value="Canada">Canada</option>
      <option value="Cape Verde">Cape Verde</option>
      <option value="Cayman Islands">Cayman Islands</option>
      <option value="Central African Republic">Central African Republic</option>
      <option value="Chad">Chad</option>
      <option value="Chile">Chile</option>
      <option value="China">China</option>
      <option value="Christmas Island">Christmas Island</option>
      <option value="Cocos (Keeling) Islands">Cocos (Keeling) Islands</option>
      <option value="Colombia">Colombia</option>
      <option value="Comoros">Comoros</option>
      <option value="Congo">Congo</option>
      <option value="Congo, The Democratic Republic of The">
        Congo, The Democratic Republic of The
      </option>
      <option value="Cook Islands">Cook Islands</option>
      <option value="Costa Rica">Costa Rica</option>
      <option value="Cote D'ivoire">Cote D'ivoire</option>
      <option value="Croatia">Croatia</option>
      <option value="Cuba">Cuba</option>
      <option value="Cyprus">Cyprus</option>
      <option value="Czech Republic">Czech Republic</option>
      <option value="Denmark">Denmark</option>
      <option value="Djibouti">Djibouti</option>
      <option value="Dominica">Dominica</option>
      <option value="Dominican Republic">Dominican Republic</option>
      <option value="Ecuador">Ecuador</option>
      <option value="Egypt">Egypt</option>
      <option value="El Salvador">El Salvador</option>
      <option value="Equatorial Guinea">Equatorial Guinea</option>
      <option value="Eritrea">Eritrea</option>
      <option value="Estonia">Estonia</option>
      <option value="Ethiopia">Ethiopia</option>
      <option value="Falkland Islands (Malvinas)">
        Falkland Islands (Malvinas)
      </option>
      <option value="Faroe Islands">Faroe Islands</option>
      <option value="Fiji">Fiji</option>
      <option value="Finland">Finland</option>
      <option value="France">France</option>
      <option value="French Guiana">French Guiana</option>
      <option value="French Polynesia">French Polynesia</option>
      <option value="French Southern Territories">
        French Southern Territories
      </option>
      <option value="Gabon">Gabon</option>
      <option value="Gambia">Gambia</option>
      <option value="Georgia">Georgia</option>
      <option value="Germany">Germany</option>
      <option value="Ghana">Ghana</option>
      <option value="Gibraltar">Gibraltar</option>
      <option value="Greece">Greece</option>
      <option value="Greenland">Greenland</option>
      <option value="Grenada">Grenada</option>
      <option value="Guadeloupe">Guadeloupe</option>
      <option value="Guam">Guam</option>
      <option value="Guatemala">Guatemala</option>
      <option value="Guernsey">Guernsey</option>
      <option value="Guinea">Guinea</option>
      <option value="Guinea-bissau">Guinea-bissau</option>
      <option value="Guyana">Guyana</option>
      <option value="Haiti">Haiti</option>
      <option value="Heard Island and Mcdonald Islands">
        Heard Island and Mcdonald Islands
      </option>
      <option value="Holy See (Vatican City State)">
        Holy See (Vatican City State)
      </option>
      <option value="Honduras">Honduras</option>
      <option value="Hong Kong">Hong Kong</option>
      <option value="Hungary">Hungary</option>
      <option value="Iceland">Iceland</option>
      <option value="India">India</option>
      <option value="Indonesia">Indonesia</option>
      <option value="Iran, Islamic Republic of">
        Iran, Islamic Republic of
      </option>
      <option value="Iraq">Iraq</option>
      <option value="Ireland">Ireland</option>
      <option value="Isle of Man">Isle of Man</option>
      <option value="Israel">Israel</option>
      <option value="Italy">Italy</option>
      <option value="Jamaica">Jamaica</option>
      <option value="Japan">Japan</option>
      <option value="Jersey">Jersey</option>
      <option value="Jordan">Jordan</option>
      <option value="Kazakhstan">Kazakhstan</option>
      <option value="Kenya">Kenya</option>
      <option value="Kiribati">Kiribati</option>
      <option value="Korea, Democratic People's Republic of">
        Korea, Democratic People's Republic of
      </option>
      <option value="Korea, Republic of">Korea, Republic of</option>
      <option value="Kuwait">Kuwait</option>
      <option value="Kyrgyzstan">Kyrgyzstan</option>
      <option value="Lao People's Democratic Republic">
        Lao People's Democratic Republic
      </option>
      <option value="Latvia">Latvia</option>
      <option value="Lebanon">Lebanon</option>
      <option value="Lesotho">Lesotho</option>
      <option value="Liberia">Liberia</option>
      <option value="Libyan Arab Jamahiriya">Libyan Arab Jamahiriya</option>
      <option value="Liechtenstein">Liechtenstein</option>
      <option value="Lithuania">Lithuania</option>
      <option value="Luxembourg">Luxembourg</option>
      <option value="Macao">Macao</option>
      <option value="Macedonia, The Former Yugoslav Republic of">
        Macedonia, The Former Yugoslav Republic of
      </option>
      <option value="Madagascar">Madagascar</option>
      <option value="Malawi">Malawi</option>
      <option value="Malaysia">Malaysia</option>
      <option value="Maldives">Maldives</option>
      <option value="Mali">Mali</option>
      <option value="Malta">Malta</option>
      <option value="Marshall Islands">Marshall Islands</option>
      <option value="Martinique">Martinique</option>
      <option value="Mauritania">Mauritania</option>
      <option value="Mauritius">Mauritius</option>
      <option value="Mayotte">Mayotte</option>
      <option value="Mexico">Mexico</option>
      <option value="Micronesia, Federated States of">
        Micronesia, Federated States of
      </option>
      <option value="Moldova, Republic of">Moldova, Republic of</option>
      <option value="Monaco">Monaco</option>
      <option value="Mongolia">Mongolia</option>
      <option value="Montenegro">Montenegro</option>
      <option value="Montserrat">Montserrat</option>
      <option value="Morocco">Morocco</option>
      <option value="Mozambique">Mozambique</option>
      <option value="Myanmar">Myanmar</option>
      <option value="Namibia">Namibia</option>
      <option value="Nauru">Nauru</option>
      <option value="Nepal">Nepal</option>
      <option value="Netherlands">Netherlands</option>
      <option value="Netherlands Antilles">Netherlands Antilles</option>
      <option value="New Caledonia">New Caledonia</option>
      <option value="New Zealand">New Zealand</option>
      <option value="Nicaragua">Nicaragua</option>
      <option value="Niger">Niger</option>
      <option value="Nigeria">Nigeria</option>
      <option value="Niue">Niue</option>
      <option value="Norfolk Island">Norfolk Island</option>
      <option value="Northern Mariana Islands">Northern Mariana Islands</option>
      <option value="Norway">Norway</option>
      <option value="Oman">Oman</option>
      <option value="Pakistan">Pakistan</option>
      <option value="Palau">Palau</option>
      <option value="Palestinian Territory, Occupied">
        Palestinian Territory, Occupied
      </option>
      <option value="Panama">Panama</option>
      <option value="Papua New Guinea">Papua New Guinea</option>
      <option value="Paraguay">Paraguay</option>
      <option value="Peru">Peru</option>
      <option value="Philippines">Philippines</option>
      <option value="Pitcairn">Pitcairn</option>
      <option value="Poland">Poland</option>
      <option value="Portugal">Portugal</option>
      <option value="Puerto Rico">Puerto Rico</option>
      <option value="Qatar">Qatar</option>
      <option value="Reunion">Reunion</option>
      <option value="Romania">Romania</option>
      <option value="Russian Federation">Russian Federation</option>
      <option value="Rwanda">Rwanda</option>
      <option value="Saint Helena">Saint Helena</option>
      <option value="Saint Kitts and Nevis">Saint Kitts and Nevis</option>
      <option value="Saint Lucia">Saint Lucia</option>
      <option value="Saint Pierre and Miquelon">
        Saint Pierre and Miquelon
      </option>
      <option value="Saint Vincent and The Grenadines">
        Saint Vincent and The Grenadines
      </option>
      <option value="Samoa">Samoa</option>
      <option value="San Marino">San Marino</option>
      <option value="Sao Tome and Principe">Sao Tome and Principe</option>
      <option value="Saudi Arabia">Saudi Arabia</option>
      <option value="Senegal">Senegal</option>
      <option value="Serbia">Serbia</option>
      <option value="Seychelles">Seychelles</option>
      <option value="Sierra Leone">Sierra Leone</option>
      <option value="Singapore">Singapore</option>
      <option value="Slovakia">Slovakia</option>
      <option value="Slovenia">Slovenia</option>
      <option value="Solomon Islands">Solomon Islands</option>
      <option value="Somalia">Somalia</option>
      <option value="South Africa">South Africa</option>
      <option value="South Georgia and The South Sandwich Islands">
        South Georgia and The South Sandwich Islands
      </option>
      <option value="Spain">Spain</option>
      <option value="Sri Lanka">Sri Lanka</option>
      <option value="Sudan">Sudan</option>
      <option value="Suriname">Suriname</option>
      <option value="Svalbard and Jan Mayen">Svalbard and Jan Mayen</option>
      <option value="Swaziland">Swaziland</option>
      <option value="Sweden">Sweden</option>
      <option value="Switzerland">Switzerland</option>
      <option value="Syrian Arab Republic">Syrian Arab Republic</option>
      <option value="Taiwan">Taiwan</option>
      <option value="Tajikistan">Tajikistan</option>
      <option value="Tanzania, United Republic of">
        Tanzania, United Republic of
      </option>
      <option value="Thailand">Thailand</option>
      <option value="Timor-leste">Timor-leste</option>
      <option value="Togo">Togo</option>
      <option value="Tokelau">Tokelau</option>
      <option value="Tonga">Tonga</option>
      <option value="Trinidad and Tobago">Trinidad and Tobago</option>
      <option value="Tunisia">Tunisia</option>
      <option value="Turkey">Turkey</option>
      <option value="Turkmenistan">Turkmenistan</option>
      <option value="Turks and Caicos Islands">Turks and Caicos Islands</option>
      <option value="Tuvalu">Tuvalu</option>
      <option value="Uganda">Uganda</option>
      <option value="Ukraine">Ukraine</option>
      <option value="United Arab Emirates">United Arab Emirates</option>
      <option value="United Kingdom">United Kingdom</option>
      <option value="United States">United States</option>
      <option value="United States Minor Outlying Islands">
        United States Minor Outlying Islands
      </option>
      <option value="Uruguay">Uruguay</option>
      <option value="Uzbekistan">Uzbekistan</option>
      <option value="Vanuatu">Vanuatu</option>
      <option value="Venezuela">Venezuela</option>
      <option value="Viet Nam">Viet Nam</option>
      <option value="Virgin Islands, British">Virgin Islands, British</option>
      <option value="Virgin Islands, U.S.">Virgin Islands, U.S.</option>
      <option value="Wallis and Futuna">Wallis and Futuna</option>
      <option value="Western Sahara">Western Sahara</option>
      <option value="Yemen">Yemen</option>
      <option value="Zambia">Zambia</option>
      <option value="Zimbabwe">Zimbabwe</option>
    </select>
  </uk-select>
</div>
```

## Custom keywords

Sometimes, there are items that have related keywords that may be slightly off or awkward when included as anchor tags. For these use cases, we can leverage the `data-keywords` attribute.

For example, if we have a "Form" link but also want it to appear when users search for terms like "checkbox," "input," "toggle switch," etc., we can simply add a comma-separated list of terms like this: `data-keywords="apple, mango, lemon"`.

### Example

```html
<div class="h-10">
  <uk-select
    cls-custom="button: uk-input-fake w-full; dropdown: w-full"
    name="option"
    searchable
  >
    <select hidden>
      <option data-keywords="apple, mango, lemon" value="option1">
        Option 1
      </option>
      <option value="option2">Option 2</option>
      <option value="option3">Option 3</option>
      <option value="option4">Option 4</option>
      <option value="option5">Option 5</option>
    </select>
  </uk-select>
</div>
```

## Disable input

To prevent user input, add the `disabled` attribute to the `<uk-select>` element. This will disable the custom select, making it impossible for users to enter or modify its value.

### Example

```html
<div class="h-10">
  <uk-select
    cls-custom="button: uk-input-fake w-full; dropdown: w-full"
    disabled
  >
    <select hidden>
      <option value="apple">Apple</option>
      <option value="apricot">Apricot</option>
      <option value="avocado" selected>Avocado</option>
      <option value="ackee">Ackee</option>
      <option value="asian_pear">Asian Pear</option>
      <option value="abiu">Abiu</option>
      <option value="ambarella">Ambarella</option>
    </select>
  </uk-select>
</div>
```

## Error state

To indicate an error state in the form, simply add the `.uk-form-destructive` class to the `cls-custom` attribute. This will apply a "destructive" state to the component, providing visual feedback to the user.

### Example

```html
<div class="space-y-1.5">
  <label class="uk-form-label text-destructive">Select an option</label>
  <div class="uk-form-controls">
    <div class="h-10">
      <uk-select
        cls-custom="button: uk-input-fake uk-form-destructive w-full; dropdown: w-full"
      >
        <select hidden>
          <option value="option1">Option 1</option>
          <option value="option2">Option 2</option>
          <option value="option3">Option 3</option>
          <option value="option4">Option 4</option>
          <option value="option5">Option 5</option>
        </select>
      </uk-select>
    </div>
  </div>
  <p class="uk-form-help text-destructive">This field is required.</p>
</div>
```

## Preventing layout shift

When loading Web Components, a brief delay may cause a flash of unstyled content. To mitigate this issue, consider setting a predefined height on the parent element to prevent layout shift and ensure a smooth user experience.

```html
<div class="h-10">
  <uk-select>
    <!-- ... -->
  </uk-select>
</div>
```

## Internationalization

### Example

```html
<div class="h-10">
  <uk-select
    cls-custom="button: uk-input-fake w-full; dropdown: w-full"
    i18n="search-placeholder: 検索; selection-count: :n: つのオプションが選択されました"
    multiple
    placeholder="オプションを選択"
    searchable
  >
    <select hidden>
      <option value="option1">オプション 1</option>
      <option value="option2">オプション 2</option>
      <option value="option3">オプション 3</option>
      <option value="option4">オプション 4</option>
      <option value="option5">オプション 5</option>
    </select>
  </uk-select>
</div>
```

## Available options

| Name                 | Description                                                                                                              |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| `selection-count`    | Displays a customizable message, e.g. ":n: つのオプションが選択されました", where :n: is the number of selected options. |
| `search-placeholder` | The placeholder for the search box.                                                                                      |

## Attributes

The following attributes are available for this component:

| Name                     | Type    | Default | Description                                                                                                                                                        |
| ------------------------ | ------- | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `insertable`             | Boolean | false   | Allows users to add new options that aren't in the original list.                                                                                                  |
| `force-prevent-rerender` | Boolean | false   | Forcefully prevents component rerendering.                                                                                                                         |
| `name`                   | String  |         | Specifies the name of the input field.                                                                                                                             |
| `multiple`               | Boolean | false   | Determines whether the component accepts multiple values or not.                                                                                                   |
| `disabled`               | Boolean | false   | Enables or disables the entire component.                                                                                                                          |
| `placeholder`            | String  |         | Sets the placeholder text for the component.                                                                                                                       |
| `searchable`             | Boolean | false   | Adds a search input field within the dropdown menu, allowing users to search for specific options.                                                                 |
| `cls-custom`             | String  |         | Allows you to add custom CSS classes.                                                                                                                              |
| `i18n`                   | String  |         | Enables internationalization. Please see [Internationalization](#internationalization) for available options.                                                      |
| `reactive`               | Boolean | false   | Enables reactivity by using `MutationObserver` to monitor the referenced `<select hidden>` element for changes, triggering updates to the `<uk-select>` component. |
| `value`                  | String  |         | A comma-separated list of values that will be prepopulated in the input field.                                                                                     |
| `icon`                   | String  |         | Sets a customized icon. If no icon is passed, it will default to a chevron down icon.                                                                              |
| `drop`                   | String  |         | Customize the dropping option for the dropdown. See [Drop](https://franken-ui.dev/docs/2.1/drop) component for more options.                                                             |

## Events

The custom select component triggers the following events on elements with this component attached:

| Name               | Description                                                                           |
| ------------------ | ------------------------------------------------------------------------------------- |
| `uk-select:input`  | Fired after the value has changed, providing an opportunity to respond to user input. |
| `uk-select:search` | Fired after the value inside search box has changed.                                  |
