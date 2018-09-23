Other topics
=====

Combining micro-attributes
-----

Human CSS uses a relatively limited number of general-purpose micro-attributes.
So `green` means green for text, or borders, or backgrounds.
But what if I want to specify both text color **and** border color on an element?
How do I know which color is which?
Other micro-class frameworks solve this by a proliferation of classes such as `green-border`, and `green-text`.
We take a different approach, which is to place the attributes on individual, nested HTML elements:

```html
<div one em margin>
  <div thick dark blue border>
    <div x-light pink background>
      <div five percent padding>
        <div large bold white text>
          Bob
        </div>
      </div>
    </div>
  </div>
</div>
```

Although this does result in more deeply nested HTML,
it also has major advantages.
Each element has a single, well-defined purpose,
and as mentioned above we need only generic attributes such as `blue` which work everywhere.

Defining your own attributes
-----

What if I want to **include** the `padding` functionality into my own attribute definition?
We would caution against this approach,
which goes against the grain of the micro-class/micro-attribute  philosophy.
However, it does have the "advantage" of allowing me to simply say `<div class="my-class">`.
You can do this using the `postcss-inherit` plug-in, which provides an `@inherit` pseudo-property, as follows:

```css
[my-padded-red] {
  @inherit [red], [thick][padding];
}
```

If you really want to go this route, you'll have to make sure to add `postcss-inherit` to your package,
and arrange for it to be added to the list of plug-ins used in the preprocessing step,
