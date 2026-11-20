# pkgreviewr

# pkgreviewr

The goal of pkgreviewr is to facilitate **rOpenSci** reviewers in their
package reviews.

It creates a review project containing populated templates of all the
files you’ll need to complete your review. It also clones the source
code of the package under review to a convenient location, allowing easy
checking and testing.

See [Getting
started](https://docs.ropensci.org/pkgreviewr/articles/get_started.md)
vignette for more details

## Installation

You can install `pkgreviewr` from R-universe with:

``` r

install.packages("pkgreviewr", repos = c("https://ropensci.r-universe.dev", "https://cloud.r-project.org"))
```

Or from GitHub with:

``` r

# install.packages("pak")
pak::pak("ropensci-org/pkgreviewr")
```

### Git and GitHub setup

`pkgreviewr` functions clone the source code of the package under review
so require **Git** to be installed. It also interacts with GitHub to get
data from the software-review repository and to prepopulate review
project files.

Therefore, to ensure it will work well, please run
[`usethis::git_sitrep()`](https://usethis.r-lib.org/reference/git_sitrep.html).

### R Notebooks

The package currently also makes use of
[**`R Notebooks`**](https://rmarkdown.rstudio.com/r_notebooks.html) (an
RMarkdown format) and requires installation of **Rstudio version 1.0**
or higher, but we are [considering offering an option to remove the
requirement for
RStudio](https://github.com/ropenscilabs/pkgreviewr/issues/64).

------------------------------------------------------------------------

## Review workflow

  

#### 1. Create and initialise review project

``` r

library(pkgreviewr)
review_parent <- withr::local_tempdir() # not a temp dir in real life :-)
pkgreview_create(
  pkg_repo = "ropensci/rdflib",
  review_parent = review_parent
)
#> ✔ Setting `fork = FALSE`.
#> ✔ Creating '/tmp/RtmpxDZe8i/filebd7173b99561/rdflib/'.
#> ✔ Cloning repo from "git@github.com:ropensci/rdflib.git" into
#>   '/tmp/RtmpxDZe8i/filebd7173b99561/rdflib'.
#> ✔ Setting active project to "/tmp/RtmpxDZe8i/filebd7173b99561/rdflib".
#> ℹ Default branch is "master".
#> ✔ Setting active project to "<no active project>".
#> ✔ review project "rdflib-review" initialised
```

The review project directory will contain all the files you’ll need to
complete the review and will be initialised with git.

``` r

fs::dir_ls(review_parent)
#> /tmp/RtmpxDZe8i/filebd7173b99561/rdflib
#> /tmp/RtmpxDZe8i/filebd7173b99561/rdflib-review
fs::dir_tree(fs::path(review_parent, "rdflib-review"))
#> /tmp/RtmpxDZe8i/filebd7173b99561/rdflib-review
#> ├── R
#> ├── README.md
#> ├── index.Rmd
#> └── review.md
```

#### 2. Perform review

Open `index.Rmd` and work through the review in the notebook. You can
make notes either in `index.Rmd` or directly in the `pkgreview.md`
response template.

  

#### 3. Submit review

Submit your review in the package
[`ropensci/software-review`](https://github.com/ropensci/software-review/issues)
issue by copying and pasting the completed `pkgreview.md` template.

  

#### 4. Publish review\*

OPTIONAL: Publish your review on GitHub. See
[vignette](https://docs.ropensci.org/pkgreviewr/articles/publish-review-on-github.md)
for further instructions

  

------------------------------------------------------------------------

## `pkgreviewr` for editors

`pkgreviewr` can now also be used to set up projects for editor checks.
See [`pkgreviewr` for
editors](https://docs.ropensci.org/pkgreviewr/articles/editors.md)
vignette.

------------------------------------------------------------------------

Please note that ‘pkgreviewr’ is released with a [Contributor Code of
Conduct](https://docs.ropensci.org/pkgreviewr/CODE_OF_CONDUCT.md). By
contributing to this project, you agree to abide by its terms.
