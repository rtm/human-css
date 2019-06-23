Flexbox
=====

Human CSS expects most layout to be done using flexbox,
and provides the `flex` micro-attribute to control them.
The micro-attribute values available include ones to control direction, wrapping, and alignment.
You'll no longer need to struggle with trying to remember the names or meanings or values of
properties like `align-items`.

Examples of flexbox:

```html
<div flex="wrap">
  <div self="one-third">
  <div self="one-third">
  <div basis one-third>
</div>

<div flex="y justify center"></div>
```

Flexbox is specified using the `flex` micro-attribute.
The direction is specified by values of `x` or `y`.
Other aspects of the flexbox may be controlled by the micro-attribute values `wrap`, `reverse`, and `inline`.

Justification along the main axis is specified by `justify` and `justify-gap` micro-attrihute values.
Alignment of items is controlled by `top`, `middle`, `bottom`, `left`, `center`, and `right` micro-attribute values,
which are always interpreted in the correct way depending on the flexbox direction
.
Individual items can be controlled by the `self` micro-attribute,
with vlaues such as `no-shrink`,
as well as `top`, `middle`, `bottom`, `left`, `center`, `right`, `stretch`, and `baseline` micro-attribute valuess.
