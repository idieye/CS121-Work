Loops
========================================================

```r
# MySum
MySum <- function(v) {
    sofar <- 0
    k <- 1
    sofar <- sofar + v[k]
    k <- k + 1
    if (k == length(v)) 
        break
    return(sofar)
}
```


```r
# mySum using loops
mySum <- function(v) {
    sofar <- 0
    k <- 1
    repeat {
        sofar <- sofar + v[k]
        k <- k + 1
        if (k == (length(v) + 1)) 
            break
    }
    return(sofar)
}
```

```r
# mySum test
mySum(1:10)
```

```
## [1] 55
```


```r
# mySumwhile
mySumwhile <- function(v) {
    sofar <- 0
    k <- 1
    while (k != (length(v) + 1)) {
        sofar <- sofar + v[k]
        k <- k + 1
    }
    return(sofar)
}
```

```r
# mySumwhiletest
mySumwhile(1:10)
```

```
## [1] 55
```

```r
# mySumfor
mySumfor <- function(v) {
    sofar <- 0
    for (k in 1:length(v)) {
        sofar <- sofar + v[k]
    }
    return(sofar)
}
```


```r
# mySumfor test
mySumfor(1:10)
```

```
## [1] 55
```

```r
# myRunningSum
myRunningSum <- function(v) {
    sofar <- 0
    res <- c(0)
    for (k in 1:length(v)) {
        sofar <- sofar + v[k]
        res <- c(res, sofar)
    }
    return(res)
}
```


```r
# myRunningSum test
myRunningSum(1:10)
```

```
##  [1]  0  1  3  6 10 15 21 28 36 45 55
```


```r
myRunningSumrev <- function(v) {
    sofar <- 0
    res <- c(0)
    for (k in 1:length(v)) {
        sofar <- sofar + v[k]
        res <- c(sofar, res)
    }
    return(res)
}
```

```r
# myRunningSumrev test
myRunningSumrev(1:10)
```

```
##  [1] 55 45 36 28 21 15 10  6  3  1  0
```

```r
# myUnique
myUnique <- function(v) {
    already <- c(0)
    for (k in v) {
        if (!(k %in% already)) 
            already <- c(already, k)
    }
    return(already)
}
```


```r
# myUniquetest
myUnique(c("dog", "ant", "bee", "cat", "dog"))
```

```
## [1] "0"   "dog" "ant" "bee" "cat"
```


```

```

```

```

```

```

```

