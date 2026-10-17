# Learn Dream

A book that teaches [Dream](https://github.com/dream-mindv2/dreams) from a first program to a small web server, one
idea a chapter: values and functions, patterns, collections, laziness,
effects and errors, types, modules, processes, testing, and a service built
from all of them.

Every example in it is a whole program. The site is built by `mind docs`,
which compiles and runs each one and puts what it printed under it, so the
output on the page is the output the program printed. Names in code are
links into the standard library's reference, which the site carries with it.

## Reading it

With Dream installed, from this repository:

```sh
mind docs serve --watch   # build it, serve it at http://127.0.0.1:8000/, rebuild on change
mind docs                 # or just build it, into target/docs/
```

The site works offline. `target/docs/index.html` opens straight from the disk
too. In the [Dream workspace](https://github.com/Custards1/dream), where this repository is
checked out at `learn/`, `just learn` and `just learn-serve` do the same.

## Writing it

The chapters are the Markdown files in [`docs/`](docs), read in the order
their names sort. A `dream` block is a program that must compile and run
cleanly, `dream fails` one that must not, and `dream no-run` a fragment that
is shown but not compiled. `[docs] strict-examples` is on, so a chapter whose
example stops doing what its fence says fails the build. The workspace's
`just test-mind` runs that check (`mind/tool/tests/learn.sh`), which keeps the
book honest as the language changes under it.

Write for someone who has programmed before but has never seen Dream: one
new idea at a time, each shown working before it is explained, and each
example short enough to read in a glance. Prefer what the standard library
already does to writing it again. The book teaches the library too.
