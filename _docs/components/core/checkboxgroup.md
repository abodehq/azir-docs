---
title: Blue Eye CheckBox Group
description:
---

# CheckboxGroup

An advance component used to create a multiple-exclusion scope for a set of CheckBox buttons.

> for great customization you can pass your custom CheckBox button template component as a child to the CheckBox Group component ;)

## Installation

to install the latest version of `be-radio` you only need to run:

> this package incluse also : **(Radio, Switch, CheckBox, RadioGroup, CheckboxGroup )**

```bash
npm install be-radio --save
```

or

```bash
yarn add be-radio
```

**Examples**

#### Basic

```jsx
import { CheckBox, CheckboxGroup } from "be-radio";
---
<CheckboxGroup
  onChange={event => {
    console.log(event);
  }}
  style={ { flexWrap: "wrap" } }
  flexDirection="row"
  options={[
    {
      id: "1",
      value: "React",
      checked: true,
      disabled: false
    },
    {
      id: "2",
      value: "Angular",
      checked: false,
      disabled: false
    },
    {
      id: "3",
      value: "c#",
      checked: true,
      disabled: false
    },
    {
      id: "4",
      value: "php",
      checked: false,
      disabled: false
    },
    {
      id: "5",
      value: "java",
      checked: true,
      disabled: false
    }
  ]}
>
  <CheckBox style={ { padding: 10 } } />
</CheckboxGroup>
```

<img src="https://i.imgur.com/IycnPvz.jpg" alt="Basic" style="width:350px" />

### Props

- [`options`](checkboxgroup#options)
- [`onChange`](checkboxgroup#onchange)
- [`flexDirection`](checkboxgroup#flexdirection)
- [`style`](checkboxgroup#style)

---

# Reference

### `options`

an array of options that will pass to the radio group component to render the radios.check the example above.

| Type                                                                              | Required | Default |
| --------------------------------------------------------------------------------- | -------- | ------- |
| interface IOptions {id: string;value: string;checked: boolean;disabled: boolean;} | Yes      | []      |

### `onChange`

Handler to be called when the user click one of the unselected radio buttons ; passes the event as an argument.

Event object contains two objects :

1. **options** array which contains all the informations about all the buttons.
2. **target** the radio button object which clicked by user.

```jsx
Event {
  "options": Array [
    Object {
      "checked": true,
      "disabled": false,
      "id": "1",
      "value": "React",
    },
    Object {
      "checked": false,
      "disabled": false,
      "id": "2",
      "value": "Angular",
    },
    Object {
      "checked": false,
      "disabled": false,
      "id": "3",
      "value": "c#",
    },
    Object {
      "checked": false,
      "disabled": false,
      "id": "4",
      "value": "php",
    },
    Object {
      "checked": false,
      "disabled": false,
      "id": "5",
      "value": "java",
    },
  ],
  "target": Object {
    "checked": true,
    "id": "1",
    "value": "React",
  },
}
```

| Type     | Required |
| -------- | -------- |
| function | Yes      |

### `flexDirection`

flexDirection controls which directions children of a container go.(radio buttons) row goes left to right, column goes top to bottom

| Type                                             | Required | Default |
| ------------------------------------------------ | -------- | ------- |
| 'row', 'row-reverse', 'column', 'column-reverse' | No       | row     |

### `style`

override checkboxgroup container style for example if you want to change flexWrap if you have many radios ....

| Type  | Required |
| ----- | -------- |
| style | No       |
