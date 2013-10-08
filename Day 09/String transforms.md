String Transforms
========================================================

```r
# Reverser
Reverser <- function(x) {
    letters <- strsplit(x, "")[[1]]
    R <- letters[rev(1:nchar(x))]
    paste(R, collapse = "")
}
```


```r
# Reverser Test
Reverser("world")
```

```
## [1] "dlrow"
```

```r
Reverser("Ibrahima")
```

```
## [1] "amiharbI"
```

```r
Reverser("Computer")
```

```
## [1] "retupmoC"
```

```r
# Scrambler
Scrambler <- function(x) {
    letters <- strsplit(x, "")[[1]]
    R <- letters[sample(1:nchar(x))]
    paste(R, collapse = "")
}
```

```r
# Scrambler test
Scrambler("love")
```

```
## [1] "leov"
```

```r
Scrambler("Senegal")
```

```
## [1] "elSngea"
```

```r
Scrambler("Minnesota")
```

```
## [1] "aetnosinM"
```


```r
VowelBleeper
```

```
## Error: object 'VowelBleeper' not found
```

```r
VowelBleeper <- function(x) {
    letters <- strsplit(x, "")
    Vowels <- c("e", "o", "a", "e", "i", "y")
    R <- gsub(Vowels, "*", x)
    paste(R, collapse = "")
}
```

```r
# VowelBleeper test
VowelBleeper("computer")
```

```
## Warning: argument 'pattern' has length > 1 and only the first element will
## be used
```

```
## [1] "comput*r"
```


```

```

```

