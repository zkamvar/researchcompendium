<!-- README.md is generated from README.Rmd. Please edit that file -->
[![Last-changedate](https://img.shields.io/badge/last%20change-2016--10--20-brightgreen.svg)](https://github.com/benmarwick/researchcompendium/commits/master) [![minimal R version](https://img.shields.io/badge/R%3E%3D-3.3.1-brightgreen.svg)](https://cran.r-project.org/) [![Licence](https://img.shields.io/github/license/mashape/apistatus.svg)](http://choosealicense.com/licenses/mit/) [![Travis-CI Build Status](https://travis-ci.org/benmarwick/researchcompendium.png?branch=master)](https://travis-ci.org/benmarwick/researchcompendium) [![Circle CI](https://circleci.com/gh/benmarwick/researchcompendium.svg?style=shield&circle-token=:circle-token)](https://circleci.com/gh/benmarwick/researchcompendium) [![codecov.io](https://codecov.io/github/benmarwick/researchcompendium/coverage.svg?branch=master)](https://codecov.io/github/benmarwick/researchcompendium?branch=master) [![ORCiD](https://img.shields.io/badge/ORCiD-0000--0001--7879--4531-green.svg)](http://orcid.org/0000-0001-7879-4531)

Research compendium for a report on xxxx
----------------------------------------

### Compendium DOI:

<http://dx.doi.org/xxxxxxx>

The files at the URL above will generate the results as found in the publication. The files hosted at github.com/benmarwick/researchcompendium are the development versions and may have changed since the report was published

### Authors of this repository:

Ben Marwick (<benmarwick@gmail.com>)

### Published in:

Marwick, B, xxxxx

### Overview of contents

This repository is our research compendium for our analysis of xxxx. The compendium contains all data, code, and text associated with the publication. The `Rmd` files in the `analysis/paper/` directory contain details of how all the analyses reported in the paper were conducted, as well as instructions on how to rerun the analysis to reproduce the results. The `data/` directory in the `analysis/` directory contains all the raw data.

### The supplementary files

The `analysis/` directory contains:

-   the manuscript as submitted (in MS Word format) and it's Rmd source file
-   all the data files (in CSV format, in the `data/` directory)
-   supplementary information source files (in R markdown format) and executed versions
-   all the figures that are included in the paper (in the `figures/` directory)

### The R package

This repository is organized as an R package. There are no actual R functions in this package - all the R code is in the Rmd file. I simply used the R package structure to help manage dependencies, to take advantage of continuous integration for automated code testing, and so I didn't have to think too much about how to organise the files.

To download the package source as you see it on GitHub, for offline browsing, use this line at the shell prompt (assuming you have Git installed on your computer):

``` r
git clone https://github.com/benmarwick/researchcompendium.git
```

Once the download is complete, open the `researchcompendium.Rproj` in RStudio to begin working with the package and compendium files.

The package has a number of dependencies on other R packages, and programs outside of R. These are listed at the bottom of this README. Installing these can be time-consuming and complicated, so we've done two things to simpify access to the compendium. First is the packrat directory, which contains the source code for all the packages we depend on. If all works well, these will be installed on your computer when you open `researchcompendium.Rproj` in RStudio. Second is our Docker image that includes all the necessary software, code and data to run our analysis. The Docker image may give a quicker entry point to the project, and is more self-contained, so might save some fiddling with installing things.

### The Docker image

A Docker image is a lightweight GNU/Linux virtual computer that can be run as a piece of software on Windows and OSX (and other Linux systems). To capture the complete computational environment used for this project we have a Dockerfile that specifies how to make the Docker image that we developed this project in. The Docker image includes all of the software dependencies needed to run the code in this project, as well as the R package and other compendium files. To launch the Docker image for this project, first, [install Docker](https://docs.docker.com/installation/) on your computer. At the Docker prompt, enter:

    docker run -dp 8787:8787 benmarwick/researchcompendium

This will start a server instance of RStudio. Then open your web browser at localhost:8787 or or run `docker-machine ip default` in the shell to find the correct IP address, and log in with rstudio/rstudio.

Once logged in, use the Files pane (bottom right) to navigate to `/` (the root directory), then open the folder for this project, and open the `.Rproj` file for this project. Once that's open, you'll see the `analysis/paper` directory in the Files pane where you can find the R markdown document, and knit them to produce the results in the paper. More information about using RStudio in Docker is avaiable at the [Rocker](https://github.com/rocker-org) [wiki](https://github.com/rocker-org/rocker/wiki/Using-the-RStudio-image) pages.

We developed and tested the package on this Docker container, so this is the only platform that We're confident it works on, and so recommend to anyone wanting to use this package to generate the vignette, etc.

### Licenses

Manuscript: [CC-BY-4.0](http://creativecommons.org/licenses/by/4.0/)

Code: [MIT](http://opensource.org/licenses/MIT) year: 2016, copyright holder: Ben Marwick

Data: [CC-0](http://creativecommons.org/publicdomain/zero/1.0/) attribution requested in reuse

### Dependencies

I used [RStudio](http://www.rstudio.com/products/rstudio/) on Ubuntu 16.04 and Windows 7. See the colophon section of the docx file in `analysis/paper` for a full list of the packages that this project depends on.

### Contact

Ben Marwick, Associate Professor, Department of Anthropology Denny Hall 117, Box 353100, University of Washington Seattle, WA 98195-3100 USA

1.  (+1) 206.552.9450 e. <bmarwick@uw.edu>
2.  (+1) 206.543.3285 w. <http://faculty.washington.edu/bmarwick/>
