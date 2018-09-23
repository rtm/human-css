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

With human CSS, many pages may need no specific CSS rules whatsoever.

For instance, consider:

```html
<span large dark red bold text></span>
<div thin light green top border></div>
<div one third width></div>
```

Human CSS provides an easy interface to using flexbox,
removing the need for the baroque grid systems some frameworks and libraries try to provide.
For instance, the classic `float: right` is just

```html
<div flex justify>
  <div>I'm on the left</div>
  <div>I'm on the right</div>
</div>
```

Why micro-attributes?
---------------------

The micro-attributes which comprise human CSS are HTML attributes with very particular meaning.
These attributes are assigned to HTML elements.
In the micro-attribute approach, a single HTML element might have two, five, or more attributes.
The styling in the HTML becomes semantic and readable.
Instead of having a class "book-list-entry" which contains 20 properties over in some distant CSS file,
we add three or four attributes to HTML which clearly express the styling of the entry.
In the best case, which is readily realizable in practice, no element-specific class is necessary at all.

### Caveats

Human CSS uses CSS custom properties, also known as CSS variables, in its implementation.
This excludes IE11 from consideration (but Edge is fine).

This library is currently at v0.1.0.
it has been used successfully in several projects, but is by no means completely shaken down.
