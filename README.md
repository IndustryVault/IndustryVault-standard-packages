## IndustryVault Recommended Packages

This is an R package that just attaches the IndustryVault-recommended packages (`industryvault-packages`) for use on our platform.  It includes most of Hadley Wickham's packages (colloquially known as the "Hadleyverse").  It's based on a similar package by Tony Boyles.

### Installation

    # install.packages("devtools")
    library("devtools")
    install_github("IndustryVault/industryvault-packages")

### Use

    library("industryvault-packages") 
    # All of the IndustryVault-recommended packages are now available in your environment.
    # There's no need to call library("dplyr"), etc.
    
    detach("package:industryvault-packages")
    # All of the recommended-packages have been removed from your environment again.


### What Happens

When you install an R Package, R checks the DESCRIPTION file for dependencies. If you have unmet dependencies, R tries to install them from CRAN.  Then, whenever you load the package, R makes those dependencies available.  This package just "depends on" all of the packages that the IndustryVault team recommends, despite the fact that it doesn't do anything.  

Here are the packages that the `industryvault-packages` package loads:

 - plyr
 - ggplot2
 - dplyr
 - tidyr
 - readr
 - haven
 - lubridate
 - stringr
 - readxl
 - devtools
 - xml2
 - testthat
 - assertthat or assertr
 - 
 - beepr
 - broom
 - choroplethr
 - DiagrammeR
 - directlabels
 - doParallel
 - dotwhisker
 - foreach
 - ggthemes
 - ggvis
 - Hmisc
 - htmlwidgets
 - httr
 - knitcitations
 - leaflet
 - lintr
 - metricsgraphics
 - noncensus
 - pbapply
 - rafalib
 - rUnemploymentData
 - rmarkdown ???
 - rms
 - RPostgreSQL
 - scales
 - slackr
 - stargazer
 - statebins
 - tufterhandout
 - xtable


install_github( c("adletaw/captioned", "arilamstein/choroplethrZip", "dgrtwo/snippr", "edwindj/chunked", "hadley/haven", "hadley/purrr", "hadley/rvest", "hadley/svglite",
"haozhu233/ezsummary", "hrbrmstr/ggcounty", "jjallaire/revealjs", "karthik/rdrop2", "kevinushey/rex", "nutterb/pixiedust", "ramnathv/slidify", "ramnathv/slidifyLibraries", "ropensci/testdat", "rstudio/bookdown", "trinker/wakefield", "walkerke/tigris") )
