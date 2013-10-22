Day 13
========================================================

```r
# Add up V
addEm <- function(v) {
    sum <- 0
    for (k in 1:length(v)) sum <- sum + v[k]
    return(sum)
}
```

```r
# addEm test
addEm(1:5)
```

```
## [1] 15
```

```r
addEm(1:10)
```

```
## [1] 55
```



```r
# newaddEm
newaddEm <- function(v) {
    if (length(v) == 0) {
        return(0)
    }
    return(v[1] + newaddEm(v[-1]))
}
```

```r
# newaddEm test
newaddEm(1:5)
```

```
## [1] 15
```

```r
newaddEm(1:10)
```

```
## [1] 55
```


```

```

