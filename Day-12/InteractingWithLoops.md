Day 12 deliverable: interacting with loops
========================================================

```r
# Testing human response times
getData <- function(N) {
    for (k in 1:N) {
        before <- Sys.time
        readline("Press return:")
        after <- Sys.time()
        delay <- as.numeric(after - before)
        cat(rep("\n", 20))
        result[k] <- delay
        Sys.sleep(runif(1, min = 1, max = 5))
    }
    return(result)
}
```



