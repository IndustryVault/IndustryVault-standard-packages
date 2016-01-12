# IndustryVault's Recommended R Packages

This is an R package that just attaches the IndustryVault-recommended packages (`industryvault-packages`) for use on our platform.  It includes most of Hadley Wickham's packages (colloquially known as the "Hadleyverse").  It's based on a similar package by Tony Boyles.


## Installation

    install.packages("devtools")
    library("devtools")
    install_github("IndustryVault/Rpackages")


## Use

    library("Rpackages") 
    # All of the IndustryVault-recommended R packages are now available in your environment.
    # There's no need to call library("dplyr"), etc.


## What Happens

When you install an R Package, R checks the DESCRIPTION file for dependencies. If you have unmet dependencies, R tries to install them from CRAN.  Then, whenever you load the package, R makes those dependencies available.  This package just "depends on" all of the packages that the IndustryVault team recommends, despite the fact that it doesn't do anything.  


## Recommended Packages

The three most important R packages used on the IndustryVault platform are `dplyr`, `ggplot2`, and `rmarkdown`.  For R users new to our platform, these are the first packages with which you should become familiar.

That said, here is the complete list of packages in the `Rpackages` package installs and loads.  Note that packages associated with the "Hadleyverse" are denoted with (H), and packages hosted on GitHub.com (not CRAN) are denoted with (G).  The packages installed include:

### Ingest
  - readr:  read flat files (csv, tsv, fwf) into R (H)
  - readxl:  read excel files (.xls and .xlsx) into R (H)
  - haven:  read SPSS, Stata and SAS files from R (H)
  - rvest:  simple web scraping for R (H)
  - httr:  download web data ala the `curl` command, customised to modern web APIs (H)
  - wakefield:  generate random data sets

### Manipulation
  - dplyr:  data manipulation ala plyr, specialised for data frames  (H)
  - multidplyr:  a backend for dplyr that partitions a data frame across multiple cores (G, H)
  - testdat:  a package to run unit tests on tabular data (G)
  - assertr:  a suite of functions designed to verify assumptions about data
  - tidyr:  easily tidy data with spread and gather functions (H)
  - lubridate:  make working with dates in R just that little bit easier (H)
  - stringr:  wrapper for R string functions to make them more consistent, simpler and easier to use (H)
  - broom:  convert statistical analysis objects from R into tidy format
  - RPostgreSQL:  R interface to the PostgreSQL database, inc. AWS Redshift (rstats-db/RPostgres in development)
  - chunked:  chunkwise text-file processing for 'dplyr'
  - ezsummary:  pre-programming the common dataset summary task 

### Visualization
  - ggplot2:  powerful plotting library in R based on the Grammar of Graphics (H)
  - ggalt:  extra coordinate systems, geoms, and statistical transformations for ggplot2 (H)
  - ggsubplot: embed subplots in ggplot2 graphics in R (H)
  - dotwhisker:  generate dot-and-whisker plots of regression results
  - ggmap:  plotting maps in R with ggplot2 (H)
  - ggcounty:  generate ggplot2 geom_map county maps
  - choroplethr:  simplifies the creation of choropleths (thematic maps) in R
  - choroplethrZip:  simplifies data and visualization of US ZIP Codes (G)
  - statebins:  "map-like" alternative to choropleths of US States
  - gtable: tools to make it easier to work with “tables” of graphics objects (grobs) (H)
  - ggthemes:  ggplot themes and scales
  - scales:  more graphical scales, for use on chart axes, etc (H)
  - directlabels:  direct labels for multicolor plots in lattice or ggplot2
  - ggrepel:  repel overlapping text labels away from each other (G)
  - ggvis:  web-based data visualizaton ala ggplot2
  - svglite:  lightweight svg graphics (web optimal) for R (H)
  - bigvis:  exploratory data analysis for large datasets (10-100 million observations) (G, H)
  - metricsgraphics:  htmlwidget interface to the MetricsGraphics.js D3 chart library
  - leaflet:  JavaScript library for mobile-friendly interactive maps based on htmlwidgets (G)
  - rafalib:  interesting collection of functions for data exploration

### Reporting
  - rmarkdown:  dynamic documents for R (H)
  - knitr:  a general-purpose tool for dynamic report generation in R  (H)
  - knitcitations:  generate citations for knitr markdown and html files
  - captioner:  generate figure/table numbers and captions for RMarkdown docs
  - DiagrammeR:  create graph diagrams and flowcharts using R
  - pixiedust: broom-compatiable table formatting
  - stargazer:  well-formatted regression and summary statistics tables
  - xtable:  export Tables to LaTeX or HTML (alternative to stargazer)
  - tufterhandout:  output formats for Tufte-style handouts in pdf and html for Rmarkdown
  - revealjs:  RMarkdown custom format for reveal.js HTML presentations (G)
  - bookdown:  package and set of conventions for making books with Rmarkdown and RStudio (G)

### Programming
  - devtools:  tools to make an R developer's life easier (H)
  - magrittr:  R package to bring forward-piping features ala F#’s |> operator.
  - testthat:  an R package to make testing fun (H)
  - rex:  friendly regular expressions for R (G)
  - htmlwidgets:  HTML Widgets for R, easily creating R bindings to JavaScript libraries
  - assertthat:  user-friendly assertions for R (H)
  - lazyeval:  a strategy for doing non-standard evaluation (NSE) in R (H)
  - profvis:  visualise line profiling results in R (H)
  - lintr:  static code analyis (i.e., `lint`) for R
  - foreach:  looping construct (i.e., `for` loop) that support parallel execution
  - doParallel:  `foreach` parallel adaptor for the 'parallel' package
  - snippr:  manage, share, and install RStudio code snippets (G)
  - slackr:  send messages to Slack channels/users from R
  - rpushbullet:  send messages to your computer, phone, or tablet using Pushbullet service

## TODO
  - decide on implementing this package using drat, packrat, or some other method. (Not checkpoint due to GitHub repos)
  - add vignette for use of three most important packages `dplyr`, `ggplot2`, and `rmarkdown`
  - add vignette for examples of all packages
  - best practices ?
  - consider adding separate packages for datasets; see, for example:
    - noncensus:  self-contained U.S. Census Region and Demographic Data
    - rUnemploymentData:  data and functions for dealing with US Unemployment Data in R
    - tigris:  download and use Census TIGER/Line shapefiles in R
  - safety testing
    - find out if it's safe to add `rdrop2`:  Dropbox Interface from R
    - should we allow user-installed packages on AWS?
    - can we prevent data export on AWS from R and RStudio?
  - GitHub repo installation code is below:
        
    install_github( c("arilamstein/choroplethrZip", "dgrtwo/snippr", "eddelbuettel/rpushbullet", "edwindj/chunked", "hadley/bigvis", "hadley/svglite", "haozhu233/ezsummary", "hrbrmstr/ggcounty", "jjallaire/revealjs", "karthik/rdrop2", "kevinushey/rex", "nutterb/pixiedust", "ramnathv/slidify", "ramnathv/slidifyLibraries", "ropensci/testdat", "rstudio/bookdown", "trinker/wakefield", "walkerke/tigris") )

