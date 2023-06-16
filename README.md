
# Respository `<repository-name>`

\<repository-description\>

# License

This template is licensed under the [Creative Commons Attribution 4.0
International license](https://creativecommons.org/licenses/by/4.0/).
Please see the [license file](LICENSE.md).

When using this template, please don’t forget to:

- Adapt this license section to your own needs

- License your own content, and remember that [open is
  better](https://choosealicense.com/).

- Link to the [original
  license](https://creativecommons.org/licenses/by/4.0/) and give
  appropriate credit; please do so by including the following in the
  “License” section of the README.md file in your own project:

  > ## Attributions
  > 
  > This project makes use of the
  > [barebones-rproj-template](https://github.com/DaniMori/barebones-rproj-template)
  > Github template created by [Daniel Morillo](https://github.com/DaniMori)
  > and licensed under the [Creative Commons Attribution 4.0
  > International
  > license](https://creativecommons.org/licenses/by/4.0/).

# Project installation

## Software components

- Install [R version
  4.3.0](https://cran.rstudio.com/bin/windows/base/old/4.3.0/): In
  Windows, using the [binary
  installer](https://cran.rstudio.com/bin/windows/base/old/4.3.0/R-4.3.0-win.exe)
  is recommended.

- [Rstudio
  Desktop](https://www.rstudio.com/products/rstudio/download/#download):
  Although not strictly necessary, it is recommended to install the
  Rstudio IDE; for better reproducibility, use build [2023.06.0+421 for
  Windows
  10/11](https://download1.rstudio.org/electron/windows/RStudio-2023.06.0-421.exe).

- [Git client](https://git-scm.com/download): Install the Git client in
  order to be able to clone locally the project repository. On Windows,
  use [the 64-bit Windows
  installer](https://github.com/git-for-windows/git/releases/download/v2.41.0.windows.1/Git-2.41.0-64-bit.exe).

## Installing the project locally

This project is hosted as a GitHub repository. It can be cloned as a
local git repository following [these
instructions](https://book.cds101.com/using-rstudio-server-to-clone-a-github-repo-as-a-new-project.html#step---2)
(steps 2 through 7). Note that this will create a local copy of
(‘clone’) the GitHub repository as an Rstudio project in the folder
specified. The URL that must be entered into the `Repository URL` text
box is:

```
<repository_url>
```

After cloning the repository, the Rstudio project will open
automatically in the Rstudio IDE. If it doesn’t, or you want to return
later to the project in Rstudio, you can do so by double clicking on the
file `rstudio_project.Rproj` that has been created in the project folder
when cloning the repository.

**NOTE:** It is common practice to avoid using and versioning
`.Rprofile` files. However, this project uses [package
`renv`](https://cran.r-project.org/package=renv) to create a
reproducible environment, which needs the `.Rprofile` file that lives in
the root directory of the project. **Please DO NOT delete or edit this
file**; it will install and activate the `renv` package and make it
ready for restoring the environment.

## Restoring the environment

The reproducible environment created by `renv` must be restored to
install all the packages this project needs to be built properly. In
order to this, use the “renv” -\> “Restore library…” button in Rstudio’s
“Packages” tab to restore the environment. Alternatively, you can type in the
console:

``` r
renv::restore()
```

### NOTE. About the installation of package `renv`:

The `renv` package will be usually installed and activated
automatically. If the "renv" button does not appear in the "Packages" tab, it is
because the `renv` package was not installed. In that case, install first the
`renv` package by running

``` r
install.packages("renv")
```

Then, restore the environment following the previous instructions.

# Repository structure

The file structure of this repository is as follows:

```
<repository-folder>
|
|--- dat  (To store input datasets; must NEVER be checked-in to Github)
|
|--- doc  (To store important documentation of the project)
|
|--- R    (R functions created for this project live here)
|
|--- renv (System library necesssary for `renv` to work. DON'T TOUCH)
|
|--- src  (Source scripts that implement the main processes)
|
|--- www  (Project assets, e.g., images, bibliography files, etc.)
```

Use the folders as indicated to store the different files and generate
the outputs of the processes.
