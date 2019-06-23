Colors
======

Human CSS allows you to easily think of colors in terms of their hue, lightness, and saturation,
using micro-attribute values for hues (`red`), as well as saturations such as ``bright` and ligthnesses such as `dark`.
This is the so-called ["HSL" model](https://en.wikipedia.org/wiki/HSL_and_HSV).
It makes it easy to implement coordinated color schemes.

```html
<span text="dark red color">
```

The HSL model in terms of which colors are specified
allows you to easily think of colors in terms of their hue, lightness, and saturation.
The standard hues are red, orange, yellow, lime, green, aquamarine, cyan, azure, blue, purple, magenta, and pink.
The hues can then be combined with additional micro-class values for saturation,
including `xx-bright`, `x-bright`, `bright`, `dull`, `x-dull`, and `xx-dull`,
and with additional micro-attributes for lightness,
including `xx-light` (white, essentially), `x-light`, `light`, `dark`, `x-dark`, and `xx-dark` (black, essentially).

There is a special attribute `color` which has no immediate effect.
Instead, it sets global color values.
For example, `color="red"` sets the global hue to red.

To actually apply this color to text, for example,
use the `color` keyword in conjunction with the `text` attribute.
For example, the following will yield a thick red bordered div, with lighter red text:

```
<div color='red">
  <div border="thick darker color">
    <div text="lighter color">
```

The color components may also be modified in relatively terms using
`brighter`, `duller`, `lighter`, or `darker`,
or corresponding versions prefixed with `x-`.
In the case of border, for example, you might say `border="lighter blue color"`.

Human CSS does not directly support HTML colors.
To use HTML colors, apply them yourself via normal CSS mechanisms.
