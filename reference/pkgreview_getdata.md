# pkgreview_getdata

get package metadata from package source code.

## Usage

``` r
pkgreview_getdata(
  pkg_repo,
  pkg_dir = NULL,
  template = c("review", "editor"),
  issue_no = NULL
)
```

## Arguments

- pkg_repo:

  character string of the repo owner and name in the form of
  `"owner/repo"`.

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

a list of package metadata

## Examples
