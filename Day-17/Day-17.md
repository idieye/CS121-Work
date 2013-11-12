Day-17
========================================================

```r
require(COMP121)
```

```
## Loading required package: COMP121 Loading required package: jpeg Loading
## required package: png Loading required package: RCurl Loading required
## package: bitops Loading required package: markdown
```

```r
# Generate a plane of colors

## Utility Functions
ShowImage <- function(image) {
    size <- dim(image)
    canvas(x = c(1, size[2]), y = c(1, size[1]), asp = 1)
    rasterImage(image, 1, 1, size[2], size[1])
}

# vvvvvvvvvvvvvvvvvvvvvvvvvvvv ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

planeBind <- function(red, green, blue) {
    array(c(red, green, blue), dim <- c(dim(red)[1], dim(red)[2], 3))
}
# ==========================
colorPlane <- function(npixels = 50, howMuchBlue = 0.5) {
    
    x <- seq(0, 1, length = npixels)
    
    # initialize state
    red <- matrix(0, nrow = npixels, ncol = npixels)
    for (k in 1:npixels) {
        # update
        red[, k] <- cbind(x)
    }
    
    green <- matrix(0, nrow = npixels, ncol = npixels)
    for (k in 1:npixels) {
        green[k, ] <- rbind(x)
    }
    
    blue <- matrix(howMuchBlue, nrow = npixels, ncol = npixels)
    
    return(planeBind(red, green, blue))
}

ShowImage(colorPlane(howMuchBlue = 1, npixels = 50))
```

![plot of chunk unnamed-chunk-1](figure/unnamed-chunk-1.png) 

```r
require(manipulate)
```

```
## Loading required package: manipulate
```

```r
manipulate({
    plot(1:2)
}, blue = slider(0, 1, step = 0.01, label = "Amount of Blue"))
```

```
## Error: no such symbol rs_createUUID
```
