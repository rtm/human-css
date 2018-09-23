Motivation
=====

Our current CSS systems are a steaming pile of crap.
We have thousands of lines of CSS.
Half of these lines of CSS are not even used,
because no one can remember what they do and are afraid to touch them.
Most of the rest is redundant, over-specified, verbose, and duplicative.

Because CSS systems are most often created by "UI designers", rather than engineers,
basic computing principles of orthogonality, factoring, and composition are ignored.

We have become addicted to CSS preprocessors which
merely provide some basic syntactic sugar, and, more perniciously,
promote bad design practices.
Huge sets of rules with complex selectors bog down the browser.

Each new page we write requires dozens or hundreds of new lines of CSS.
Any UI change requires parallel changes to both HTML and CSS.
We use CSS in a way which results in inconsistent UIs.
We rewrite CSS over and over, since often there is no way to re-use what we have done.
There is no reasonable way to understand the CSS, or convince ourselves that it is correct, or test it.

In a futile attempt to escape this maze, we bring in monstrously large, over-engineered
frameworks such as Bootstrap, which add a massive surface area of new classes to learn and deal with.
Just as jQuery attempts to solve JavaScript problems which no longer need solving,
Bootstrap attempts to solve styling problems which no longer need solving,
in particular its cumbersome and confusing grid system.
In addition to added complexity for the programmer, these massive frameworks slow down
build times, page loading times, and rendering times.
They also make undue use of obsolete CSS features such as floats,
while failing to support modern CSS features such as flexbox.

As we proliferate these obese classes, we soon run into namespacing problems.
Names conflict with each other, and we end up needing weird namespace solutions which call for
classes with names like `Book__chapter--title`.
Then we start relying on preprocessors to handle these over-named classes,
which "help" us by allowing us to write weird-looking, brittle rules such as

    .Book {
      &__chapter {
        &--title {
          text-align: center;
          }
        }
     }

Human CSS is designed to put an end to this madness.
