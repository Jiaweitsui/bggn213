Biological Network Analysis
================

``` r
install.packages("igraph")
BiocManager::install("RCy3")
```

``` r
library(RCy3)
library(igraph)
```

    ## 
    ## Attaching package: 'igraph'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     decompose, spectrum

    ## The following object is masked from 'package:base':
    ## 
    ##     union

``` r
library(RColorBrewer)
```

``` r
cytoscapePing()
```

    ## [1] "You are connected to Cytoscape!"

``` r
cytoscapeVersionInfo()
```

    ##       apiVersion cytoscapeVersion 
    ##             "v1"          "3.7.2"

``` r
g <- makeSimpleIgraph()
createNetworkFromIgraph(g,"myGraph")
```

    ## Loading data...
    ## Applying default style...
    ## Applying preferred layout...

    ## networkSUID 
    ##          80

``` r
fig <- exportImage(filename="demo", type="png", height=350)
```

    ## Warning: This file already exists. A Cytoscape popup 
    ##                 will be generated to confirm overwrite.

``` r
knitr::include_graphics("./demo.png")
```

![](./demo.png)<!-- -->

``` r
setVisualStyle("Marquee")
```

    ##                 message 
    ## "Visual Style applied."

``` r
fig <- exportImage(filename="demo_marquee", type="png", height=350)
```

    ## Warning: This file already exists. A Cytoscape popup 
    ##                 will be generated to confirm overwrite.

``` r
knitr::include_graphics("./demo_marquee.png")
```

![](./demo_marquee.png)<!-- -->

``` r
styles <- getVisualStyleNames()
styles
```

    ##  [1] "Ripple"               "size_rank"            "Universe"            
    ##  [4] "Gradient1"            "default black"        "Curved"              
    ##  [7] "Sample3"              "Directed"             "Marquee"             
    ## [10] "Sample2"              "Big Labels"           "Nested Network Style"
    ## [13] "Minimal"              "BioPAX"               "BioPAX_SIF"          
    ## [16] "Sample1"              "Solid"                "default"

``` r
plot(g)
```

![](Class_16_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->
