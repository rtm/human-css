Grid
====

Human CSS provides the `grid` micro-attribute for CSS grid layout,
complementing the existing `flex` micro-attribute.

Basic usage
-----------

Set up a grid container with a number of equal columns:

```html
<div grid="three gap">
  <div>One</div>
  <div>Two</div>
  <div>Three</div>
</div>
```

Responsive grids
----------------

Use `auto-fill` or `auto-fit` for grids that adapt to available space.
Control the minimum cell size with the `--grid-min` CSS variable (defaults to `10rem`).

```html
<div grid="auto-fit" gap="medium" style="--grid-min: 15rem">
  <div>Card</div>
  <div>Card</div>
  <div>Card</div>
  <div>Card</div>
</div>
```

`auto-fill` creates as many tracks as will fit, even if empty.
`auto-fit` collapses empty tracks, allowing items to stretch.

Direction and density
---------------------

By default, grid items flow by row.
Use `columns` to flow by column, or `dense` to pack items tightly:

```html
<div grid="three columns"></div>
<div grid="three dense"></div>
```

Alignment
---------

Grid uses the same alignment keywords as flexbox:

```html
<div grid="three center middle"></div>
<div grid="two justify"></div>
```

`top`, `middle`, `bottom` control vertical alignment.
`left`, `center`, `right` control horizontal alignment.
`stretch` stretches items in both directions.
`justify` and `justify-gap` distribute space between or around columns.

Spanning
--------

Grid children can span multiple columns or rows:

```html
<div grid="four">
  <div span="two">Wide item</div>
  <div>Normal</div>
  <div>Normal</div>
  <div span-row="two">Tall item</div>
</div>
```

Subgrid
-------

Children can inherit the parent grid's tracks:

```html
<div grid="three">
  <div grid="subgrid" span="two">
    <div>Aligned to parent grid</div>
    <div>Aligned to parent grid</div>
  </div>
</div>
```

Gap
---

The `gap` micro-attribute works with both grid and flex containers:

```html
<div grid="three" gap="thick"></div>
<div flex="wrap" gap="thin"></div>
```

Gap sizes: `thin` (0.25em), `medium` (0.5em), `thick` (1em), `x-thick` (2em),
or use any length with a number and unit.
Use `gap="row"` or `gap="column"` to set gaps in only one direction.
