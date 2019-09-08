---
title: Azir Switch
description:
---

# Switch

An advance Switch component that should render nicely on any platform. Supports a great level of customization.

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
import { Switch } from "azir-radio";
---
<Switch
  id="1"
  value="5"
  onChange={event => {
    console.log(event);
  }}>
  Nice Switch :)
</Switch>
```

<img src="https://i.imgur.com/x6aoTmo.jpg" alt="Basic" style="width:250px" />

#### Custom Icons

```jsx
import { Switch } from "azir-radio";
import  { AzirIcons } from "azir-icon";
---
<Switch
  id="1"
  value="5"
  onChange={event => {
    console.log(event);
  }}
  iconActive={AzirIcons.switchOn}
  iconInActive={AzirIcons.switchOff}
  hideInActiveIcon={false}
  checked
>
  Custom Switch !
</Switch>

<Switch
  id="1"
  value="5"
  onChange={event => {
    console.log(event);
  }}
  iconActive={AzirIcons.switchOn1}
  iconInActive={AzirIcons.switchOff1}
  hideInActiveIcon={false}
  checked
>
  Custom Switch !
</Switch>
```

<img src="https://i.imgur.com/ueOYuk2.jpg" alt="with icon" style="width:250px" />

### Props

- [`id`](switch#id)
- [`value`](switch#value)
- [`onChange`](switch#onchange)
- [`disabled`](switch#disabled)
- [`checked`](switch#checked)
- [`flexDirection`](switch#flexdirection)
- [`size`](switch#size)
- [`hideLable`](switch#hidelable)
- [`textActiveColor`](switch#textactivecolor)
- [`textInActiveColor`](switch#textinactivecolor)
- [`textDisabledColor`](switch#textdisabledcolor)
- [`iconActive`](switch#iconactive)
- [`iconInActive`](switch#iconinactive)
- [`iconActiveColor`](switch#iconactivecolor)
- [`iconInActiveColor`](switch#iconinactivecolor)
- [`icondisabledcolor`](switch#icondisabledcolor)
- [`hideInActiveIcon`](switch#hideinactiveicon)
- [`hideIconBorder`](switch#hideiconborder)
- [`style`](switch#style)
- [`textStyle`](switch#textstyle)
- [`iconStyle`](switch#iconstyle)

---

# Reference

### `id`

the id of your component.

| Type   | Required |
| ------ | -------- |
| string | Yes      |

### `value`

the value property do not appear in the user interface.The value property only has meaning when you click on the component and you want to receive the value for which switch has been selected.

| Type   | Required |
| ------ | -------- |
| string | Yes      |

### `onChange`

Handler to be called when the user click the the component ; passes the event as an argument.

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

flexDirection controls which directions children of a container go.(switch icon, and label) row goes left to right, column goes top to bottom

| Type                                             | Required | Default |
| ------------------------------------------------ | -------- | ------- |
| 'row', 'row-reverse', 'column', 'column-reverse' | No       | row     |

### `size`

set the size of the icon .

| Type   | Required | Default                   |
| ------ | -------- | ------------------------- |
| Number | No       | BETheme.SIZES.SWITCH_SIZE |

### `hideLable`

Hide switch label when it set to true . or you simply not pass text children to the switch component.

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

if you want to change the default icon of the switch button when its active, you need just to pass the new icon name using this prop.

| Type                                                                        | Required | Default                          |
| --------------------------------------------------------------------------- | -------- | -------------------------------- |
| [azir-icon (SolidIcons, RegularIcons, BrandIcons,customIcons)](icon#icon-1) | No       | AzirTheme.STRINGS.SWITCH_ICON_ON |

### `iconInActive`

if you want to change the default icon of the switch button when its inActive, you need just to pass the new icon name using this prop.

| Type                                                                        | Required | Default                           |
| --------------------------------------------------------------------------- | -------- | --------------------------------- |
| [azir-icon (SolidIcons, RegularIcons, BrandIcons,customIcons)](icon#icon-1) | No       | AzirTheme.STRINGS.SWITCH_ICON_OFF |

### `iconActiveColor`

the color of the switch icon and its border when its checked .

| Type                                       | Required | Default |
| ------------------------------------------ | -------- | ------- |
| [azir-color](../../guides/color-reference) | No       | theme   |

### `iconInActiveColor`

the color of the switch icon and its border when its unchecked .

| Type                                       | Required | Default              |
| ------------------------------------------ | -------- | -------------------- |
| [azir-color](../../guides/color-reference) | No       | BETheme.COLORS.BLACK |

### `iconDisabledColor`

the color of the switch icon and its border when its disabled .

| Type                                       | Required | Default              |
| ------------------------------------------ | -------- | -------------------- |
| [azir-color](../../guides/color-reference) | No       | BETheme.COLORS.MUTED |

### `hideInActiveIcon`

by default when switch button is uncheced we only show the border and hide the icon by default.if you want to keep the icon when the switch is unchecked you need to set the prop to false.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | true    |

### `hideIconBorder`

by default we show the switch icon border , this is very important in the case hideInActiveIcon set to true.if you dont like to show the icon border just set this prop to true.

| Type | Required | Default |
| ---- | -------- | ------- |
| bool | No       | false   |

### `style`

override switch button (label + icon) container style for example if you want to change width,height,padding,....

| Type  | Required |
| ----- | -------- |
| style | No       |

### `textStyle`

override switch button label style for example if you want to change fontSize,....

| Type  | Required |
| ----- | -------- |
| style | No       |

### `iconStyle`

override switch button icon style for example if you want to change borderRadius,....

| Type  | Required |
| ----- | -------- |
| style | No       |
