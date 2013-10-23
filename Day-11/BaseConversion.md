Base conversion deliverable
========================================================

```r
# Task 1 toBase function
toBase <- function(Z, b) {
    sofar <- c()
    while (Z != 0) {
        r <- Z%%b
        Z <- (Z - r)/b
        sofar <- c(r, sofar)
    }
    return(as.character(sofar))
}
```

```r
# test toBase function
toBase(10, 2)
```

```
## [1] "1" "0" "1" "0"
```

```r
toBase(1000, 16)
```

```
## [1] "3"  "14" "8"
```

```r
toBase(100, 3)
```

```
## [1] "1" "0" "2" "0" "1"
```




```r
baseToNumeric(2, Z)
```

```
## Error: could not find function "baseToNumeric"
```


```r
# basetoNumeric without loops
basetoNumeric <- function(Nvec, b) {
    howMany <- length(Nvec)
    herdsize <- b^((howMany - 1):0)
    return(sum(as.numeric(Nvec) * herdsize))
}
```


```r
# basetoNumeric test
basetoNumeric(c("7", "6", "5", "4"), 8)
```

```
## [1] 4012
```

```r
basetoNumeric(c("7", "6", "5", "4"), 9)
```

```
## [1] 5638
```

```r
basetoNumeric(c("7", "6", "5", "4"), 12)
```

```
## [1] 13024
```


```r
# basetoNumeric with loops
BasetoNumeric <- function(Nvec, b) {
    sheepCount <- 0
    boxSize <- 1
    for (k in length(Nvec):1) {
        sheepCount <- sheepCount + boxSize * Nvec[k]
        boxSize <- boxSize * b
    }
    return(as.numeric(sheepCount))
}
```

```r
# BasetoNumeric test
BasetoNumeric(c("7", "6", "5", "4"), 8)
```

```
## Error: non-numeric argument to binary operator
```

```r
# look at syllabus
```


```


