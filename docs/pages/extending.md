Extending Human CSS
===================

Defining your own attributes
-----

What if I want to **include** the `padding` functionality into my own attribute definition?
We would caution against this approach,
which goes against the grain of the micro-class/micro-attribute  philosophy.
However, it does have the "advantage" of allowing me to simply say `<div class="my-padded-red-border">`,
if that is your cup of tea.
You can do this using the `postcss-inherit` plug-in, which provides an `@inherit` pseudo-property, as follows:

```css
[my-padded-red-border] {
  @inherit [border~=red][border~=color], [padding~=thick];
}
```

If you really want to go this route, you'll have to make sure to add `postcss-inherit` to your package,
and arrange for it to be added to the list of plug-ins used in the preprocessing step,

JavaScript
----------

Since human CSS uses attributes,
to control it from JavaScript you will have to add, modify, or remove attributes,
using `Element#setAttribute` and `Element#removeAttribute`.
You may also use the new [`toggleAttribute` API](https://developer.mozilla.org/en-US/docs/Web/API/Element/toggleAttribute) if available on the browser you want to support.
