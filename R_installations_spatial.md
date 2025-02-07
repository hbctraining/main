# Spatial transcriptomics Nanocourse

## Installation Requirements

### Applications
Download the most recent versions of R and RStudio for your laptop:

 - [R](http://lib.stat.cmu.edu/R/CRAN/) **(version 4.4.0 or above)**
 - [RStudio](https://www.rstudio.com/products/rstudio/download/#download)

> **Note 1**: If you have a Mac with an M1 chip, download and install this tool before intalling your packages: https://mac.r-project.org/tools/gfortran-12.2-universal.pkg

> **Note 2**: At any point (especially if you’ve used R/Bioconductor in the past), in the console **R may ask you if you want to update any old packages by asking Update all/some/none? [a/s/n]:**. If you see this, **type "a" at the prompt and hit Enter** to update any old packages. _Updating packages can sometimes take quite a bit of time to run, so please account for that before you start with these installations._  


### Day 1 Module

**(1)** Install BiocManager:

```r
if (!requireNamespace("BiocManager", quietly = TRUE)) 
    install.packages("BiocManager")

```

**(2)** Install SpatialFeatureExperiment v1.9.7+ :

```r
ncpu = 2

BiocManager::install("pachterlab/SpatialFeatureExperiment",
                     ref = "devel",
                     Ncpus = ncpu)
```

**(3)** Install the remaining packages:

```r
pkgs = c("SFEData",
         "scuttle",
         "scater",
         "scran",
         "bluster",
         "BiocParallel",
         "Voyager",
         "fastverse",
         "ggplot2",
         "pals")

BiocManager::install(pkgs,
                     Ncpus = ncpu)
```



### Day 2 Module

**(1)** Install the packages listed below from **CRAN** using the `install.packages()` function. 

1. `tidyverse`
2. `Seurat`
3. `patchwork`
4. `qs`
5. `quadprog`
6. `remotes`
7. `devtools`


**Please install them one-by-one as follows:**

```r
install.packages("tidyverse")
install.packages("Seurat")
install.packages("patchwork")
& so on ...
```

**(2)** Install the packages listed below from **Bioconductor** using the command below.

```r
BiocManager::install("glmGamPoi")
```

**(3)** Install the packages listed below from GitHub using the given `remotes:install_github` or `devtools::install_github` command as provided below.

1. SeuratWrappers: `remotes::install_github('satijalab/seurat-wrappers')`
2. BANKSY: `remotes::install_github("prabhakarlab/Banksy@devel")`
3. spacexr: `devtools::install_github("dmcable/spacexr", build_vignettes = FALSE)`


### Loading libraries
Finally, please check that all the packages were installed successfully by **loading them one at a time** using the `library()` function.  

```r
## Day 1 module requirements
library(SpatialFeatureExperiment)
library(scuttle)
library(Voyager)
library(fastverse)
library(ggplot2)
library(SFEData)
library(scater)
library(scran)
library(bluster)
library(BiocParallel)
library(pals)


## Day 2 module requirements
library(qs)
library(Seurat)
library(tidyverse)
library(patchwork)
library(quadprog)
library(remotes)
library(devtools)
library(glmGamPoi)
library(SeuratWrappers)
library(Banksy)
library(spacexr)

```

### Report successful installation 
Once all packages have been loaded, run sessionInfo().  

```r
sessionInfo()
```



---
