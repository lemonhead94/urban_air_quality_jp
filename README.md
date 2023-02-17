# Reproducibility Study: Have vehicle registration restrictions improved urban air quality in Japan

**Authors:** Michelle Koch and Jorit Studer

**Module:** Natural Experiments Using R (May 13th, 2023)

**Supervisor:** Lukas Schmid

## Project Structure

```
|--analysis.pdf       # Report rendered by Bookdown
|--data\              # Data for the analysis
|--latex\             # Custom Title Page in Latex
|--references\        # References
  |--references.bib     # BibTeX references
  |--apa.csl            # APA 7th Edition Citation Style Language

|--analysis.html      # Report rendered by Bookdown with animated worcloud2
```

## Installation

The following packages are required to knitr this report using bookdown.

```r
packages <- c("dplyr","readxl","tidyverse", "bookdown", "car", "ivreg", "sandwich", "rddensity", "rdrobust", "fixest", "Synth")
package.check <- lapply(packages, FUN = function(x) {
    if (!require(x, character.only = TRUE)) {
        install.packages(x, dependencies = TRUE)
        library(x, character.only = TRUE)
    }
})
```