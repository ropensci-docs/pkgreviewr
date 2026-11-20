# Create software review/editor response template

Clone an up to date copy of the specified ropensci software
review/editor response template.

## Usage

``` r
use_onboarding_tmpl(template = c("review", "editor"), destdir)
```

## Arguments

- template:

  character string, one of `review` or `editor`.

- destdir:

  where to save the template

## Value

writes a `{template}.md` checklist template file in `destdir`.

## Examples

``` r
if (FALSE) { # \dontrun{
use_onboarding_tmpl(template = "editor")
} # }
```
