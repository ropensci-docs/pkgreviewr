# Publish pkgreview on GitHub

**Programmatically using
[`usethis::use_github()`](https://usethis.r-lib.org/reference/use_github.html)**

1.  Git ignore the files you do not want to share.

2.  Run
    [`usethis::git_sitrep()`](https://usethis.r-lib.org/reference/git_sitrep.html)
    to check your settings.

3.  Run
    [`usethis::use_github()`](https://usethis.r-lib.org/reference/use_github.html)
    to create a github repository for your review and add it as a remote
    for your review project. The naming of the github repository is
    handled automatically.

## Enable GitHub Pages

- In your review GitHub repository click on **Settings**

- Scroll down to the **GitHub Pages** section and change **Source**
  location to **main branch**

- \*\*Github Pages is now enabled and your report review [will be
  published](http://annakrystalli.me/rdflib-review/index.nb.md) at the
  link displayed.
