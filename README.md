
## gtrendsR [![Travis-CI Build Status](https://api.travis-ci.org/PMassicotte/gtrendsR.svg?branch=master)](https://travis-ci.org/PMassicotte/gtrendsR) [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/PMassicotte/gtrendsR?branch=master&svg=true)](https://ci.appveyor.com/project/PMassicotte/gtrendsR) [![Package-License](https://img.shields.io/badge/license-GPL%20%28%3E=%202%29-brightgreen.svg?style=flat)](http://www.gnu.org/licenses/gpl-2.0.html) [![CRAN](http://www.r-pkg.org/badges/version/gtrendsR)](https://cran.r-project.org/package=gtrendsR) [![Downloads](http://cranlogs.r-pkg.org/badges/gtrendsR?color=brightgreen)](http://www.r-pkg.org/pkg/gtrendsR)

`gtrendsR` provides an interface for retrieving and displaying Google Trends information. 

Trends (number of hits) over time as well as geographic representation of the results can be displayed.

## Changes in Google Trends API

Due to recent changes to Google Trends API, the CRAN version of the package is no longer working. If you wan to continue to query Google Trends, you have to install the development version of the package. This will be soon deployed on CRAN.

### Example

In this simple example, trends for keywords `nhl`, `nba` are retrieved for Canada and USA and then plotted from R.

``` {.r}
library(gtrendsR)

res <- gtrends(c("nhl", "nba"), geo = c("CA", "US"))
plot(res)
```

### Installation

Since release 1.3.0, the package is on [CRAN](https://cran.r-project.org) and
can be installed via

``` {.r}
install.packages("gtrendsR")
```

Release-candidate packages are available in the [ghrr drat repository](https://ghrr.github.io/drat/)
and can installed via

```r
install.packages("drat")       # easier repo access + creation
drat:::add("ghrr")             # make it known
install.packages("gtrendsR")   # install it
```

Development version (which may be less stable) can be installed directly from this repository via

``` {.r}
if (!require("devtools")) install.packages("devtools")
devtools::install_github("PMassicotte/gtrendsR")
```

### Authors

Philippe Massicotte and Dirk Eddelbuettel

### License

GPL (>= 2)
