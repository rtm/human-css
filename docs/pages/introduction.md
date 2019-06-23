Introduction
======

Human CSS is a system of **micro-attributes** which allow HTML to be styled semantically and readably,
while greatly reducing the need for individual CSS rules.
The great majority of common styling needs can be met by composing these micro-attributes.

What are micro-attributes?
--------------------------

Human CSS is based on the micro-class philosophy,
in which elements are styled within HTML by specifying one or more micro-classes.
However, instead of classes, we use attributes,
for greater brevity and readability.
Hence the term "micro-attributes".
Each attribute corresponds to a grouping of style properties,
such as `text` or `border`,
each of which is specified as a set of space-delimited values for the attribute,
which we call "micro-attribute values",
just like `class`.

With human CSS, many pages may need no specific CSS rules whatsoever.

For instance, consider:

```html
<span text="large dark red bold text"></span>
<div border="thin light green top"></div>
<div width="one third"></div>
```

The above uses the human CSS color scheme, based on HSL,
which allows you to easily specify colors using hues (like `red`),
and darknesses (like `light` or `dark`).

Human CSS provides an easy interface to using flexbox,
removing the need for the baroque grid systems some frameworks and libraries try to provide.
For instance, the classic `float: right` is just

```html
<div flex="justify">
  <div>I'm on the left</div>
  <div>I'm on the right</div>
</div>
```

Why micro-attributes?
---------------------

The micro-attributes which comprise human CSS are HTML attributes with very particular meaning.
These attributes are assigned to HTML elements.
In this micro-attribute approach, a single HTML element might have one, two, or even more attributes,
each with one or more values.
This makes the styling in the HTML semantic and readable.
Instead of having a class "book-list-entry" which contains 20 properties over in some distant CSS file,
we add one or two attributes to HTML which clearly express the styling of the entry.
In the best case, which is readily realizable in practice, no element-specific class is necessary at all.

### Caveats

Human CSS uses CSS custom properties in its implementation.
This excludes IE11 from consideration (but Edge is fine).

This library is currently at v0.1.0.
it has been used successfully in several projects, but is by no means completely shaken down.
*Caveat emptor*.
