Language
========================================================

```r
require(mosaic)
```

```
## Loading required package: mosaic Loading required package: grid Loading
## required package: lattice
## 
## Attaching package: 'mosaic'
## 
## The following objects are masked from 'package:stats':
## 
## D, IQR, binom.test, cor, cov, fivenum, median, prop.test, sd, t.test, var
## 
## The following object is masked from 'package:base':
## 
## max, mean, min, print, prod, range, sample, sum
```

```r
fetchData("COMP121/word-hints.R")
```

```
## Retrieving from http://www.mosaic-web.org/go/datasets/COMP121/word-hints.R
```

```
## [1] TRUE
```

```r
letterProportion <- function(string) {
    letters <- unlist(strsplit(string, ""))
    return(prop.table(table(letters)))
}
```



```r
# letterProportiontest
letterProportion("I have a dream")
```

```
## letters
##               I       a       d       e       h       m       r       v 
## 0.21429 0.07143 0.21429 0.07143 0.14286 0.07143 0.07143 0.07143 0.07143
```

```r
letterProportion("Il faut battre le fer quand il est a chaud")
```

```
## letters
##               I       a       b       c       d       e       f       h 
## 0.21429 0.02381 0.11905 0.02381 0.02381 0.04762 0.09524 0.04762 0.02381 
##       i       l       n       q       r       s       t       u 
## 0.02381 0.07143 0.02381 0.02381 0.04762 0.02381 0.09524 0.07143
```



```r
res <- letterProportion("cet examen est tres diffile")
freqCompare <- function(res, langProp) {
    gap <- res - langProp
    chisq <- sum((gap^2)/langProp)
    return(chisq)
}
```



```r
whichlanguage <- function(string) {
    langProp <- list(E = English, G = German, Fi = Finnish, Fr = French, I = Italian, 
        S = Spanish)
    res <- letterProportion(string)
    comp <- freqCompare(res, langProp)
    FinalRes <- langProp[[min(comp)]]
    return(FinalRes)
}
```




