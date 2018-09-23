Human CSS
======

Human CSS is a system of **micro-attributes** which allow HTML to be styled semantically and readably,
while greatly reducing the need for individual CSS rules.
The great majority of common styling needs can be met by composing these micro-attributes.

Human CSS is based on the micro-class philosophy,
in which elements are styled within HTML by specifying one or more micro-classes.
However, instead of classes, we use attributes,
for greater brevity and readability.
Hence the term "micro-attributes".

With human CSS, many pages may need no specific CSS rules whatsoever.

For instance, consider:

```
<span large dark red bold text>
<div thin light green top border>
<div one third width>
```

Human CSS provides an easy interface to using flexbox,
removing the need for the baroque grid systems some frameworks and libraries try to provide.
For instance, the classic `float: right` is just

    <div flex justify>
      <div>I'm on the left</div>
      <div>I'm on the right</div>
    </div>

### Getting started

Install the library.

    $ npm install @rtm/human-css

Import it into your project's CSS, for example:

    @import "human-css";
    --or--
    @import "~human-css";

For more information, please visit the [`docs/pages`](docs/pages) directory, or https://human-css.readthedocs.io/en/latest/.

### Caveats

Human CSS uses CSS custom properties, also known as CSS variables, in its implementation.
This excludes IE11 from consideration (but Edge is fine).

This library is currently at v0.1.0.
It has been used successfully in several projects, but is by no means completely shaken down.

## Contributing

This repository has no build step or dependencies.
The entire content of the repo, other than documentation, is in `index.css`.
