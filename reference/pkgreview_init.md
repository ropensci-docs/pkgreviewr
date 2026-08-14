# Initialise pkgreview

Initialise pkgreview

## Usage

``` r
pkgreview_init(
  pkg_repo,
  review_dir = ".",
  pkg_dir = NULL,
  template = c("review", "editor"),
  issue_no = NULL
)
```

## Arguments

- pkg_repo:

  character string of the repo owner and name in the form of
  `"owner/repo"`.

- review_dir:

  path to the review directory. Defaults to the working directory. \#
  nolint: line_length_linter

- pkg_dir:

  path to package source directory, cloned from github. Defaults to the
  package source code directory in the review parent.

- template:

  character string, one of `review` or `editor`.

- issue_no:

  integer. Issue number of the pkg review in the rOpenSci
  [`software-review`
  repository](https://github.com/ropensci/software-review/issues). \#
  nolint: line_length_linter If `NULL` (default), the issue number is
  extracted from the rOpenSci **Under Review** badge on the pkg
  repository README. Supplying an integer to `issue_no` overrides this
  behaviour and can be useful if a badge has not been added to the
  README yet.

## Value

Initialisation creates pre-populated `index.Rmd`, `pkgreview.md` and
`README.md` documents. \# nolint: line_length_linter To initialise
correctly, the function requires that the source code for the package
has been cloned. This might need to be done manually if it failed during
review creation. If setup is correct.

## Examples

``` r
if (FALSE) { # \dontrun{
# run from within an uninitialised pkgreviewr project
pkgreview_init(pkg_repo = "ropensci/rdflib")
} # }
```
