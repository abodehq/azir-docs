---
title: Azir Text
description:
---

# Text

An advance Text component for displaying text. Azir Text supports nesting, styling, and touch handling.

> we have also add Pixel–perfect, native–looking [Typographic styles](texttypography) for React Native.

<p align="center">
 <img src="https://i.imgur.com/jUQLsA2.jpg" />
</p>

## Installation

to install the latest version of `azir-text` you only need to run:

```bash
npm install azir-text  --save
```

or

```bash
yarn add azir-text
```

> We provide a series of predefined collections for you to start with that match the native design systems for iOS and Android. You can use them directly wherever you would supply a textStyle. [Text Typography](texttypography)

**Examples**

#### Example

```jsx
import Text from "azir-text";
---
<Text
    h1
    italic
    bold
    center
    color="error"
    style={ { textDecorationLine: "underline" } }
    onPress={() => {
        console.log("Text Pressed");
    }}
    >
    I am bold & <Text color="success">Green</Text>
</Text>
```

<img src="https://i.imgur.com/yqJZHzb.jpg" alt="Basic" style="width:250px" />

### Props

- [`color`](text#color)
- [`bold`](text#bold)
- [`italic`](text#italic)
- [`center`](text#center)
- [`size`](text#size)
- [`style`](text#style)

---

# Reference

### `color`

Text Color

| Type                                       | Required | Default |
| ------------------------------------------ | -------- | ------- |
| [azir-color](../../guides/color-reference) | No       | theme   |

### `Azir Text Sizes`

> you can pass any of these text sizes props., typography styles have more priority than these props.

| Prop | type    | Default                           |
| ---- | ------- | --------------------------------- |
| h1   | boolean | Sets the text's fontSize to 44px. |
| h2   | boolean | Sets the text's fontSize to 38px. |
| h3   | boolean | Sets the text's fontSize to 30px. |
| h4   | boolean | Sets the text's fontSize to 24px. |
| h5   | boolean | Sets the text's fontSize to 18px. |
| p    | boolean | Sets the text's fontSize to 16px. |

### `bold`

add bold to text font style , typography styles have more priority than this prop.

| Type    | Required | Default |
| ------- | -------- | ------- |
| boolean | No       | false   |

### `italic`

add italic to text font style .

| Type    | Required | Default |
| ------- | -------- | ------- |
| boolean | No       | false   |

### `center`

align text to center .

| Type    | Required | Default |
| ------- | -------- | ------- |
| boolean | No       | false   |

### `size`

override text size Size, this will ovveride any premade font sizes like h1,h2 or even typography font size.

| Type   | Required | Default              |
| ------ | -------- | -------------------- |
| number | No       | AzirTheme.SIZES.FONT |

### `style`

override text style for example if you want to change fontSize,textDecorationLine,...

| Type  | Required |
| ----- | -------- |
| style | No       |

> **You Still can pass any of react native Text Props**
