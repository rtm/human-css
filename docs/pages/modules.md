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

The `background` micro-attribute provides a background of the specified color.

```html
<div background="x-light blue color"></div>
```

Background images are also supported by setting a CSS variable:

```html
<div background="image cover" style="--image: url(photo.jpg)"></div>
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
box sizing (`border` or `content`), and so on.

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


Grid
----

The `grid` micro-attribute sets up a CSS grid container.
Use English number words for equal columns, or `auto-fill`/`auto-fit` for responsive grids.

```html
<div grid="three gap">
  <div>Column 1</div>
  <div>Column 2</div>
  <div>Column 3</div>
</div>

<div grid="auto-fit" style="--grid-min: 15rem">
  <div>Responsive card</div>
  <div>Responsive card</div>
  <div>Responsive card</div>
</div>

<div grid="two">
  <div span="two">Full-width header</div>
  <div>Sidebar</div>
  <div>Content</div>
</div>
```

Alignment uses the same keywords as flex: `top`, `middle`, `bottom`, `left`, `center`, `right`, `stretch`.

Gap
---

The `gap` micro-attribute adds spacing between flex or grid children.

```html
<div flex="wrap" gap="thick"></div>
<div grid="three" gap="thin"></div>
```

Aspect ratio
------------

```html
<img aspect-ratio="video">
<div aspect-ratio="square"></div>
<div aspect-ratio="photo"></div>
```

The predefined ratios are `square` (1:1), `video` (16:9), `photo` (4:3), `portrait` (3:4), and `wide` (21:9).

Logical properties
------------------

Margins, padding, and inset support logical (writing-direction-aware) sides:
`inline`, `block`, `inline-start`, `inline-end`, `block-start`, `block-end`.
These work correctly for both LTR and RTL layouts.

```html
<div padding="thick inline"></div>
<div margin="thin block-start"></div>
<div inset="inline"></div>
```

Logical sizing is available with `inline-size`, `max-inline-size`, and `min-inline-size`.

Text wrap
---------

Control how text wraps within elements:

```html
<h2 text="balance">Balanced heading avoids orphans</h2>
<p text="pretty">Pretty wrapping for body text</p>
```

Opacity
-------

```html
<div opaque></div>
<div semi-opaque></div>
<div transparent></div>
<div opacity 0.8></div>
```

## Shadows

Box shadows and text shadows are supported with identical x and y offsets.

```html
<div box-shadow color="blue"></div>
<span text-shadow="blur" color="red">Shadowed text</span>
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

The `transition` micro-attribute provides a streamlined interface for simple transitions.

```html
<div transition="fast linear delay"></div>
```

## Overflow

```html
<div overflow="scroll x"></div>
<div overflow="hidden"></div>
```

## Cursor

```html
<div cursor="pointer"></div>
```

## Lists

```html
<ul list="upper roman outside"></ul>
<ol list="decimal inside"></ol>
```

## Ruby

The `ruby` micro-attribute controls ruby annotation positioning and alignment,
useful for CJK text and linguistic annotations.

```html
<ruby ruby="over center">
  漢<rp>(</rp><rt>かん</rt><rp>)</rp>
  字<rp>(</rp><rt>じ</rt><rp>)</rp>
</ruby>
```

Position values: `over`, `under`, `left`, `right`, `before`, `after`, `inter-character`.
Alignment values: `start`, `center`, `justify`, `justify-gap`.

## Resize

```html
<textarea resize="vertical"></textarea>
```

## Scroll snap

```html
<div scroll-snap="x mandatory">
  <div scroll-snap-align="center"></div>
</div>
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

#### `whitespace="newlines"`

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
