Units and measures
=====

Many micro-class frameworks suffer from a proliferation of classes such as `width-75`.
This limits the user to only the classes the designer provides.
In contrast, we provide individual micro-attributes for numbers, lengths, and units,
so we can write

```html
<div half width>
<div two rem border>
<div three columns>
```

THe special keyword `size` indicates a ratio to a current size of 100%.
For instance, the following might specify a `flex-basis` of one-third the screen width:

```html
<div flex>
  <div basis one third size>
```

All standard CSS units are provided as micro-attributes.
including lengths such as `px`, `em`, and `rem`.
Common numbers and percentages may also be used as micro-attributes,
in addition to built-in classes such as `1/2`.

There are two CSS variables: `--number` and `--length` which are exposed,
for your use in your own CSS micro-attribute or micro-class rules.

We allow numbers to be specified using English words such as "two",
or Arabic numerals such as "2",
and percents as in "ten percent" or "half width",
and fractions such as "1/2".
and lengths as in "five rem".
