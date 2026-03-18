Extending Human CSS
===================

Defining your own attributes
-----------------------------

What if I want to **include** the `padding` functionality into my own attribute definition?
We would caution against this approach,
which goes against the grain of the micro-attribute philosophy.
However, it does have the "advantage" of allowing me to simply say `<div my-padded-red-border>`,
if that is your cup of tea.
You can do this using the `postcss-inherit` plug-in, which provides an `@inherit` pseudo-property, as follows:

```css
[my-padded-red-border] {
  @inherit [border~=red][border~=color], [padding~=thick];
}
```

Note that each micro-attribute value must be a separate `~=` selector.
For example, `[border~=red][border~=color]` is correct;
`[border~="red color"]` would **not** work,
because `~=` matches a single word, not a phrase.

You can also create your own attributes with scoped values.
For instance, you could define a `custom-border` attribute
with values like `padded-red`:

```css
[custom-border~=padded-red] {
  @inherit [border~=red][border~=color], [padding~=thick];
}

[custom-border~=thin-blue] {
  @inherit [border~=thin][border~=blue][border~=color];
}
```

This allows usage like:

```html
<span custom-border="padded-red">Styled text</span>
<div custom-border="thin-blue">Another element</div>
```

If you really want to go this route, you'll have to make sure to add `postcss-inherit` to your package,
and arrange for it to be added to the list of plug-ins used in the preprocessing step.

JavaScript
----------

Since human CSS uses attributes,
to control it from JavaScript you will have to add, modify, or remove attributes,
using `Element#setAttribute` and `Element#removeAttribute`.
You may also use the [`toggleAttribute` API](https://developer.mozilla.org/en-US/docs/Web/API/Element/toggleAttribute).

```js
// Add styling
el.setAttribute('border', 'thick red color');

// Change a value
el.setAttribute('text', 'bold large');

// Remove styling
el.removeAttribute('border');

// Toggle a standalone attribute
el.toggleAttribute('visible');
```
