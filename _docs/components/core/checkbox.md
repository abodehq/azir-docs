---
title: Azir checkBox
description:
---

# Checkbox

An advance CheckBox component that should render nicely on any platform. Supports a great level of customization.

## Installation

to install the latest version of `azir-radio` you only need to run:

> this package incluse also : **(Radio, Switch, CheckBox, RadioGroup, CheckboxGroup )**

```bash
npm install azir-radio --save
```

or

```bash
yarn add azir-radio
```

**Examples**

#### Basic

```jsx
import { CheckBox } from "azir-radio";
---
<CheckBox
  id="1"
  value="5"
  onChange={event => {
    console.log(event);
  }}>
  Nice CheckBox :)
</CheckBox>
```

<img src="https://i.imgur.com/CsdyH5B.jpg" alt="Basic" style="width:250px" />

#### Advance

```jsx
import { CheckBox } from "azir-radio";
---
<CheckBox
  id="1"
  value="5"
  onChange={event => {
    console.log(event);
  }}
  checked
  hideIconBorder={true}
  size={60}
  iconActiveColor="success"
  textActiveColor="#00ff00"
  textStyle={ { fontSize: 18 } }>
  active  :)
</CheckBox>
<CheckBox
  id="2"
  value="10"
  onChange={event => {
    console.log(event);
  }}
  checked={false}
  hideInActiveIcon={false}
  hideLable={false}
  size={30}
  iconInActiveColor="red"
  textInActiveColor="theme"
  textStyle={ { fontSize: 14 } }
  iconStyle={ { borderRadius: 0 } }
  style={ { borderWidth: 1, borderColor: "#ff9900", padding: 5 } }>
  inactive  :(
</CheckBox>
```

<img src="https://i.imgur.com/FkMZffs.jpg" alt="Basic" style="width:250px" />

#### Custom Icons

```jsx
import { CheckBox } from "azir-radio";
import  { SolidIcons } from "azir-icon";
---
 <CheckBox
  id="1"
  value="5"
  onChange={event => {
    console.log(event);
  }}
  iconActive={SolidIcons.checkDouble}
  iconInActive={SolidIcons.checkDouble}
  hideInActiveIcon={false}
  checked
>
  Box
</CheckBox>
```

<img src="https://i.imgur.com/nk5xPPY.jpg" alt="Basic" style="width:150px" />

### Props

