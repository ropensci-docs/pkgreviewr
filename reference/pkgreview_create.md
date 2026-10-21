# Create a review project.

Create and initialise an rOpenSci package review project

## Usage

``` r
pkgreview_create(
  pkg_repo,
  review_parent = ".",
  template = c("review", "editor"),
  issue_no = NULL
)
```

## Arguments

- pkg_repo:

  character string of the repo owner and name in the form of
  `"owner/repo"`.

- review_parent:

  directory in which to setup review project and source package source
  code.

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

setup review project with templates

## Examples

``` r
if (FALSE) { # \dontrun{
# for a review project
pkgreview_create(
  pkg_repo = "ropensci/rdflib",
  review_parent = "~/Documents/reviews/"
)
# for editors checks
pkgreview_create(
  pkg_repo = "ropensci/rdflib",
  review_parent = "~/Documents/editorials/",
  template = "editor"
)
} # }
```
