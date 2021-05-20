# Carpentries R Package Universe

Visit <https://carpentries.r-universe.dev/ui#builds> for more information.


## Motivation

The R-universe allows us to host builds of in-development packages that are
built hourly, superseding the need for maintaining our own drat repository.

Using this registry means that we can install packages without needing to build
them with the following code:

```r
# Enable this universe
options(repos = c(
    carpentries = 'https://carpentries.r-universe.dev',
    CRAN = 'https://cloud.r-project.org'))

# Install some packages
install.packages('sandpaper')
```

## Adding new packages

To add a new package, edit [packages.json](packages.json) with the following
format:

```json
[
    {
        "package": <NAME>,
        "url": <GITHUB URL>,
        "branch": <RELEASE BRANCH>
    }
]
```
