Flexbox
=====

Human CSS expects most layout to be done using flexbox,
and provides a solid set of micro-attributes to control them.
The micro-attributes available include ones to control direction, wrapping, and alignment.
You'll no longer need to struggle with trying to remember the names or meanings or values of
properties like `align-items`.

Examples of flexbox:

```html
<div flex wrap>
  <div basis one-third>
  <div basis one-third>
  <div basis one-third>
</div>

<div flex vertical justify align-center></div>
```

Flexbox is specified using the `flex` micro-attribute.
The direction is specified by `horizontal` or `vertical`.
Other aspects of the flexbox may be controlled by the micro-attributes `wrap`, `reverse`, and `inline`.

Justification along the main axis is specified by `justify` and `justify-gap` micro-attrihutes.
Alignment of items is controlled by `align-top`, `align-middle`, `aslign-bottom`, `align-left`, `align-center`, `align-right` micro-attributes,
which are always interpreted in the correct way depending on the flexbox direction.

Individual items can be controlled by the `grow` and `no-shrink` micro-attributes,
as well as `self-top`, `self-middle`, `self-bottom`, `self-left`, `self-center`, `self-righ`, `self-stretch`, and `self-baseline` micro-attributes.
