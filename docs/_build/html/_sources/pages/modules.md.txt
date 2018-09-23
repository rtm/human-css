Modules
======

This documentation groups the micro-attributes into modules.

Text
----

The text micro-attribute grouping provides control over text color, fonts, alignment, and so on.
It is introduced by the micro-attribute `text`.
`text` is combined with micro-attributes for color,
font size using standard synonyms such as `large` (or any length),
font weight using standard synonyms such as `bold`, and others.

Other text features include `italic`, `underline`, `upper`, `lower`, `capitalize`, `small-caps`, and so on.

Borders, margins, outlines, and padding
---------------------------------------

Borders, margins, outlines, and padding are introduced by the `border`, `margin`, `outline`, and `padding` micro-attributes.
The attributes `top`, `left`, `bottom`, and `right` may be given to indicate which side or sides are to be affected.
A number or length, or keyword such as `thick` or `thin`,  specifies the size of the border, margin, outline, or padding.
For borders and outlines, the standard types such as `solid` and `dotted` are available as micro-attributes.
Colors may also be specified for borders and padding.

Background
----------

The `background` micro-atteribute provides a background of the specified color.

```html
<div beige background></div>
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


Display and visibility
----------------------

```html
<div show></div>
<div inline></div>
<div hide></div>
<div visible></div>
<div invisible></div>
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

```html
<div transition fast linear delay></div>
```
