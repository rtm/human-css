Attributes
======

This page lists the available Human CSS attributes and the meaning and values of each.

Text
----

The text micro-attribute provides control over text color, fonts, alignment, and so on.
It is introduced by the micro-attribute `text`.
`text` takes values for color,
font size using standard synonyms such as `large` (or any length),
font weight using standard synonyms such as `bold`,
and others.

Other text attribute values include `italic`, `underline`, `upper`, `lower`, `capitalize`, `small-caps`, and so on.

Borders, margins, outlines, and padding
---------------------------------------

Borders, margins, outlines, and padding are specified by the `border`, `margin`, `outline`, and `padding` micro-attributes.
The attribute values `top`, `left`, `bottom`, and `right` may be given to indicate which side or sides are to be affected.
A number or length, or keyword such as `thick` or `thin`,  specifies the size of the border, margin, outline, or padding.
For borders and outlines, the standard types such as `solid` and `dotted` are available as micro-attributes.
Colors may also be specified for borders and padding.

Background
----------

The `background` micro-atteribute provides a background of the specified color.

```html
<div background="x-light blue color"></d
```

Sizes
-----

Box sizes are indicated with micro-attributes such as `width` and `height`,
which are given together with other micro-attributes indicating the size,
as a length, percentage, or keyword such as `half`.

```html
<div half width></div>
<div 40% height></div>
<div max-height 50 vh></div>
```

Box
---

The `box` micro-attribute specifies styling related to boxes,
including position (`absolute` etc.),
display (`hidden`),
vertical alignment,
`visible` and `invisible`,
box sizing ('border` or `content`), and so on.

Spacing
-------

People commonly use top margins and bottom margins and top padding and bottom padding and special spacing elements
to space out their elements.
Human CSS classes provide a simple mechanisms for controlling spacing.
The `spaced` micro-attribute adds space between child elements.
Variants of these (indicated by modifier micro-attributes) provide more or less spacing.

Example of spaced children:

```html
<div spaced>
  <div></div>
  <div></div>
</div>
```


Opacity
-------

```html
<div opaque></div>
<div semi-opaque></div>
<div transparent></div>
<div opacity 0.8></div>
```

## Z-index

```html
<div back></div>
<div front></div>
<div backmost></div>
<div frontmost></div>
```

## Position

```html
<div absolute></div>
<div relative></div>
<div fixed></div>
```

## Transitions

THe `transition` micro-attribute provides a streamlined interface for simple transitions.

```html
<div transition="fast linear delay"></div>
```

## White space

Human CSS redefines the factors involved in white space control,
making it easier to remember and specify your desired behavior.
The CSS property values each indicate a combination of whether newlines are to be honored,
whether whitespace is to be preserved, and whether wrapping is desired.

These human CSS micro-attribute values map those concepts into `white-space` values,
so hopefully you'll never have to consult that page again.

### Values

#### `newlines`

Honor newlines.

#### `spaces`

Preserve spaces and tabs.

#### `nowrap`

Do not wrap (other than at newlines, if they are being honored).

### Usages

#### `whitespace="newlines spaces nowrap"`

This is the classical `white-space: pre` case.
It is appropriate for code fragments.

#### `whitespace='newlines`

This corresponds to `pre-line`, which is like `pre`, but spaces and tabs will be collapsed.
This is suitable for the common case of displaying a user post.

#### `whitespace="newlines spaces"`

Newlines are honored, spaces preserved, and wrapping occurs, meaning that output may extend to multiple lines,
this is equivalent to `white-space: pre-wrap`.

#### `whitespace="nowrap"`

This is equivalent to `white-space: nowrap`.
Therefore, all output will be on a single line.
In this case, whitespace is never preserved.

Note that CSS offers no alternative for preserving whitespace while not honoring newlines and not wrapping.
