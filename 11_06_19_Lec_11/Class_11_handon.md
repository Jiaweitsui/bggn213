Class 11: Structural Bioinformatics
================

## 

``` r
data <- read.csv("Data Export Summary.csv")
data
```

    ##   Experimental.Method Proteins Nucleic.Acids Protein.NA.Complex Other
    ## 1               X-Ray   131463          2060               6768     8
    ## 2                 NMR    11241          1304                262     8
    ## 3 Electron Microscopy     2925            32               1004     0
    ## 4               Other      280             4                  6    13
    ## 5        Multi Method      144             5                  2     1
    ##    Total
    ## 1 140299
    ## 2  12815
    ## 3   3961
    ## 4    303
    ## 5    152

\#89% of structures solved by X-Ray, \#3% of structures solved by
Electron Microscopy.

``` r
(data$Total[1])/sum(data$Total)
```

    ## [1] 0.8906177

``` r
(data$Total[3])/sum(data$Total)
```

    ## [1] 0.02514442

``` r
ans <- data$Total
```
