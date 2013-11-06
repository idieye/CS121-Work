Day 14
========================================================

```r
# Reverse a vector recursively
revrec <- function(v) {
    if (length(v) == 1) 
        return(v) else {
        c(revrec(v[-1]), v[1])
    }
}
```


```r
# test case
revrec(c(1, 2, 3, 5))
```

```
## [1] 5 3 2 1
```

```r
revrec(c(0, 19, 21, 90, 101, 125))
```

```
## [1] 125 101  90  21  19   0
```


