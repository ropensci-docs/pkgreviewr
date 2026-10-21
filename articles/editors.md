# pkgreviewr for editors

`pkgreviewr` now also provides templates for editors.

``` r

library(pkgreviewr)

pkgreview_create("nldoc/nlrx",
  review_parent = "~/Documents/workflows/rOpenSci/editorials/",
  template = "editor",
  issue_no = 262
)
```

As with initialising a review, the repo is downloaded into
`review_parent`.

It also creates a `pkgreviewr` project containing editor related
templates:

    .
    ├── editor.md
    ├── index.Rmd
    ├── nlrx-review.Rproj
    └── request.Rmd

### `index.Rmd`

Similar to a review project, `index.Rmd` is a pre-populated notebook
where initial editor checks can be performed

### `editor.md`

This file contains the editor checks response template

### `request.Rmd`

This contains a prepopulated parametarised `.Rmd` for generating request
emails. The parameters it accepts are:

- person’s name
- some friendly banter
- whether JOSS submission is involved

Use:

``` r

render_request()
```

to render the document by first launching a form in the browser to enter
parameter values. Alternatively, you can manually edit the YAML header
with parameter values and knit.
