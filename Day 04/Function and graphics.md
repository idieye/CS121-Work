Functions and graphics deliverable
========================================================


```r
# How many odds
oddcount <- function(x) {
    sum((x%%2 == 0) == FALSE)
}
```


```r
# oddcount Test
oddcount(c(1, 2, 3, 4, 5, 6, 7))
```

```
## [1] 4
```

```r
oddcount(c(25, 26, 39, 43, 1001, 91, 33))
```

```
## [1] 6
```

```r
oddcount(c(96, 20, 24, 78, 100, 32))
```

```
## [1] 0
```

```r
# How many evens
evencount <- function(x) {
    sum((x%%2) == 0)
}
```

```r
# evencount test
evencount(c(1, 2, 3, 4, 5, 6, 7))
```

```
## [1] 3
```

```r
evencount(c(25, 26, 39, 43, 1001, 91, 33))
```

```
## [1] 1
```

```r
evencount(c(96, 20, 24, 78, 100, 32))
```

```
## [1] 6
```


```r
# HypothenuseLength
HypothenuseLength <- function(a, b) {
    c = sqrt(a^2 + b^2)
    return(c)
}
```



```r
# Hypothenuse Length test
HypothenuseLength(4, 3)
```

```
## [1] 5
```


```

```r
# LawOfcosine
LawOfcosine <- function(a, b, theta) {
    c = sqrt(a^2 + b^2 - 2 * a * b * cos(theta))
    return(c)
}
```


```r
# LawOfcosine Test
LawOfcosine(13, 84, pi/2)
```

```
## [1] 85
```

```r
LawOfcosine(2, 3, pi/2)
```

```
## [1] 3.606
```

```r
LawOfcosine(3, 2, pi/4)
```

```
## [1] 2.125
```

```r
LawOfcosine(3, 2, pi/6)
```

```
## [1] 1.615
```

```r
LawOfcosine(3, 4, pi/2)
```

```
## [1] 5
```



```r
# Find angle
angleFinder <- function(a, b, c) {
    theta = acos((c^2 - a^2 - b^2)/(-2 * a * b))
    return(theta)
}
```


```r
angleFinder(3, 4, 5)
```

```
## [1] 1.571
```

```r
angleFinder(13, 84, 85)
```

```
## [1] 1.571
```

```r
angleFinder(3, 2, 2.125)
```

```
## [1] 0.7855
```

```r

# Graphics

```

```r
# Circles
circle <- function(x, y, r, ...) {
    ang <- seq(0, 2 * pi, length = 100)
    xx <- x + r * cos(ang)
    yy <- y + r * sin(ang)
    polygon(xx, yy, ...)
    Plot(xx)
}
```

```r
circle(0, 0, 5)
```

```
## Error: plot.new has not been called yet
```


