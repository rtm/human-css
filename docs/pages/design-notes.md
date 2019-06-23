Design notes
============

Performance
-----------

CSS is rarely the major bottleneck in application performance.
Of course there may be exceptions involving huge systems,
or extremely poorly written CSS rules,
or use of CSS properties with known performance implications.

Human CSS classes offer improved performance because the dozens or hundreds of CSS files often seen in
poorly-engineered applications are much smaller (or not needed at all).
This reduces both download and processing time.

Unused features
---------------

### Floats

We do not use or support floats, and neither should you.

### `!important`

We neither need nor use `!important`, and we recommend you do not either.

Inline styles
------------

Some element-specific styling can obviously not be handled with micro-attributes,
`background-image` for example.
If a page has only one or two such cases, we suggest inlining the rule with the `style` attribute.
We are not religious zealots, and this can be a better approach than creating a separate CSS file
and defining an additional class merely in order to target the element.

Unsupported features
--------------------

The following CSS features require more complex properties which are not well-suited to the micro-attribute approach,
and therefore are not (currently) supported:

1. Animations or more complex transitions
2. Box shadows and text shadows
3. Properties involving URLs, such as `background-image`
4. Pseudo-classes
5. Pseudo-elements

Some of thse might be able to be supported when browser support for the `attr()` function is available.
