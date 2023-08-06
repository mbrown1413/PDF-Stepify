
# PDF-Stepify

Highlights each numbered step in a PDF by duplicating a page for each step and
highlighting the current step.

For a working copy, and a better explanation, see the <a href="https://mbrown1413.github.io/pdf-stepify/">github pages site</a>.

For details on the code, keep reading...

## What counts as a step?

The `textMatches` function defines what text items are counted as steps. The string of a text item matches if:

* it is exactly a number followed by "." (this matches typical numbered lists in office programs which have separate text items for the numbers and the text after them), or
* it *starts* with a number followed by ")" (other text may follow, which is useful for manually writing out "1) ... 2) ...")

A step must be on a new line. If two steps are on the same line, only the first
will be recognized.

This works in most cases, but it may not match your criteria. The boundaries
between text items can be different depending on the software used to save the
PDF. In the future there may be options for the user to modify the algorithm
for determining steps. For now you can modify the source code. Pretty easy,
it's just a few static files!

## License

MIT license. For details see LICENSE.txt
