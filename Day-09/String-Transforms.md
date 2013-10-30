String Transforms
========================================================

```r
# Reverser function
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
## [1] "ovel"
```

```r
Scrambler("Senegal")
```

```
## [1] "aneeglS"
```

```r
Scrambler("Minnesota")
```

```
## [1] "tMeinnaso"
```


```r

VowelBleeper <- function(x) {
    letters <- unlist(strsplit(x, ""))
    Vowels <- "[aeiou]"  #  c('e','o','a','e','i','y')
    R <- gsub(Vowels, "*", x)
    paste(R, collapse = "")
}
```

```r
# VowelBleeper test
VowelBleeper("computer")
```

```
## [1] "c*mp*t*r"
```


```

```

```