- [`id`](checkbox#id)
- [`value`](checkbox#value)
- [`onChange`](checkbox#onchange)
- [`disabled`](checkbox#disabled)
- [`checked`](checkbox#checked)
- [`flexDirection`](checkbox#flexdirection)
- [`size`](checkbox#size)
- [`hideLable`](checkbox#hidelable)
- [`textActiveColor`](checkbox#textactivecolor)
- [`textInActiveColor`](checkbox#textinactivecolor)
- [`textDisabledColor`](checkbox#textdisabledcolor)
- [`iconActive`](checkbox#iconactive)
- [`iconInActive`](checkbox#iconinactive)
- [`iconActiveColor`](checkbox#iconactivecolor)
- [`iconInActiveColor`](checkbox#iconinactivecolor)
- [`icondisabledcolor`](checkbox#icondisabledcolor)
- [`hideInActiveIcon`](checkbox#hideinactiveicon)
- [`hideIconBorder`](checkbox#hideiconborder)
- [`style`](checkbox#style)
- [`textStyle`](checkbox#textstyle)
- [`iconStyle`](checkbox#iconstyle)

---

# Reference

### `id`

the id of your component, should be unique when u use checkBoxGroup.

| Type   | Required |
| ------ | -------- |
| string | Yes      |

### `value`

the value property do not appear in the user interface.The value property only has meaning when you click on the component and you want to receive the value for which checkBox has been selected.

| Type   | Required |
| ------ | -------- |
| string | Yes      |

### `onChange`

Handler to be called when the user click the the component, ; passes the event as an argument.

```jsx
Event Object {
  "checked": false,
  "id": "1",
  "value": "5",
}
```

| Type     | Required |
| -------- | -------- |
| function | Yes      |

### `disabled`

If true, disable all interactions for this component.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | false   |

### `checked`

the default state if it checked or not .

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | false   |

### `flexDirection`

flexDirection controls which directions children of a container go.(checkBox icon, and label) row goes left to right, column goes top to bottom

| Type                                             | Required | Default |
| ------------------------------------------------ | -------- | ------- |
| 'row', 'row-reverse', 'column', 'column-reverse' | No       | row     |

### `size`

set the size of the icon .

| Type   | Required | Default                 |
| ------ | -------- | ----------------------- |
| Number | No       | BETheme.SIZES.ICON_SIZE |

### `hideLable`

Hide checkBox label when it set to true . or you simply not pass text children to the checkBox component.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | false   |

### `textActiveColor`

the text color of the component label when its checked .

| Type                                       | Required | Default |
| ------------------------------------------ | -------- | ------- |
| [azir-color](../../guides/color-reference) | No       | theme   |

### `textInActiveColor`

the text color of the component label when its unchecked .

| Type                                       | Required | Default              |
| ------------------------------------------ | -------- | -------------------- |
| [azir-color](../../guides/color-reference) | No       | BETheme.COLORS.BLACK |

### `textDisabledColor`

the text color of the component label when its disabled .

| Type                                       | Required | Default              |
| ------------------------------------------ | -------- | -------------------- |
| [azir-color](../../guides/color-reference) | No       | BETheme.COLORS.MUTED |

### `iconActive`

if you want to change the default icon of the checkBox button when its active, you need just to pass the new icon name using this prop.

| Type                                                                        | Required | Default                                 |
| --------------------------------------------------------------------------- | -------- | --------------------------------------- |
| [azir-icon (SolidIcons, RegularIcons, BrandIcons,customIcons)](icon#icon-1) | No       | AzirTheme.STRINGS.CHECKBOX_DEFAULT_ICON |

### `iconInActive`

if you want to change the default icon of the checkBox button when its inActive, you need just to pass the new icon name using this prop.

| Type                                                                        | Required | Default                                 |
| --------------------------------------------------------------------------- | -------- | --------------------------------------- |
| [azir-icon (SolidIcons, RegularIcons, BrandIcons,customIcons)](icon#icon-1) | No       | AzirTheme.STRINGS.CHECKBOX_DEFAULT_ICON |

### `iconActiveColor`

the color of the checkBox icon and its border when its checked .

| Type                                       | Required | Default |
| ------------------------------------------ | -------- | ------- |
| [azir-color](../../guides/color-reference) | No       | theme   |

### `iconInActiveColor`

the color of the checkBox icon and its border when its unchecked .

| Type                                       | Required | Default              |
| ------------------------------------------ | -------- | -------------------- |
| [azir-color](../../guides/color-reference) | No       | BETheme.COLORS.BLACK |

### `iconDisabledColor`

the color of the checkBox icon and its border when its disabled .

| Type                                       | Required | Default              |
| ------------------------------------------ | -------- | -------------------- |
| [azir-color](../../guides/color-reference) | No       | BETheme.COLORS.MUTED |

### `hideInActiveIcon`

by default when checkBox button is uncheced we only show the border and hide the icon by default.if you want to keep the icon when the checkBox is unchecked you need to set the prop to false.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | true    |

### `hideIconBorder`

by default we show the checkBox icon border , this is very important in the case hideInActiveIcon set to true.if you dont like to show the icon border just set this prop to true.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | false   |

### `style`

override checkBox button (label + icon) container style for example if you want to change width,height,padding,....

| Type  | Required |
| ----- | -------- |
| style | No       |

### `textStyle`

override checkBox button label style for example if you want to change fontSize,....

| Type  | Required |
| ----- | -------- |
| style | No       |

### `iconStyle`

override checkBox button icon style for example if you want to change borderRadius,....

| Type  | Required |
| ----- | -------- |
| style | No       |
